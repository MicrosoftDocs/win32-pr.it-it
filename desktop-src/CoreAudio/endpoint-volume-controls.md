---
description: Controlli volume endpoint
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: Controlli volume endpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526403be9c600f67791650956bd7e5096f6c9afc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966180"
---
# <a name="endpoint-volume-controls"></a>Controlli volume endpoint

Le interfacce [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) consentono ai client di controllare i livelli di volume delle [sessioni audio](audio-sessions.md), ovvero raccolte di flussi audio in modalità condivisa. Queste interfacce non funzionano con flussi audio in modalità esclusiva.

Le applicazioni che gestiscono flussi in modalità esclusiva possono controllare i livelli di volume di tali flussi tramite l'interfaccia [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) . Questa interfaccia controlla il livello del volume del [dispositivo dell'endpoint audio](audio-endpoint-devices.md). Usa il controllo volume hardware per il dispositivo endpoint se l'hardware audio implementa tale controllo. In caso contrario, l'interfaccia **IAudioEndpointVolume** implementa il controllo del volume nel software.

Se un dispositivo dispone di un controllo volume hardware, le modifiche apportate al controllo tramite l'interfaccia [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) influiscono sul livello del volume sia in modalità condivisa che in modalità esclusiva. Se un dispositivo non dispone di controlli di volume e silenziamento hardware, le modifiche apportate al volume software e ai controlli di silenziamento tramite questa interfaccia influiscono sul livello del volume in modalità condivisa, ma non in modalità esclusiva. In modalità esclusiva, l'applicazione e l'hardware audio scambiano direttamente i dati audio, ignorando i controlli software.

Come regola generale, le applicazioni devono evitare di usare l'interfaccia [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) per controllare i livelli di volume dei flussi in modalità condivisa. Al contrario, le applicazioni devono usare l'interfaccia [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)o [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) a tale scopo.

Se in un'applicazione viene visualizzato un controllo volume che utilizza l'interfaccia [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) per controllare il livello di volume di un dispositivo dell'endpoint audio, il controllo volume deve rispecchiare il controllo volume endpoint visualizzato dal programma di controllo del volume di sistema, sndvol. Come spiegato in precedenza, il controllo volume endpoint viene visualizzato sul lato sinistro della finestra sndvol, nella casella di gruppo etichetta **dispositivo**. Se l'utente modifica il volume dell'endpoint di un dispositivo tramite il controllo volume in sndvol, il controllo del volume dell'endpoint corrispondente nell'applicazione dovrebbe essere spostato all'uniformità con il controllo in sndvol. Analogamente, se l'utente modifica il livello del volume tramite il controllo volume endpoint nella finestra dell'applicazione, il controllo volume corrispondente in sndvol dovrebbe essere spostato all'uniformità con il controllo volume dell'applicazione.

Per assicurarsi che il controllo volume endpoint in una finestra dell'applicazione rispecchi il controllo volume endpoint in sndvol, l'applicazione deve implementare un'interfaccia [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) e registrare tale interfaccia per ricevere le notifiche. Successivamente, ogni volta che l'utente modifica il livello di volume dell'endpoint in sndvol, l'applicazione riceve una chiamata di notifica tramite il relativo metodo [**IAudioEndpointVolumeCallback:: OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) . Durante questa chiamata, il metodo **OnNotify** può aggiornare il controllo volume endpoint nella finestra dell'applicazione in modo che corrisponda all'impostazione di controllo mostrata in sndvol. Analogamente, ogni volta che l'utente modifica il livello di volume dell'endpoint tramite il controllo del volume nella finestra dell'applicazione, sndvol riceve una notifica e aggiorna immediatamente il controllo del volume dell'endpoint per visualizzare il nuovo livello di volume.

L'esempio di codice seguente è un file di intestazione che mostra una possibile implementazione dell'interfaccia [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) :


```C++
// Epvolume.h -- Implementation of IAudioEndpointVolumeCallback interface

#include <windows.h>
#include <commctrl.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

// Dialog handle from dialog box procedure
extern HWND g_hDlg;

// Client's proprietary event-context GUID
extern GUID g_guidMyContext;

// Maximum volume level on trackbar
#define MAX_VOL  100

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// Client implementation of IAudioEndpointVolumeCallback
// interface. When a method in the IAudioEndpointVolume
// interface changes the volume level or muting state of the
// endpoint device, the change initiates a call to the
// client's IAudioEndpointVolumeCallback::OnNotify method.
//-----------------------------------------------------------
class CAudioEndpointVolumeCallback : public IAudioEndpointVolumeCallback
{
    LONG _cRef;

public:
    CAudioEndpointVolumeCallback() :
        _cRef(1)
    {
    }

    ~CAudioEndpointVolumeCallback()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;

    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioEndpointVolumeCallback) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioEndpointVolumeCallback*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback method for endpoint-volume-change notifications.

    HRESULT STDMETHODCALLTYPE OnNotify(PAUDIO_VOLUME_NOTIFICATION_DATA pNotify)
    {
        if (pNotify == NULL)
        {
            return E_INVALIDARG;
        }
        if (g_hDlg != NULL && pNotify->guidEventContext != g_guidMyContext)
        {
            PostMessage(GetDlgItem(g_hDlg, IDC_CHECK_MUTE), BM_SETCHECK,
                        (pNotify->bMuted) ? BST_CHECKED : BST_UNCHECKED, 0);

            PostMessage(GetDlgItem(g_hDlg, IDC_SLIDER_VOLUME),
                        TBM_SETPOS, TRUE,
                        LPARAM((UINT32)(MAX_VOL*pNotify->fMasterVolume + 0.5)));
        }
        return S_OK;
    }
};
```



La classe CAudioEndpointVolumeCallback nell'esempio di codice precedente è un'implementazione dell'interfaccia [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) . Poiché **IAudioEndpointVolumeCallback** eredita da [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), la definizione della classe contiene le implementazioni dei metodi **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)e [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Il metodo [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) nella definizione della classe viene chiamato ogni volta che uno dei metodi seguenti modifica il livello del volume dell'endpoint:

-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume:: semute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

L'implementazione del metodo [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) nell'esempio di codice precedente invia messaggi al controllo volume nella finestra dell'applicazione per aggiornare il livello del volume visualizzato.

Un'applicazione chiama il metodo [**IAudioEndpointVolume:: RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) per registrare l'interfaccia [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) per la ricezione delle notifiche. Quando l'applicazione non richiede più notifiche, chiama il metodo [**IAudioEndpointVolume:: UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) per eliminare la registrazione.

L'esempio di codice seguente è un'applicazione Windows che chiama i metodi [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) e [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) per registrare e annullare la registrazione della classe CAudioEndpointVolumeCallback nell'esempio di codice precedente:


```C++
// Epvolume.cpp -- WinMain and dialog box functions

#include "stdafx.h"
#include "Epvolume.h"

HWND g_hDlg = NULL;
GUID g_guidMyContext = GUID_NULL;

static IAudioEndpointVolume *g_pEndptVol = NULL;
static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define ERROR_CANCEL(hr)  \
              if (FAILED(hr)) {  \
                  MessageBox(hDlg, TEXT("The program will exit."),  \
                             TEXT("Fatal error"), MB_OK);  \
                  EndDialog(hDlg, TRUE); return TRUE; }

//-----------------------------------------------------------
// WinMain -- Registers an IAudioEndpointVolumeCallback
//   interface to monitor endpoint volume level, and opens
//   a dialog box that displays a volume control that will
//   mirror the endpoint volume control in SndVol.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    CAudioEndpointVolumeCallback EPVolEvents;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    hr = CoCreateGuid(&g_guidMyContext);
    EXIT_ON_ERROR(hr)

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioEndpointVolume),
                           CLSCTX_ALL, NULL, (void**)&g_pEndptVol);
    EXIT_ON_ERROR(hr)

    hr = g_pEndptVol->RegisterControlChangeNotify(
                     (IAudioEndpointVolumeCallback*)&EPVolEvents);
    EXIT_ON_ERROR(hr)

    InitCommonControls();
    DialogBox(hInstance, L"VOLUMECONTROL", NULL, (DLGPROC)DlgProc);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    if (pEnumerator != NULL)
    {
        g_pEndptVol->UnregisterControlChangeNotify(
                    (IAudioEndpointVolumeCallback*)&EPVolEvents);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(g_pEndptVol)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    HRESULT hr;
    BOOL bMute;
    float fVolume;
    int nVolume;
    int nChecked;

    switch (message)
    {
    case WM_INITDIALOG:
        g_hDlg = hDlg;
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMIN, FALSE, 0);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMAX, FALSE, MAX_VOL);
        hr = g_pEndptVol->GetMute(&bMute);
        ERROR_CANCEL(hr)
        SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK,
                           bMute ? BST_CHECKED : BST_UNCHECKED, 0);
        hr = g_pEndptVol->GetMasterVolumeLevelScalar(&fVolume);
        ERROR_CANCEL(hr)
        nVolume = (int)(MAX_VOL*fVolume + 0.5);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETPOS, TRUE, nVolume);
        return TRUE;

    case WM_HSCROLL:
        switch (LOWORD(wParam))
        {
        case SB_THUMBPOSITION:
        case SB_THUMBTRACK:
        case SB_LINERIGHT:
        case SB_LINELEFT:
        case SB_PAGERIGHT:
        case SB_PAGELEFT:
        case SB_RIGHT:
        case SB_LEFT:
            // The user moved the volume slider in the dialog box.
            SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK, BST_UNCHECKED, 0);
            hr = g_pEndptVol->SetMute(FALSE, &g_guidMyContext);
            ERROR_CANCEL(hr)
            nVolume = SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_GETPOS, 0, 0);
            fVolume = (float)nVolume/MAX_VOL;
            hr = g_pEndptVol->SetMasterVolumeLevelScalar(fVolume, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        }
        break;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDC_CHECK_MUTE:
            // The user selected the Mute check box in the dialog box.
            nChecked = SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_GETCHECK, 0, 0);
            bMute = (BST_CHECKED == nChecked);
            hr = g_pEndptVol->SetMute(bMute, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        case IDCANCEL:
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;
    }
    return FALSE;
}
```



Nell'esempio di codice precedente, la funzione [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) chiama la [**funzione CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza dell'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) e chiama il metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo di rendering predefinito. **WinMain** chiama il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per ottenere l'interfaccia [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) del dispositivo e chiama [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) per registrare l'applicazione per ricevere le notifiche delle modifiche del volume dell'endpoint. Quindi, **WinMain** apre una finestra di dialogo per visualizzare un controllo volume endpoint per il dispositivo. Nella finestra di dialogo viene visualizzata anche una casella di controllo che indica se il dispositivo è disattivato. Il controllo del volume dell'endpoint e la casella di controllo mute nella finestra di dialogo rispecchiano le impostazioni della casella di controllo volume endpoint e mute visualizzata da sndvol. Per ulteriori informazioni su **WinMain** e **CoCreateInstance**, vedere la documentazione di Windows SDK. Per ulteriori informazioni su **IMMDeviceEnumerator** e **IMMDevice**, vedere [enumerazione di dispositivi audio](enumerating-audio-devices.md).

La routine della finestra di dialogo, DlgProc, nell'esempio di codice precedente, gestisce le modifiche apportate dall'utente al volume e disattiva le impostazioni tramite i controlli della finestra di dialogo. Quando DlgProc chiama [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) o [**semute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), sndvol riceve la notifica della modifica e aggiorna il controllo corrispondente nella finestra per riflettere il nuovo volume o l'impostazione di mute. Se, invece di usare la finestra di dialogo, l'utente aggiorna le impostazioni volume e mute tramite i controlli della finestra sndvol, il metodo [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) nella classe CAudioEndpointVolumeCallback aggiorna i controlli della finestra di dialogo per visualizzare le nuove impostazioni.

Se l'utente modifica il volume tramite i controlli della finestra di dialogo, il metodo [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) nella classe CAudioEndpointVolumeCallback non invia messaggi per aggiornare i controlli nella finestra di dialogo. A tale scopo, sarebbe ridondante. **OnNotify** aggiorna i controlli della finestra di dialogo solo se la modifica del volume ha avuto origine in sndvol o in un'altra applicazione. Il secondo parametro nelle chiamate al metodo [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) e [**semute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) nella funzione DlgProc è un puntatore a un GUID del contesto evento che uno dei due metodi passa a **OnNotify**. **OnNotify** controlla il valore del GUID del contesto evento per determinare se la finestra di dialogo è l'origine della modifica del volume. Per ulteriori informazioni sui GUID del contesto degli eventi, vedere **IAudioEndpointVolumeCallback:: OnNotify**.

Quando l'utente esce dalla finestra di dialogo, la chiamata [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) nell'esempio di codice precedente elimina la registrazione della classe CAudioEndpointVolumeCallback prima della terminazione del programma.

È possibile modificare facilmente l'esempio di codice precedente per visualizzare i controlli volume e mute per il dispositivo di acquisizione predefinito. Nella funzione [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) , modificare il valore del primo parametro nella chiamata al metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) da eRender a eCapture.

L'esempio di codice seguente è lo script di risorsa che definisce il volume e i controlli di silenziamento visualizzati nell'esempio di codice precedente:


```C++
// Epvolume.rc -- Resource script

#include "resource.h"
#include "windows.h"
#include "commctrl.h"

//
// Dialog box
//
VOLUMECONTROL DIALOGEX 0, 0, 160, 60
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Audio Endpoint Volume"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    LTEXT      "Min",IDC_STATIC_MINVOL,10,10,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,130,10,20,12
    CONTROL    "",IDC_SLIDER_VOLUME,"msctls_trackbar32",
               TBS_BOTH | TBS_NOTICKS | WS_TABSTOP,10,20,140,12
    CONTROL    "Mute",IDC_CHECK_MUTE,"Button",
               BS_AUTOCHECKBOX | WS_TABSTOP,20,40,70,12
END
```



L'esempio di codice seguente è il file di intestazione della risorsa che definisce gli identificatori di controllo visualizzati negli esempi di codice precedenti:


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



Gli esempi di codice precedenti si combinano per formare una semplice applicazione per il controllo e il monitoraggio del volume dell'endpoint del dispositivo di rendering predefinito. Un'applicazione più utile può inoltre notificare all'utente quando lo stato del dispositivo cambia. Ad esempio, il dispositivo potrebbe essere disabilitato, scollegato o rimosso. Per altre informazioni sul monitoraggio di questi tipi di eventi, vedere [eventi del dispositivo](device-events.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli del volume](volume-controls.md)
</dt> </dl>

 

 
