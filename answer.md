# 第2次練習題目-隨堂-QZ2
>
>學號：113111132
><br />
>姓名：曹翔凱
><br />
>作業撰寫時間：150 mins
><br />
>最後撰寫文件日期：2026/10/24
>

## 說明內容

本題使用 Unity 新版輸入系統，在 `PlayerController.cs` 的 `Update()` 方法中加入鍵盤輸入偵測。

1. **W 鍵偵測：** 使用 `Keyboard.current.wKey.isPressed` 判斷 W 鍵是否按住。按住時，使用 `Debug.Log` 在 Unity Console 印出「玩家按了W鍵!」訊息。
2. **A、S、D 鍵偵測：** 程式會持續檢查玩家是否按下 A、S 或 D 鍵，按下時就在 Unity Console 顯示對應訊息，例如按下 A 鍵會顯示「玩家按了A鍵!」。

以下分別呈現 W 鍵與 A、S、D 鍵的程式碼、執行結果及程式說明。



ANS:
![W 鍵程式碼說明截圖](1A.png)
![按下 W 鍵主控台執行結果](W_key.png)

#### 程式說明

- **第 1 列 `using UnityEngine;`**  
  引入 Unity 核心引擎命名空間，啟用 Unity 內建的基本功能。
- **第 2 列 `using UnityEngine.InputSystem;`**  
  引入新版輸入系統工具箱，使程式能夠識別鍵盤與按鍵。
- **第 4～5 列 `public class PlayerController : MonoBehaviour {`**  
  宣告與 C# 檔名相同的公開類別，並繼承 `MonoBehaviour` 以便掛載至場景物件上。
- **第 6～9 列 `void Start() { }`**  
  遊戲啟動時執行一次的初始化函式（本題無須初始化故留空）。
- **第 11～12 列 `void Update() {`**  
  遊戲執行期間每個影格自動重複執行的函式，用於即時偵測按鍵。
- **第 13 列 `// 題目 1：偵測 W 鍵`**  
  單行註解，用來說明程式用途，不影響執行。
- **第 14 列 `if (Keyboard.current.wKey.isPressed)`**  
  當鍵盤上的 W 鍵處於按住狀態時，執行下方動作。
- **第 15、17 列 `{` 與 `}`**  
  標示條件成立時執行的程式碼區塊範圍。
- **第 16 列 `Debug.Log("玩家按了W鍵!");`**  
  偵測到 W 鍵被按住時，在 Unity Console 印出指定訊息。


ANS：
![A、S、D 鍵程式碼說明截圖](2A.png)
![A、S、D 鍵主控台執行結果](asd_key.png)

#### 程式說明

- **第 20 列 `if (Keyboard.current.aKey.wasPressedThisFrame)`**  
  `Keyboard.current` 代表目前使用的鍵盤，`aKey` 代表 A 鍵。這行會檢查 A 鍵是不是剛剛被按下；如果是，就執行大括號中的程式。
- **第 21、23 列 `{` 與 `}`**  
  標示 A 鍵條件成立時要執行的程式碼範圍。
- **第 22 列 `Debug.Log("玩家按了A鍵!");`**  
  A 鍵被按下時，在 Unity Console 印出對應訊息。
- **第 24 列（空白列）**  
  用來區隔不同按鍵的偵測程式。
- **第 25 列 `if (Keyboard.current.sKey.wasPressedThisFrame)`**  
  `sKey` 代表 S 鍵。這行會檢查 S 鍵是不是剛剛被按下；如果是，就執行大括號中的程式。
- **第 26、28 列 `{` 與 `}`**  
  標示 S 鍵條件成立時要執行的程式碼範圍。
- **第 27 列 `Debug.Log("玩家按了S鍵!");`**  
  S 鍵被按下時，在 Unity Console 印出對應訊息。
- **第 29 列（空白列）**  
  用來區隔不同按鍵的偵測程式。
- **第 30 列 `if (Keyboard.current.dKey.wasPressedThisFrame)`**  
  `dKey` 代表 D 鍵。這行會檢查 D 鍵是不是剛剛被按下；如果是，就執行大括號中的程式。
- **第 31、33 列 `{` 與 `}`**  
  標示 D 鍵條件成立時要執行的程式碼範圍。
- **第 32 列 `Debug.Log("玩家按了D鍵!");`**  
  D 鍵被按下時，在 Unity Console 印出對應訊息。
- **第 34 列 `}`**  
  標示 `Update()` 函式程式碼區塊的結束。
- **第 35 列 `}`**  
  標示 `PlayerController` 類別程式碼區塊的結束。

## 其他

在 Unity 新增腳本的過程中遇到了不少狀況，例如腳本掛載到錯誤的物件，導致訊息沒有出現。透過反覆排錯與修正，我學會了正確的掛載方式。雖然除錯花了不少時間，但解決問題後，讓我對 Unity 的操作邏輯與腳本運作有了更進一步的理解。
