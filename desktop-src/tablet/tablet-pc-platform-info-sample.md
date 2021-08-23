---
description: Questo programma controlla la presenza e la configurazione dei componenti principali di MicrosoftTablet PC e Touch Technology.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Esempio di informazioni sulla piattaforma Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1731fc30e0405b2702bb45d0a9d0556b861ad09994ac683d739da33afe018088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819982"
---
# <a name="tablet-pc-platform-info-sample"></a>Esempio di informazioni sulla piattaforma Tablet PC

Questo programma controlla la presenza e la configurazione dei componenti principali di MicrosoftTablet PC e Touch Technology. Determina se i componenti Tablet PC sono abilitati nel sistema operativo, elencando i nomi e le informazioni sulla versione per i controlli di base e il riconoscimento grafia e riconoscimento vocale predefinito.

L'applicazione usa l'API Windows GetSystemMetrics, passando SM TABLETPC, per determinare se l'applicazione è in \_ esecuzione in un Tablet PC. SM \_ TABLETPC è definito in WinUser.h.

Di particolare interesse è il modo in cui l'applicazione usa la raccolta Recognizers per fornire informazioni sul sistema di riconoscimento predefinito. Prima di provare a usare la raccolta Recognizers e l'oggetto Recognizer, l'applicazione verifica la corretta creazione.

## <a name="components"></a>Componenti

Usando il modulo unione ridistribuibile, alcune parti dell'API Tablet PC Platform possono essere installate in versioni non Tablet di Vista e Windows XP Professional . La chiamata GetSystemMetrics indica solo che è installato Windows XP Tablet PC Edition. Un'applicazione deve sempre determinare se un determinato componente è disponibile. Il modo corretto per determinare se un componente dell'API è installato è tentare di creare un'istanza di un oggetto o di un controllo e verificarne l'esistenza prima di tentare di usarlo, come illustrato nell'esempio seguente.


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



L'applicazione rileva i componenti voce installati esaminando la chiave del Registro di sistema appropriata:


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



 

 



