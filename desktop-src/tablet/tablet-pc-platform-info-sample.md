---
description: Questo programma controlla la presenza e la configurazione dei componenti MicrosoftTablet PC e Touch Technology core.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Esempio di informazioni sulla piattaforma Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d815f21233b1edcc90d456df68b3736c170a5fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317902"
---
# <a name="tablet-pc-platform-info-sample"></a>Esempio di informazioni sulla piattaforma Tablet PC

Questo programma controlla la presenza e la configurazione dei componenti MicrosoftTablet PC e Touch Technology core. Determina se i componenti tablet PC sono abilitati nel sistema operativo, elencando i nomi e le informazioni sulla versione per i controlli di base e il riconoscimento vocale e della grafia predefiniti.

L'applicazione usa l'API Windows GetSystemMetrics, passando in SM \_ TABLETPC, per determinare se l'applicazione è in esecuzione in un Tablet PC. Il \_ TABLETPC SM è definito in winuser. h.

Di particolare interesse è il modo in cui l'applicazione usa la raccolta Recognizers per fornire informazioni sul riconoscimento predefinito. Prima di provare a usare la raccolta Recognizers e l'oggetto Recognizer, l'applicazione verifica la corretta creazione.

## <a name="components"></a>Componenti

Utilizzando il modulo merge ridistribuibile, è possibile che alcune parti dell'API della piattaforma Tablet PC siano installate in versioni non Tablet di vista e Windows XP Professional. La chiamata GetSystemMetrics indica solo che è installato Windows XP Tablet PC Edition. Un'applicazione deve sempre determinare se è disponibile un determinato componente. Il modo corretto per determinare se un componente dell'API è installato consiste nel tentare di creare un'istanza di un oggetto o di un controllo e verificare che esista prima di provare a usarlo, come illustrato nell'esempio seguente.


```C++
IInkRecognizers* pIInkRecognizers = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkRecognizers,
                              NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IInkRecognizers, 
                              (void **)&pIInkRecognizers);
if (SUCCEEDED(hr)) 
{
  // use the component
} else
{
  // component unavailable
}
```



L'applicazione individua i componenti vocali installati esaminando la chiave del registro di sistema appropriata:


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



La chiave viene letta usando RegQueryValueExW.

Infine, nell'esempio vengono individuati i controlli installati.


```C++
LPCOLESTR gc_wszProgId[NUM_CONTROLS] = {L"InkEd.InkEdit", L"msinkaut.InkOverlay"};
// ...
for (int i = 0, j = 0; i < NUM_CONTROLS; i++)
{
    // Get the component info
    CLSID clsid;
    if (SUCCEEDED(CLSIDFromProgID(gc_wszProgId[i], &clsid)) && GetComponentInfo(clsid, info) == TRUE)
    {
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][0], info.wchName);
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][1], info.wchVersion);
        j++;
    }
}
```



 

 



