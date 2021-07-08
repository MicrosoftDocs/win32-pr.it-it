---
description: Controlli del volume degli endpoint
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: Controlli del volume degli endpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57be477a86a1de4584a7590d20d4e0199e782f10
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481886"
---
# <a name="endpoint-volume-controls"></a><span data-ttu-id="8fbdd-103">Controlli del volume degli endpoint</span><span class="sxs-lookup"><span data-stu-id="8fbdd-103">Endpoint Volume Controls</span></span>

<span data-ttu-id="8fbdd-104">Le interfacce [**ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) consentono ai client di controllare i livelli di volume delle sessioni [audio,](audio-sessions.md)ovvero raccolte di flussi audio in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-104">The [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces enable clients to control the volume levels of [audio sessions](audio-sessions.md), which are collections of shared-mode audio streams.</span></span> <span data-ttu-id="8fbdd-105">Queste interfacce non funzionano con i flussi audio in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-105">These interfaces do not work with exclusive-mode audio streams.</span></span>

<span data-ttu-id="8fbdd-106">Le applicazioni che gestiscono flussi in modalità esclusiva possono controllare i livelli di volume di tali flussi tramite [**l'interfaccia IAudioEndpointVolume.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-106">Applications that manage exclusive-mode streams can control the volume levels of those streams through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface.</span></span> <span data-ttu-id="8fbdd-107">Questa interfaccia controlla il livello del volume del [dispositivo endpoint audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="8fbdd-107">This interface controls the volume level of the [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="8fbdd-108">Usa il controllo del volume hardware per il dispositivo endpoint se l'hardware audio implementa tale controllo.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-108">It uses the hardware volume control for the endpoint device if the audio hardware implements such a control.</span></span> <span data-ttu-id="8fbdd-109">In caso contrario, **l'interfaccia IAudioEndpointVolume** implementa il controllo del volume nel software.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-109">Otherwise, the **IAudioEndpointVolume** interface implements the volume control in software.</span></span>

<span data-ttu-id="8fbdd-110">Se un dispositivo ha un controllo del volume hardware, le modifiche apportate al controllo tramite [**l'interfaccia IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) influiscono sul livello del volume sia in modalità condivisa che in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-110">If a device has a hardware volume control, changes made to the control through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface affect the volume level both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="8fbdd-111">Se un dispositivo non dispone di controlli del volume hardware e dell'audio, le modifiche apportate al volume software e i controlli di disattivazione tramite questa interfaccia influiscono sul livello del volume in modalità condivisa, ma non in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-111">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through this interface affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="8fbdd-112">In modalità esclusiva, l'applicazione e l'hardware audio scambiano direttamente i dati audio, ignorando i controlli software.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-112">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="8fbdd-113">Come regola generale, le applicazioni devono evitare di usare [**l'interfaccia IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) per controllare i livelli di volume dei flussi in modalità condivisa.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-113">As a general rule, applications should avoid using the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume levels of shared-mode streams.</span></span> <span data-ttu-id="8fbdd-114">Le applicazioni devono invece usare [**l'interfaccia ISimpleAudioVolume,**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)o [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-114">Instead, applications should use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), or [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interface for that purpose.</span></span>

<span data-ttu-id="8fbdd-115">Se un'applicazione visualizza un controllo del volume che usa [**l'interfaccia IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) per controllare il livello di volume di un dispositivo endpoint audio, tale controllo del volume deve rispecchiare il controllo del volume dell'endpoint visualizzato dal programma di controllo del volume di sistema, Sndvol.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-115">If an application displays a volume control that uses the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume level of an audio endpoint device, that volume control should mirror the endpoint volume control displayed by the system volume-control program, Sndvol.</span></span> <span data-ttu-id="8fbdd-116">Come illustrato in precedenza, il controllo del volume dell'endpoint viene visualizzato sul lato sinistro della finestra Sndvol, nella casella di gruppo con etichetta **Dispositivo**.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-116">As explained previously, the endpoint volume control appears on the left side of the Sndvol window, in the group box labeled **Device**.</span></span> <span data-ttu-id="8fbdd-117">Se l'utente modifica il volume dell'endpoint di un dispositivo tramite il controllo del volume in Sndvol, il controllo del volume dell'endpoint corrispondente nell'applicazione deve essere spostato all'unisono con il controllo in Sndvol.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-117">If the user changes the endpoint volume of a device through the volume control in Sndvol, the corresponding endpoint volume control in the application should move in unison with the control in Sndvol.</span></span> <span data-ttu-id="8fbdd-118">Analogamente, se l'utente modifica il livello del volume tramite il controllo del volume dell'endpoint nella finestra dell'applicazione, il controllo del volume corrispondente in Sndvol deve essere spostato all'unisono con il controllo del volume dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-118">Similarly, if the user changes the volume level through the endpoint volume control in the application window, the corresponding volume control in Sndvol should move in unison with the application's volume control.</span></span>

<span data-ttu-id="8fbdd-119">Per assicurarsi che il controllo del volume dell'endpoint in una finestra dell'applicazione rifletto il controllo del volume dell'endpoint in Sndvol, l'applicazione deve implementare [**un'interfaccia IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) e registrare tale interfaccia per ricevere le notifiche.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-119">To ensure that the endpoint volume control in an application window mirrors the endpoint volume control in Sndvol, the application should implement an [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface and register that interface to receive notifications.</span></span> <span data-ttu-id="8fbdd-120">Successivamente, ogni volta che l'utente modifica il livello del volume dell'endpoint in Sndvol, l'applicazione riceve una chiamata di notifica tramite il relativo metodo [**IAudioEndpointVolumeCallback::OnNotify.**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-120">Thereafter, each time the user changes the endpoint volume level in Sndvol, the application receives a notification call through its [**IAudioEndpointVolumeCallback::OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method.</span></span> <span data-ttu-id="8fbdd-121">Durante questa chiamata, il **metodo OnNotify** può aggiornare il controllo del volume dell'endpoint nella finestra dell'applicazione in modo che corrisponda all'impostazione del controllo visualizzata in Sndvol.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-121">During this call, the **OnNotify** method can update the endpoint volume control in the application window to match the control setting shown in Sndvol.</span></span> <span data-ttu-id="8fbdd-122">Analogamente, ogni volta che l'utente modifica il livello del volume dell'endpoint tramite il controllo del volume nella finestra dell'applicazione, Sndvol riceve una notifica e aggiorna immediatamente il controllo del volume dell'endpoint per visualizzare il nuovo livello di volume.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-122">Similarly, each time the user changes the endpoint volume level through volume control in the application window, Sndvol receives a notification and immediately updates its endpoint volume control to display the new volume level.</span></span>

<span data-ttu-id="8fbdd-123">L'esempio di codice seguente è un file di intestazione che illustra una possibile implementazione [**dell'interfaccia IAudioEndpointVolumeCallback:**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-123">The following code example is a header file that shows a possible implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface:</span></span>


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



<span data-ttu-id="8fbdd-124">La classe CAudioEndpointVolumeCallback nell'esempio di codice precedente è un'implementazione [**dell'interfaccia IAudioEndpointVolumeCallback.**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-124">The CAudioEndpointVolumeCallback class in the preceding code example is an implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface.</span></span> <span data-ttu-id="8fbdd-125">Poiché **IAudioEndpointVolumeCallback** eredita da [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)la definizione della classe contiene le implementazioni dei metodi **IUnknown** [**AddRef,**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)e [**QueryInterface.**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="8fbdd-125">Because **IAudioEndpointVolumeCallback** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="8fbdd-126">Il [**metodo OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) nella definizione della classe viene chiamato ogni volta che uno dei metodi seguenti modifica il livello del volume dell'endpoint:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-126">The [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the class definition is called each time one of the following methods changes the endpoint volume level:</span></span>

-   [<span data-ttu-id="8fbdd-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="8fbdd-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [<span data-ttu-id="8fbdd-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span><span class="sxs-lookup"><span data-stu-id="8fbdd-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [<span data-ttu-id="8fbdd-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="8fbdd-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [<span data-ttu-id="8fbdd-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span><span class="sxs-lookup"><span data-stu-id="8fbdd-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [<span data-ttu-id="8fbdd-131">**IAudioEndpointVolume::SetMute**</span><span class="sxs-lookup"><span data-stu-id="8fbdd-131">**IAudioEndpointVolume::SetMute**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [<span data-ttu-id="8fbdd-132">**IAudioEndpointVolume::VolumeStepDown**</span><span class="sxs-lookup"><span data-stu-id="8fbdd-132">**IAudioEndpointVolume::VolumeStepDown**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [<span data-ttu-id="8fbdd-133">**IAudioEndpointVolume::VolumeStepUp**</span><span class="sxs-lookup"><span data-stu-id="8fbdd-133">**IAudioEndpointVolume::VolumeStepUp**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

<span data-ttu-id="8fbdd-134">L'implementazione [**del metodo OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) nell'esempio di codice precedente invia messaggi al controllo del volume nella finestra dell'applicazione per aggiornare il livello di volume visualizzato.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-134">The implementation of the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the preceding code example sends messages to the volume control in the application window to update the displayed volume level.</span></span>

<span data-ttu-id="8fbdd-135">Un'applicazione chiama il metodo [**IAudioEndpointVolume::RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) per registrare [**l'interfaccia IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) per ricevere le notifiche.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-135">An application calls the [**IAudioEndpointVolume::RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) method to register its [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface to receive notifications.</span></span> <span data-ttu-id="8fbdd-136">Quando l'applicazione non richiede più notifiche, chiama il metodo [**IAudioEndpointVolume::UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) per eliminare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-136">When the application no longer requires notifications, it calls the [**IAudioEndpointVolume::UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) method to delete the registration.</span></span>

<span data-ttu-id="8fbdd-137">L'esempio di codice seguente è un'applicazione Windows che chiama i metodi [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) e [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) per registrare e annullare la registrazione della classe CAudioEndpointVolumeCallback nell'esempio di codice precedente:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-137">The following code example is a Windows application that calls the [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) and [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) methods to register and unregister the CAudioEndpointVolumeCallback class in the preceding code example:</span></span>


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
    if (g_pEndptVol != NULL)
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



<span data-ttu-id="8fbdd-138">Nell'esempio di codice precedente la funzione [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) chiama la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza dell'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) e chiama il metodo [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo di rendering predefinito.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-138">In the preceding code example, the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="8fbdd-139">**WinMain** chiama il [**metodo IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per ottenere l'interfaccia [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) del dispositivo e [**chiama RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) per registrare l'applicazione per ricevere notifiche delle modifiche al volume dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-139">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface, and it calls [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) to register the application to receive notifications of endpoint volume changes.</span></span> <span data-ttu-id="8fbdd-140">WinMain **apre quindi** una finestra di dialogo per visualizzare un controllo del volume dell'endpoint per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-140">Next, **WinMain** opens a dialog box to display an endpoint volume control for the device.</span></span> <span data-ttu-id="8fbdd-141">Nella finestra di dialogo viene inoltre visualizzata una casella di controllo che indica se il dispositivo è disattivato.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-141">The dialog box also displays a check box that indicates whether the device is muted.</span></span> <span data-ttu-id="8fbdd-142">La casella di controllo Controllo volume endpoint e disattiva audio nella finestra di dialogo rispecchia le impostazioni della casella di controllo Controllo volume endpoint e disattiva audio visualizzata da Sndvol.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-142">The endpoint volume control and mute check box in the dialog box mirror the settings of the endpoint volume control and mute check box displayed by Sndvol.</span></span> <span data-ttu-id="8fbdd-143">Per altre informazioni su **WinMain** e **CoCreateInstance,** vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-143">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="8fbdd-144">Per altre informazioni su **IMMDeviceEnumerator** e **IMMDevice**, vedere [Enumerazione di dispositivi audio.](enumerating-audio-devices.md)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-144">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="8fbdd-145">La routine della finestra di dialogo, DlgProc, nell'esempio di codice precedente, gestisce le modifiche apportate dall'utente al volume e disattiva le impostazioni tramite i controlli nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-145">The dialog box procedure, DlgProc, in the preceding code example, handles the changes that the user makes to the volume and mute settings through the controls in the dialog box.</span></span> <span data-ttu-id="8fbdd-146">Quando DlgProc chiama [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) o [**SetMute,**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)Sndvol riceve la notifica della modifica e aggiorna il controllo corrispondente nella relativa finestra per riflettere il nuovo volume o l'impostazione di disattivazione.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-146">When DlgProc calls [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) or [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), Sndvol receives notification of the change and updates the corresponding control in its window to reflect the new volume or mute setting.</span></span> <span data-ttu-id="8fbdd-147">Se, invece di usare la finestra di dialogo, l'utente aggiorna le impostazioni del volume e dell'audio tramite i controlli nella finestra Sndvol, il metodo [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) nella classe CAudioEndpointVolumeCallback aggiorna i controlli nella finestra di dialogo per visualizzare le nuove impostazioni.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-147">If, instead of using the dialog box, the user updates the volume and mute settings through the controls in the Sndvol window, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class updates the controls in the dialog box to display the new settings.</span></span>

<span data-ttu-id="8fbdd-148">Se l'utente modifica il volume tramite i controlli nella finestra di dialogo, il metodo [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) nella classe CAudioEndpointVolumeCallback non invia messaggi per aggiornare i controlli nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-148">If the user changes the volume through the controls in the dialog box, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class does not send messages to update the controls in the dialog box.</span></span> <span data-ttu-id="8fbdd-149">A tale scopo sarebbe ridondante.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-149">To do so would be redundant.</span></span> <span data-ttu-id="8fbdd-150">**OnNotify** aggiorna i controlli nella finestra di dialogo solo se la modifica del volume ha avuto origine in Sndvol o in un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-150">**OnNotify** updates the controls in the dialog box only if the volume change originated in Sndvol or in some other application.</span></span> <span data-ttu-id="8fbdd-151">Il secondo parametro nelle chiamate ai metodi [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) e [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) nella funzione DlgProc è un puntatore a un GUID del contesto dell'evento che uno dei due metodi passa a **OnNotify.**</span><span class="sxs-lookup"><span data-stu-id="8fbdd-151">The second parameter in the [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) and [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) method calls in the DlgProc function is a pointer to an event-context GUID that either method passes to **OnNotify**.</span></span> <span data-ttu-id="8fbdd-152">**OnNotify** controlla il valore del GUID del contesto dell'evento per determinare se la finestra di dialogo è l'origine della modifica del volume.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-152">**OnNotify** checks the value of the event-context GUID to determine whether the dialog box is the source of the volume change.</span></span> <span data-ttu-id="8fbdd-153">Per altre informazioni sui GUID del contesto dell'evento, vedere **IAudioEndpointVolumeCallback::OnNotify.**</span><span class="sxs-lookup"><span data-stu-id="8fbdd-153">For more information about event-context GUIDs, see **IAudioEndpointVolumeCallback::OnNotify**.</span></span>

<span data-ttu-id="8fbdd-154">Quando l'utente esce dalla finestra di dialogo, la chiamata [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) nell'esempio di codice precedente elimina la registrazione della classe CAudioEndpointVolumeCallback prima che il programma termini.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-154">When the user exits the dialog box, the [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) call in the preceding code example deletes the registration of the CAudioEndpointVolumeCallback class before the program terminates.</span></span>

<span data-ttu-id="8fbdd-155">È possibile modificare facilmente l'esempio di codice precedente per visualizzare i controlli volume e mute per il dispositivo di acquisizione predefinito.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-155">You can easily modify the preceding code example to display volume and mute controls for the default capture device.</span></span> <span data-ttu-id="8fbdd-156">Nella funzione [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) modificare il valore del primo parametro nella chiamata al metodo [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) da eRender a eCapture.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-156">In the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method from eRender to eCapture.</span></span>

<span data-ttu-id="8fbdd-157">L'esempio di codice seguente è lo script di risorsa che definisce i controlli volume e mute visualizzati nell'esempio di codice precedente:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-157">The following code example is the resource script that defines the volume and mute controls that appear in the preceding code example:</span></span>


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



<span data-ttu-id="8fbdd-158">L'esempio di codice seguente è il file di intestazione delle risorse che definisce gli identificatori di controllo visualizzati negli esempi di codice precedenti:</span><span class="sxs-lookup"><span data-stu-id="8fbdd-158">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



<span data-ttu-id="8fbdd-159">Gli esempi di codice precedenti si combinano per formare una semplice applicazione per il controllo e il monitoraggio del volume degli endpoint del dispositivo di rendering predefinito.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-159">The preceding code examples combine to form a simple application for controlling and monitoring the endpoint volume of the default rendering device.</span></span> <span data-ttu-id="8fbdd-160">Un'applicazione più utile potrebbe inoltre notificare all'utente quando lo stato del dispositivo cambia.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-160">A more useful application might additionally notify the user when the status of the device changes.</span></span> <span data-ttu-id="8fbdd-161">Ad esempio, il dispositivo potrebbe essere disabilitato, scollegato o rimosso.</span><span class="sxs-lookup"><span data-stu-id="8fbdd-161">For example, the device might be disabled, unplugged, or removed.</span></span> <span data-ttu-id="8fbdd-162">Per altre informazioni sul monitoraggio di questi tipi di eventi, vedere [Eventi del dispositivo.](device-events.md)</span><span class="sxs-lookup"><span data-stu-id="8fbdd-162">For more information about monitoring these types of events, see [Device Events](device-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fbdd-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8fbdd-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fbdd-164">Controlli del volume</span><span class="sxs-lookup"><span data-stu-id="8fbdd-164">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
