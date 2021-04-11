---
description: Contatori di picco
ms.assetid: 02f5d1b4-ba4f-424a-897f-b113d1f7cd6b
title: Contatori di picco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccd2f1ce0b8fd45fbf1cb3710c878c05544f7d4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127094"
---
# <a name="peak-meters"></a><span data-ttu-id="2245a-103">Contatori di picco</span><span class="sxs-lookup"><span data-stu-id="2245a-103">Peak Meters</span></span>

<span data-ttu-id="2245a-104">Per supportare le applicazioni Windows che visualizzano i contatori di picco, l' [API EndpointVolume](endpointvolume-api.md) include un'interfaccia [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) .</span><span class="sxs-lookup"><span data-stu-id="2245a-104">To support Windows applications that display peak meters, the [EndpointVolume API](endpointvolume-api.md) includes an [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface.</span></span> <span data-ttu-id="2245a-105">Questa interfaccia rappresenta un contatore massimo in un [dispositivo endpoint audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2245a-105">This interface represents a peak meter on an [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="2245a-106">Per un dispositivo di rendering, il valore recuperato dal contatore di picco rappresenta il valore massimo di campione rilevato nel flusso di output al dispositivo durante il periodo di misurazione precedente.</span><span class="sxs-lookup"><span data-stu-id="2245a-106">For a rendering device, the value retrieved from the peak meter represents the maximum sample value encountered in the output stream to the device during the preceding metering period.</span></span> <span data-ttu-id="2245a-107">Per un dispositivo di acquisizione, il valore recuperato dal contatore di picco rappresenta il valore massimo di campione rilevato nel flusso di input dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2245a-107">For a capture device, the value retrieved from the peak meter represents the maximum sample value encountered in the input stream from the device.</span></span>

<span data-ttu-id="2245a-108">I valori di picco ottenuti dai metodi nell'interfaccia [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) sono numeri a virgola mobile nell'intervallo normalizzato compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="2245a-108">The peak-meter values obtained from the methods in the [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface are floating-point numbers in the normalized range from 0.0 to 1.0.</span></span> <span data-ttu-id="2245a-109">Se, ad esempio, un flusso PCM contiene campioni a 16 bit e il valore di picco di esempio durante un determinato periodo di misurazione è-8914, il valore assoluto registrato dal contatore di picco è 8914 e il valore di picco normalizzato segnalato dall'interfaccia **IAudioMeterInformation** è 8914/32768 = 0,272.</span><span class="sxs-lookup"><span data-stu-id="2245a-109">For example, if a PCM stream contains 16-bit samples, and the peak sample value during a particular metering period is —8914, then the absolute value recorded by the peak meter is 8914, and the normalized peak value reported by the **IAudioMeterInformation** interface is 8914/32768 = 0.272.</span></span>

<span data-ttu-id="2245a-110">Se il dispositivo endpoint audio implementa il contatore di picco nell'hardware, l'interfaccia [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) usa il contatore hardware di picco.</span><span class="sxs-lookup"><span data-stu-id="2245a-110">If the audio endpoint device implements the peak meter in hardware, the [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface uses the hardware peak meter.</span></span> <span data-ttu-id="2245a-111">In caso contrario, l'interfaccia implementa il contatore massimo nel software.</span><span class="sxs-lookup"><span data-stu-id="2245a-111">Otherwise, the interface implements the peak meter in software.</span></span>

<span data-ttu-id="2245a-112">Se un dispositivo ha un indicatore di picco hardware, il contatore di picco è attivo sia in modalità condivisa che in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="2245a-112">If a device has a hardware peak meter, the peak meter is active both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="2245a-113">Se un dispositivo non dispone di un indicatore di picco hardware, il contatore di picco è attivo in modalità condivisa, ma non in modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="2245a-113">If a device lacks hardware peak meter, the peak meter is active in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="2245a-114">In modalità esclusiva, l'applicazione e l'hardware audio scambiano direttamente i dati audio, ignorando il contatore di picco software (che segnala sempre un valore di picco di 0,0).</span><span class="sxs-lookup"><span data-stu-id="2245a-114">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software peak meter (which always reports a peak value of 0.0).</span></span>

<span data-ttu-id="2245a-115">Il seguente esempio di codice C++ è un'applicazione Windows che visualizza un contatore massimo per il dispositivo di rendering predefinito:</span><span class="sxs-lookup"><span data-stu-id="2245a-115">The following C++ code example is a Windows application that displays a peak meter for the default rendering device:</span></span>


```C++
// Peakmeter.cpp -- WinMain and dialog box functions

#include <windows.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);
static void DrawPeakMeter(HWND, float);

// Timer ID and period (in milliseconds)
#define ID_TIMER  1
#define TIMER_PERIOD  125

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// WinMain -- Opens a dialog box that contains a peak meter.
//   The peak meter displays the peak sample value that plays
//   through the default rendering device.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioMeterInformation *pMeterInfo = NULL;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get peak meter for default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioMeterInformation),
                           CLSCTX_ALL, NULL, (void**)&pMeterInfo);
    EXIT_ON_ERROR(hr)

    DialogBoxParam(hInstance, L"PEAKMETER", NULL, (DLGPROC)DlgProc, (LPARAM)pMeterInfo);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pMeterInfo)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    static IAudioMeterInformation *pMeterInfo = NULL;
    static HWND hPeakMeter = NULL;
    static float peak = 0;
    HRESULT hr;

    switch (message)
    {
    case WM_INITDIALOG:
        pMeterInfo = (IAudioMeterInformation*)lParam;
        SetTimer(hDlg, ID_TIMER, TIMER_PERIOD, NULL);
        hPeakMeter = GetDlgItem(hDlg, IDC_PEAK_METER);
        return TRUE;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDCANCEL:
            KillTimer(hDlg, ID_TIMER);
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;

    case WM_TIMER:
        switch ((int)wParam)
        {
        case ID_TIMER:
            // Update the peak meter in the dialog box.
            hr = pMeterInfo->GetPeakValue(&peak);
            if (FAILED(hr))
            {
                MessageBox(hDlg, TEXT("The program will exit."),
                           TEXT("Fatal error"), MB_OK);
                KillTimer(hDlg, ID_TIMER);
                EndDialog(hDlg, TRUE);
                return TRUE;
            }
            DrawPeakMeter(hPeakMeter, peak);
            return TRUE;
        }
        break;

    case WM_PAINT:
        // Redraw the peak meter in the dialog box.
        ValidateRect(hPeakMeter, NULL);
        DrawPeakMeter(hPeakMeter, peak);
        break;
    }
    return FALSE;
}

//-----------------------------------------------------------
// DrawPeakMeter -- Draws the peak meter in the dialog box.
//-----------------------------------------------------------

void DrawPeakMeter(HWND hPeakMeter, float peak)
{
    HDC hdc;
    RECT rect;

    GetClientRect(hPeakMeter, &rect);
    hdc = GetDC(hPeakMeter);
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DSHADOW+1));
    rect.left++;
    rect.top++;
    rect.right = rect.left +
                 max(0, (LONG)(peak*(rect.right-rect.left)-1.5));
    rect.bottom--;
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DHIGHLIGHT+1));
    ReleaseDC(hPeakMeter, hdc);
}
```



<span data-ttu-id="2245a-116">Nell'esempio di codice precedente, la funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) chiama la [**funzione CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza dell'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) e chiama il metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo di rendering predefinito.</span><span class="sxs-lookup"><span data-stu-id="2245a-116">In the preceding code example, the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="2245a-117">**WinMain** chiama il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per ottenere l'interfaccia [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) del dispositivo e apre una finestra di dialogo per visualizzare un contatore di picco per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2245a-117">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface, and it opens a dialog box to display a peak meter for the device.</span></span> <span data-ttu-id="2245a-118">Per ulteriori informazioni su **WinMain** e **CoCreateInstance**, vedere la documentazione di Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2245a-118">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="2245a-119">Per ulteriori informazioni su **IMMDeviceEnumerator** e **IMMDevice**, vedere [enumerazione di dispositivi audio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2245a-119">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="2245a-120">Nell'esempio di codice precedente, la funzione DlgProc Visualizza il contatore massimo nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2245a-120">In the preceding code example, the DlgProc function displays the peak meter in the dialog box.</span></span> <span data-ttu-id="2245a-121">Durante l'elaborazione del \_ messaggio WM INITDIALOG, DlgProc chiama la funzione [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer) per impostare un timer che genererà messaggi del \_ timer WM a intervalli di tempo regolari.</span><span class="sxs-lookup"><span data-stu-id="2245a-121">During processing of the WM\_INITDIALOG message, DlgProc calls the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function to set up a timer that will generate WM\_TIMER messages at regular time intervals.</span></span> <span data-ttu-id="2245a-122">Quando DlgProc riceve un \_ messaggio del timer WM, chiama [**IAudioMeterInformation:: GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) per ottenere la lettura più recente del contatore di picco per il flusso.</span><span class="sxs-lookup"><span data-stu-id="2245a-122">When DlgProc receives a WM\_TIMER message, it calls [**IAudioMeterInformation::GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) to obtain the latest peak-meter reading for the stream.</span></span> <span data-ttu-id="2245a-123">DlgProc chiama quindi la funzione DrawPeakMeter per estrarre il contatore massimo aggiornato nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="2245a-123">DlgProc then calls the DrawPeakMeter function to draw the updated peak meter in the dialog box.</span></span> <span data-ttu-id="2245a-124">Per ulteriori **informazioni su INITDIALOG e sui** messaggi del \_ timer WM e WM \_ , vedere la documentazione Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2245a-124">For more information about **SetTimer** and the WM\_INITDIALOG and WM\_TIMER messages, see the Windows SDK documentation.</span></span>

<span data-ttu-id="2245a-125">È possibile modificare facilmente l'esempio di codice precedente per visualizzare un contatore di picco per il dispositivo di acquisizione predefinito.</span><span class="sxs-lookup"><span data-stu-id="2245a-125">You can easily modify the preceding code example to display a peak meter for the default capture device.</span></span> <span data-ttu-id="2245a-126">Nella funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) , modificare il valore del primo parametro nella chiamata a [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) da eRender a eCapture.</span><span class="sxs-lookup"><span data-stu-id="2245a-126">In the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) from eRender to eCapture.</span></span>

<span data-ttu-id="2245a-127">L'esempio di codice seguente è lo script di risorsa che definisce i controlli che vengono visualizzati nell'esempio di codice precedente:</span><span class="sxs-lookup"><span data-stu-id="2245a-127">The following code example is the resource script that defines the controls that appear in the preceding code example:</span></span>


```C++
// Peakmeter.rc -- Resource script

#include "resource.h"
#include "windows.h"

//
// Dialog
//
PEAKMETER DIALOGEX 0, 0, 150, 34
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Peak Meter"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    CTEXT      "",IDC_PEAK_METER,34,14,82,5
    LTEXT      "Min",IDC_STATIC_MINVOL,10,12,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,120,12,20,12
END
```



<span data-ttu-id="2245a-128">L'esempio di codice seguente è il file di intestazione della risorsa che definisce gli identificatori di controllo visualizzati negli esempi di codice precedenti:</span><span class="sxs-lookup"><span data-stu-id="2245a-128">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers

#define IDC_STATIC_MINVOL      1001
#define IDC_STATIC_MAXVOL      1002
#define IDC_PEAK_METER         1003
```



## <a name="related-topics"></a><span data-ttu-id="2245a-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2245a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2245a-130">Controlli del volume</span><span class="sxs-lookup"><span data-stu-id="2245a-130">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
