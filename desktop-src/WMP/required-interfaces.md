---
title: Interfacce necessarie (Windows Media Player SDK)
description: Informazioni sulle interfacce necessarie che Windows Media Player implementano in DirectShow o Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Windows Media Player plug-in, interfacce
- plug-in, interfacce
- plug-in per l'elaborazione di segnali digitali, interfacce
- plug-in DSP, interfacce
- interfacce, plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a3552cbe741b3b527c899e5bb7d68fe4d7c4e0bdc61203f822c57111e94a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646831"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Interfacce necessarie (Windows Media Player SDK)

Windows Media Player esegue il rendering di audio e video usando una delle pipeline seguenti.

-   DirectShow
-   Media Foundation

In Microsoft Windows XP e versioni precedenti, Player usa DirectShow. In Windows Vista, Il lettore a volte usa DirectShow e talvolta usa Media Foundation.

Un plug-in DSP implementa alcune o tutte le interfacce seguenti:

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **IMFTransform**
-   **IMFGetService**
-   **ISpecifyPropertyPages**

Un plug-in che implementa **IMediaObject** e **IWMPPluginEnable** può essere eseguito nella DirectShow pipeline. Può anche essere eseguito nella pipeline Media Foundation all'interno di un wrapper fornito da Media Foundation. Un plug-in di questo tipo è denominato Microsoft DirectX Media Object (DMO). È comune pensare che un DMO sia analogo a un oggetto filtro in DirectShow. La DMO documentazione è disponibile nella DirectShow di Windows SDK.

Un plug-in che implementa **IMFTransform** e **IMFGetService** può essere eseguito in modo nativo (non è necessario alcun wrapper) nella pipeline Media Foundation. Un plug-in di questo tipo è denominato Media Foundation Transform (MFT). La documentazione di MFT è disponibile nella Media Foundation di Windows SDK.

Un plug-in che implementa **IMediaObject,** **IWMPPluginEnable,** **IMFTransform** e **IMFGetService** può essere eseguito nella pipeline di DirectShow e può anche essere eseguito in modo nativo nella pipeline Media Foundation. Questo tipo di plug-in, denominato *plug-in DSP* a doppia modalità, può svolgere il ruolo di un DMO o di un MFT.

Quando Windows Media Player usa un plug-in DSP in modalità doppia nella pipeline Media Foundation, esegue prima una query per **l'interfaccia IMFTransform.** Se la query ha esito negativo, Windows Media Player query per **l'interfaccia IMediaObject.** Se la query **IMediaObject** ha esito positivo, il plug-in viene incapsulato e aggiunto alla Media Foundation pipeline.

Indipendentemente dalla pipeline, qualsiasi plug-in DSP che consente all'utente di impostare le proprietà deve implementare **ISpecifyPropertyPages**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica degli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Interfacce plug-in DSP**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**Creazione di pacchetti plug-in DSP**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




