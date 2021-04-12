---
title: Creazione di grafici di filtro in applicazioni DRM-Enabled
description: Creazione di grafici di filtro in applicazioni DRM-Enabled
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows Media Format SDK, creazione di grafici di filtro
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, applicazioni abilitate per DRM
- ASF (Advanced Systems Format), creazione di grafici di filtro
- ASF (Advanced Systems Format), compilazione di grafici di filtro
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), applicazioni abilitate per DRM
- ASF (Advanced Systems Format), applicazioni abilitate per DRM
- DirectShow, creazione di grafici di filtro
- DirectShow, applicazioni abilitate per DRM
- Digital Rights Management (DRM), DirectShow
- DRM (Digital Rights Management), DirectShow
- Digital Rights Management (DRM), creazione di grafici di filtro
- DRM (Digital Rights Management), compilazione di grafici di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944037a00c208e1427d3d19aa6c9dc0a352ec5fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336402"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a>Creazione di grafici di filtro in applicazioni DRM-Enabled

Se l'applicazione DirectShow supporta la riproduzione di file protetti da DRM, in genere non è consigliabile usare **RenderFile** per creare il grafico dei filtri perché non è possibile specificare i diritti DRM richiesti prima dell'apertura del file. Per impostazione predefinita, il lettore WM ASF richiede solo i diritti di riproduzione. Il filtro non viene aggiunto al grafo e pertanto non è individuabile dalle applicazioni, fino a quando un file non viene aperto correttamente.

Per creare un grafico di riproduzione abilitato per DRM usando il [lettore WM ASF](wm-asf-reader-filter.md), è necessario creare un'istanza del filtro usando **CoCreateInstance**, aggiungerlo al grafo del filtro usando **IGraphBuilder:: AddFilter**, configurarlo e quindi eseguire il rendering dei pin di output. Questa tecnica è illustrata nell'esempio PlayWndASF. Quando si compila il grafico in questo modo, è già presente il puntatore **IBaseFilter** che può essere usato per chiamare **QueryService** per ottenere **IWMDRMWriter**. Questa interfaccia non è tuttavia disponibile fino a quando l'oggetto Reader di Windows Media Format SDK non viene creato internamente dal lettore WM ASF. La prima opportunità per l'applicazione di impostare i diritti DRM è nel \_ \_ gestore eventi WMT no Rights \_ , come illustrato nel frammento di codice seguente:


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Elenco attributi DRM**](drm-attribute-list.md)
</dt> <dt>

[**Proprietà DRM**](drm-properties.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




