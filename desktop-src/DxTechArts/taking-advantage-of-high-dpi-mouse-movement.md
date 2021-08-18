---
title: Sfruttare i vantaggi del High-Definition del mouse
description: Questo articolo illustra il modo migliore per ottimizzare le prestazioni dell'input del mouse ad alta definizione in un gioco come un gioco in prima persona.
ms.assetid: 0138a248-e8e0-a392-564e-7a9229b94b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d7a6efe6916ad8605e3cdc056ffd716ac5113b66c022b0a95fd8a78b1a62e30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042391"
---
# <a name="taking-advantage-of-high-definition-mouse-movement"></a>Sfruttare i vantaggi del High-Definition del mouse

Un mouse standard del computer restituisce dati a 400 punti per pollice (DPI), mentre un mouse ad alta definizione genera dati con un valore di 800 DPI o superiore. In questo modo l'input da un mouse ad alta definizione è molto più preciso rispetto a quello di un mouse standard. Non è tuttavia possibile ottenere dati ad alta definizione tramite i messaggi \_ WM MOUSEMOVE standard. In generale, i giochi trarranno vantaggio dai dispositivi mouse ad alta definizione, ma i giochi che ottengono i dati del mouse usando solo WM MOUSEMOVE non saranno in grado di accedere alla risoluzione completa e non filtrata \_ del mouse.

Diverse aziende stanno producendo dispositivi mouse ad alta definizione, ad esempio Microsoft e Logitech. Con la crescente diffusione dei dispositivi mouse ad alta risoluzione, è importante che gli sviluppatori comprendano come usare in modo ottimale le informazioni generate da questi dispositivi. Questo articolo illustra il modo migliore per ottimizzare le prestazioni dell'input del mouse ad alta definizione in un gioco come un gioco in prima persona.

## <a name="retrieving-mouse-movement-data"></a>Recupero dei dati di spostamento del mouse

Ecco i tre metodi principali per recuperare i dati del mouse:

-   [WM \_ MOUSEMOVE](/windows)
-   [WM \_ INPUT](/windows)
-   [DirectInput](#directinput)

Ogni metodo presenta vantaggi e svantaggi, a seconda di come verranno usati i dati.

### <a name="wm_mousemove"></a>WM \_ MOUSEMOVE

Il metodo più semplice per leggere i dati di spostamento del mouse è tramite messaggi WM \_ MOUSEMOVE. Di seguito è riportato un esempio di come leggere i dati di spostamento del mouse dal messaggio WM \_ MOUSEMOVE:

```cpp
case WM_MOUSEMOVE:
{
    int xPosAbsolute = GET_X_PARAM(lParam); 
    int yPosAbsolute = GET_Y_PARAM(lParam);
    // ...
    break;
}
```

Lo svantaggio principale dei dati di WM MOUSEMOVE è che \_ sono limitati alla risoluzione dello schermo. Ciò significa che se si sposta leggermente il mouse, ma non è sufficiente per fare in modo che il puntatore si sposti al pixel successivo, non viene generato alcun messaggio \_ MOUSEMOVE WM. Pertanto, l'uso di questo metodo per leggere lo spostamento del mouse nega i vantaggi dell'input ad alta definizione.

Il vantaggio di WM MOUSEMOVE, tuttavia, è che Windows applica l'accelerazione del puntatore (nota anche come ballistica) ai dati non elaborati del mouse, il che fa sì che il puntatore del mouse si comporti come previsto dai \_ clienti. In questo modo WM MOUSEMOVE è l'opzione preferita per il controllo del puntatore (su WM INPUT o DirectInput), perché comporta \_ un comportamento più naturale per gli \_ utenti. Anche se WM MOUSEMOVE è ideale per lo spostamento dei puntatori del mouse, non è ideale per spostare una fotocamera in prima persona, perché la precisione ad alta definizione \_ andrà persa.

Per altre informazioni su WM \_ MOUSEMOVE, vedere [**WM \_ MOUSEMOVE.**](/windows/desktop/inputdev/wm-mousemove)

### <a name="wm_input"></a>WM \_ INPUT

Il secondo metodo per ottenere i dati del mouse è leggere i messaggi WM \_ INPUT. L'elaborazione dei messaggi WM INPUT è più complessa rispetto all'elaborazione dei messaggi MOUSEMOVE WM, ma i messaggi WM INPUT vengono letti direttamente dallo \_ \_ stack HID (Human Interface Device) e riflettono i risultati \_ ad alta definizione.

Per leggere i dati di spostamento del mouse dal messaggio WM INPUT, il dispositivo deve prima essere registrato. Il \_ codice seguente fornisce un esempio:

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

Il codice seguente gestisce i messaggi \_ WM INPUT nel gestore WinProc dell'applicazione:

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

Il vantaggio dell'uso di WM INPUT è che il gioco riceve dati \_ non elaborati dal mouse al livello più basso possibile.

Lo svantaggio è che WM INPUT non ha alcuna ballistica applicata ai dati, quindi se si vuole guidare un cursore con questi dati, sarà necessario un impegno aggiuntivo per fare in modo che il cursore si comporti come \_ in Windows. Per altre informazioni sull'applicazione della ballistica dei puntatori, vedere [Pointer Ballistics for Windows XP](https://www.microsoft.com/whdc/archive/pointer-bal.mspx).

Per altre informazioni su WM \_ INPUT, vedi [Informazioni sull'input non elaborato.](/windows/desktop/inputdev/about-raw-input)

### <a name="directinput"></a>DirectInput

[DirectInput](/windows-hardware/drivers/hid/directinput) è un set di chiamate API che astrae i dispositivi di input nel sistema. Internamente, DirectInput crea un secondo thread per leggere i dati WM INPUT e l'uso delle API DirectInput aggiungerà più overhead rispetto alla semplice lettura \_ diretta di WM \_ INPUT. DirectInput è utile solo per la lettura dei dati daistick DirectInput; Tuttavia, se è necessario supportare solo il controller Xbox 360 per Windows, usare [invece XInput.](/windows/desktop/xinput/xinput-game-controller-apis-portal) In generale, l'uso di DirectInput non offre vantaggi durante la lettura dei dati da dispositivi mouse o tastiera e l'uso di DirectInput in questi scenari è sconsigliato.

Confrontare la complessità dell'uso [di DirectInput,](/windows-hardware/drivers/hid/directinput)illustrato nel codice seguente, con i metodi descritti in precedenza. Per creare un mouse DirectInput, è necessario il set di chiamate seguente:

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

E quindi il dispositivo mouse DirectInput può essere letto per ogni fotogramma:

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

In generale, il metodo migliore per ricevere dati di spostamento del mouse ad alta definizione è WM \_ INPUT. Se gli utenti spostano semplicemente un puntatore del mouse, valuta la possibilità di usare WM MOUSEMOVE per evitare di dover eseguire la \_ pallatura del puntatore. Entrambi i messaggi della finestra funzioneranno correttamente anche se il mouse non è un mouse ad alta definizione. Supportando l'alta definizione, Windows giochi possono offrire un controllo più preciso agli utenti.