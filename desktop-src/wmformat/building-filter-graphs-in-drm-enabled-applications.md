---
title: Compilazione di grafi di filtro in DRM-Enabled applicazioni
description: Compilazione di grafi di filtro in DRM-Enabled applicazioni
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows Media Format SDK, creazione di grafi di filtro
- Windows Media Format SDK,DirectShow
- Windows Media Format SDK, applicazioni abilitate per DRM
- Advanced Systems Format (ASF), creazione di grafici dei filtri
- ASF (Advanced Systems Format), creazione di grafici dei filtri
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), applicazioni abilitate per DRM
- ASF (Advanced Systems Format), applicazioni abilitate per DRM
- DirectShow,creazione di grafici dei filtri
- DirectShow, applicazioni abilitate per DRM
- DRM (Digital Rights Management), DirectShow
- DRM (Digital Rights Management),DirectShow
- digital rights management (DRM), creazione di grafici dei filtri
- DRM (Digital Rights Management),creazione di grafici dei filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e7f411a52c0ce7c42410c7a901787c7f6d9d7089921019639cb3f5e708dff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447951"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a>Compilazione di grafi di filtro in DRM-Enabled applicazioni

Se l'applicazione DirectShow supporta la riproduzione di file protetti da DRM, in genere non è consigliabile usare **RenderFile** per creare il grafo dei filtri perché non è possibile specificare i diritti DRM necessari prima dell'apertura del file. Il lettore ASF WM per impostazione predefinita richiede solo i diritti di riproduzione. Il filtro non viene aggiunto al grafico e pertanto non è individuabile dalle applicazioni finché un file non viene aperto correttamente.

Per compilare un grafico di riproduzione abilitato per DRM usando il lettore [ASF WM,](wm-asf-reader-filter.md)è necessario creare un'istanza del filtro usando **CoCreateInstance,** aggiungerlo al grafico dei filtri **usando IGraphBuilder::AddFilter,** configurarlo e quindi eseguire il rendering dei pin di output. Questa tecnica è illustrata nell'esempio PlayWndASF. Quando si compila il grafo in questo modo, si dispone già del puntatore **IBaseFilter** che può essere usato per chiamare **QueryService** per ottenere **IWMDRMWriter.** Tuttavia, questa interfaccia non è disponibile fino a quando l'Windows lettore di Media Format SDK non viene creato internamente dal lettore ASF WM. La prima opportunità che l'applicazione ha di impostare i diritti DRM è nel gestore eventi WMT \_ NO \_ RIGHTS \_ EX, come illustrato in questo frammento di codice:


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

[**Funzionalità Rights Management digital**](digital-rights-management-features.md)
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

 

 




