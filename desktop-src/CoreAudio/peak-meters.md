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
# <a name="peak-meters"></a>Contatori di picco

Per supportare le applicazioni Windows che visualizzano i contatori di picco, l' [API EndpointVolume](endpointvolume-api.md) include un'interfaccia [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) . Questa interfaccia rappresenta un contatore massimo in un [dispositivo endpoint audio](audio-endpoint-devices.md). Per un dispositivo di rendering, il valore recuperato dal contatore di picco rappresenta il valore massimo di campione rilevato nel flusso di output al dispositivo durante il periodo di misurazione precedente. Per un dispositivo di acquisizione, il valore recuperato dal contatore di picco rappresenta il valore massimo di campione rilevato nel flusso di input dal dispositivo.

I valori di picco ottenuti dai metodi nell'interfaccia [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) sono numeri a virgola mobile nell'intervallo normalizzato compreso tra 0,0 e 1,0. Se, ad esempio, un flusso PCM contiene campioni a 16 bit e il valore di picco di esempio durante un determinato periodo di misurazione è-8914, il valore assoluto registrato dal contatore di picco è 8914 e il valore di picco normalizzato segnalato dall'interfaccia **IAudioMeterInformation** è 8914/32768 = 0,272.

Se il dispositivo endpoint audio implementa il contatore di picco nell'hardware, l'interfaccia [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) usa il contatore hardware di picco. In caso contrario, l'interfaccia implementa il contatore massimo nel software.

Se un dispositivo ha un indicatore di picco hardware, il contatore di picco è attivo sia in modalità condivisa che in modalità esclusiva. Se un dispositivo non dispone di un indicatore di picco hardware, il contatore di picco è attivo in modalità condivisa, ma non in modalità esclusiva. In modalità esclusiva, l'applicazione e l'hardware audio scambiano direttamente i dati audio, ignorando il contatore di picco software (che segnala sempre un valore di picco di 0,0).

Il seguente esempio di codice C++ è un'applicazione Windows che visualizza un contatore massimo per il dispositivo di rendering predefinito:


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



Nell'esempio di codice precedente, la funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) chiama la [**funzione CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un'istanza dell'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) e chiama il metodo [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) per ottenere l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo di rendering predefinito. **WinMain** chiama il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) per ottenere l'interfaccia [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) del dispositivo e apre una finestra di dialogo per visualizzare un contatore di picco per il dispositivo. Per ulteriori informazioni su **WinMain** e **CoCreateInstance**, vedere la documentazione di Windows SDK. Per ulteriori informazioni su **IMMDeviceEnumerator** e **IMMDevice**, vedere [enumerazione di dispositivi audio](enumerating-audio-devices.md).

Nell'esempio di codice precedente, la funzione DlgProc Visualizza il contatore massimo nella finestra di dialogo. Durante l'elaborazione del \_ messaggio WM INITDIALOG, DlgProc chiama la funzione [**setimer**](/windows/win32/api/winuser/nf-winuser-settimer) per impostare un timer che genererà messaggi del \_ timer WM a intervalli di tempo regolari. Quando DlgProc riceve un \_ messaggio del timer WM, chiama [**IAudioMeterInformation:: GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) per ottenere la lettura più recente del contatore di picco per il flusso. DlgProc chiama quindi la funzione DrawPeakMeter per estrarre il contatore massimo aggiornato nella finestra di dialogo. Per ulteriori **informazioni su INITDIALOG e sui** messaggi del \_ timer WM e WM \_ , vedere la documentazione Windows SDK.

È possibile modificare facilmente l'esempio di codice precedente per visualizzare un contatore di picco per il dispositivo di acquisizione predefinito. Nella funzione [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) , modificare il valore del primo parametro nella chiamata a [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) da eRender a eCapture.

L'esempio di codice seguente è lo script di risorsa che definisce i controlli che vengono visualizzati nell'esempio di codice precedente:


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



L'esempio di codice seguente è il file di intestazione della risorsa che definisce gli identificatori di controllo visualizzati negli esempi di codice precedenti:


```C++
// Resource.h -- Control identifiers

#define IDC_STATIC_MINVOL      1001
#define IDC_STATIC_MAXVOL      1002
#define IDC_PEAK_METER         1003
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli del volume](volume-controls.md)
</dt> </dl>

 

 
