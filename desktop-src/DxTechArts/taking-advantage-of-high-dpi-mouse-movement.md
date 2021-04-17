---
title: Sfruttamento del movimento del mouse High-Definition
description: Questo articolo è incentrato sul modo migliore per ottimizzare le prestazioni di input del mouse ad alta definizione in un gioco come uno sparatutto di prima persona.
ms.assetid: 0138a248-e8e0-a392-564e-7a9229b94b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebe2abd9487d95b8fe12aa3c6938e21d72d8e2f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399407"
---
# <a name="taking-advantage-of-high-definition-mouse-movement"></a>Sfruttamento del movimento del mouse High-Definition

Un mouse standard del computer restituisce i dati a 400 punti per pollice (DPI), mentre un mouse ad alta definizione genera dati a 800 DPI o superiore. In questo modo l'input da un mouse ad alta definizione è molto più preciso rispetto a quello di un mouse standard. Tuttavia, i dati ad alta definizione non possono essere ottenuti tramite i messaggi standard di WM \_ MOUSEMOVE. In generale, i giochi trarranno vantaggio da dispositivi mouse ad alta definizione, ma i giochi che ottengono dati del mouse usando solo WM \_ MOUSEMOVE non saranno in grado di accedere alla soluzione completa e non filtrata del mouse.

Una serie di aziende sta producendo dispositivi mouse a definizione elevata, ad esempio Microsoft e Logitech. Con la crescente popolarità dei dispositivi mouse ad alta risoluzione, è importante che gli sviluppatori apprendano come usare le informazioni generate da questi dispositivi in modo ottimale. Questo articolo è incentrato sul modo migliore per ottimizzare le prestazioni di input del mouse ad alta definizione in un gioco come uno sparatutto di prima persona.

## <a name="retrieving-mouse-movement-data"></a>Recupero dei dati di spostamento del mouse

Di seguito sono riportati i tre metodi principali per recuperare i dati del mouse:

-   [MOUSEMOVE di WM \_](/windows)
-   [\_input WM](/windows)
-   [DirectInput](#directinput)

Ogni metodo presenta vantaggi e svantaggi, a seconda della modalità di utilizzo dei dati.

### <a name="wm_mousemove"></a>MOUSEMOVE di WM \_

Il metodo più semplice per leggere i dati di spostamento del mouse è tramite \_ i messaggi WM MOUSEMOVE. Di seguito è riportato un esempio di come leggere i dati di spostamento del mouse dal messaggio di WM \_ MOUSEMOVE:

```cpp
case WM_MOUSEMOVE:
{
    int xPosAbsolute = GET_X_PARAM(lParam); 
    int yPosAbsolute = GET_Y_PARAM(lParam);
    // ...
    break;
}
```

Lo svantaggio principale dei dati di WM \_ MOUSEMOVE è che è limitato alla risoluzione dello schermo. Ciò significa che se si sposta leggermente il mouse, ma non è sufficiente per fare in modo che il puntatore si sposti sul pixel successivo, non \_ viene generato alcun messaggio di WM MOUSEMOVE. Pertanto, l'utilizzo di questo metodo per la lettura del movimento del mouse nega i vantaggi dell'input ad alta definizione.

Il vantaggio di WM \_ MOUSEMOVE, tuttavia, è che Windows applica l'accelerazione del puntatore, nota anche come balistica, ai dati del mouse non elaborati, che rendono il puntatore del mouse si comportano come previsto dai clienti. \_In questo modo WM MOUSEMOVE è l'opzione preferita per il controllo puntatore (over WM \_ input o DirectInput), in quanto comporta un comportamento più naturale per gli utenti. Anche se WM \_ MOUSEMOVE è ideale per lo spostamento di puntatori del mouse, non è così adatto per lo spostamento di una fotocamera di prima persona, perché la precisione ad alta definizione andrà persa.

Per altre informazioni su WM \_ MouseMove, vedere [**WM \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove).

### <a name="wm_input"></a>\_input WM

Il secondo metodo per ottenere i dati del mouse consiste nel leggere \_ i messaggi di input WM. L'elaborazione \_ dei messaggi di input WM è più complessa rispetto \_ all'elaborazione dei messaggi di WM MOUSEMOVE, ma \_ i messaggi di input WM vengono letti direttamente dallo stack HID (Human Interface Device) e riflettono i risultati ad alta definizione.

Per leggere i dati del movimento del mouse dal \_ messaggio di input WM, il dispositivo deve prima essere registrato. il codice seguente fornisce un esempio:

```cpp
// you can #include <hidusage.h> for these defines
#ifndef HID_USAGE_PAGE_GENERIC
#define HID_USAGE_PAGE_GENERIC         ((USHORT) 0x01)
#endif
#ifndef HID_USAGE_GENERIC_MOUSE
#define HID_USAGE_GENERIC_MOUSE        ((USHORT) 0x02)
#endif

RAWINPUTDEVICE Rid[1];
Rid[0].usUsagePage = HID_USAGE_PAGE_GENERIC; 
Rid[0].usUsage = HID_USAGE_GENERIC_MOUSE; 
Rid[0].dwFlags = RIDEV_INPUTSINK;   
Rid[0].hwndTarget = hWnd;
RegisterRawInputDevices(Rid, 1, sizeof(Rid[0]));
```

Il codice seguente gestisce i \_ messaggi di input WM nel gestore WinProc dell'applicazione:

```cpp
case WM_INPUT: 
{
    UINT dwSize = sizeof(RAWINPUT);
    static BYTE lpb[sizeof(RAWINPUT)];

    GetRawInputData((HRAWINPUT)lParam, RID_INPUT, lpb, &dwSize, sizeof(RAWINPUTHEADER));

    RAWINPUT* raw = (RAWINPUT*)lpb;

    if (raw->header.dwType == RIM_TYPEMOUSE) 
    {
        int xPosRelative = raw->data.mouse.lLastX;
        int yPosRelative = raw->data.mouse.lLastY;
    } 
    break;
}
```

Il vantaggio dell'uso di WM \_ input è che il gioco riceve dati non elaborati dal mouse al livello più basso possibile.

Lo svantaggio è che \_ all'input WM non è applicata alcuna balistica ai propri dati, quindi se si vuole guidare un cursore con questi dati, è necessario ulteriore sforzo per far sì che il cursore si comporti come in Windows. Per ulteriori informazioni sull'applicazione di un indicatore di misura balistico, vedere la pagina relativa [ai puntatori balistici per Windows XP](https://www.microsoft.com/whdc/archive/pointer-bal.mspx).

Per altre informazioni sull' \_ input WM, vedere [About RAW input](/windows/desktop/inputdev/about-raw-input).

### <a name="directinput"></a>DirectInput

[DirectInput](/windows-hardware/drivers/hid/directinput) è un set di chiamate API che astrae i dispositivi di input nel sistema. Internamente, DirectInput crea un secondo thread per leggere \_ i dati di input WM e l'uso delle API DirectInput aggiungerà un sovraccarico maggiore rispetto alla semplice lettura diretta di WM \_ input. DirectInput è utile solo per la lettura di dati da joystick DirectInput; Tuttavia, se è necessario supportare solo il controller Xbox 360 per Windows, usare [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) in alternativa. In generale, l'uso di DirectInput non offre alcun vantaggio durante la lettura dei dati dai dispositivi mouse o tastiera e l'uso di DirectInput in questi scenari è sconsigliato.

Confrontare la complessità dell'uso di [DirectInput](/windows-hardware/drivers/hid/directinput), illustrato nel codice seguente, ai metodi descritti in precedenza. Per creare un mouse DirectInput, sono necessari i set di chiamate seguenti:

```cpp
LPDIRECTINPUT8 pDI;
LPDIRECTINPUTDEVICE8 pMouse;

hr = DirectInput8Create(GetModuleHandle(NULL), DIRECTINPUT_VERSION, IID_IDirectInput8, (VOID**)&pDI, NULL);
if(FAILED(hr))
    return hr;

hr = pDI->CreateDevice(GUID_SysMouse, &pMouse, NULL);
if(FAILED(hr))
    return hr;

hr = pMouse->SetDataFormat(&c_dfDIMouse2);
if(FAILED(hr))
    return hr;

hr = pMouse->SetCooperativeLevel(hWnd, DISCL_NONEXCLUSIVE | DISCL_FOREGROUND);
if(FAILED(hr))
    return hr;

if(!bImmediate)
{
    DIPROPDWORD dipdw;
    dipdw.diph.dwSize       = sizeof(DIPROPDWORD);
    dipdw.diph.dwHeaderSize = sizeof(DIPROPHEADER);
    dipdw.diph.dwObj        = 0;
    dipdw.diph.dwHow        = DIPH_DEVICE;
    dipdw.dwData            = 16; // Arbitrary buffer size

    if(FAILED(hr = pMouse->SetProperty(DIPROP_BUFFERSIZE, &dipdw.diph)))
        return hr;
}

pMouse->Acquire();
```

Quindi il dispositivo DirectInput mouse può essere letto ogni frame:

```cpp
DIMOUSESTATE2 dims2; 
ZeroMemory(&dims2, sizeof(dims2));

hr = pMouse->GetDeviceState(sizeof(DIMOUSESTATE2), &dims2);
if(FAILED(hr)) 
{
    hr = pMouse->Acquire();
    while(hr == DIERR_INPUTLOST) 
        hr = pMouse->Acquire();

    return S_OK; 
}

int xPosRelative = dims2.lX;
int yPosRelative = dims2.lY;
```

## <a name="summary"></a>Riepilogo

Complessivamente, il metodo migliore per ricevere dati di spostamento del mouse ad alta definizione è l' \_ input WM. Se gli utenti stanno semplicemente migrando un puntatore del mouse, provare a usare WM \_ MOUSEMOVE per evitare di dover eseguire la balistica del puntatore. Entrambi i messaggi della finestra funzioneranno correttamente anche se il mouse non è un mouse ad alta definizione. Grazie al supporto della definizione elevata, i giochi di Windows possono offrire un controllo più preciso agli utenti.