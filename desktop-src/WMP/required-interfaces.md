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
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406094"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Interfacce necessarie (Windows Media Player SDK)

Windows Media Player esegue il rendering di audio e video usando una delle pipeline seguenti.

-   Directshow
-   Media Foundation

In Microsoft Windows XP e versioni precedenti, Player usa DirectShow. In Windows Vista, Il lettore usa a volte DirectShow e talvolta usa Media Foundation.

Un plug-in DSP implementa alcune o tutte le interfacce seguenti:

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **IMFTransform**
-   **IMFGetService**
-   **ISpecifyPropertyPages**

Un plug-in che implementa **IMediaObject** e **IWMPPluginEnable** può essere eseguito nella pipeline DirectShow. Può anche essere eseguito nella pipeline Media Foundation all'interno di un wrapper fornito da Media Foundation. Un plug-in di questo tipo è denominato Microsoft DirectX Media Object (DMO). È comune pensare che un DMO sia analogo a un oggetto filtro in DirectShow. La documentazione di DMO è disponibile nella sezione DirectShow del Windows SDK.

Un plug-in che implementa **IMFTransform** e **IMFGetService** può essere eseguito in modo nativo (non è necessario alcun wrapper) nella pipeline Media Foundation richiesta. Un plug-in di questo tipo è denominato Media Foundation Transform (MFT). La documentazione di MFT è disponibile nella Media Foundation del Windows SDK.

Un plug-in che implementa **IMediaObject,** **IWMPPluginEnable,** **IMFTransform** e **IMFGetService** può essere eseguito nella pipeline DirectShow e può anche essere eseguito in modo nativo nella pipeline Media Foundation. Questo tipo di plug-in, denominato *plug-in DSP* in modalità doppia, può svolgere il ruolo di DMO o MFT.

Quando Windows Media Player un plug-in DSP a modalità doppia nella pipeline Media Foundation, esegue prima una query per **l'interfaccia IMFTransform.** Se la query ha esito negativo, Windows Media Player query per **l'interfaccia IMediaObject.** Se la query **IMediaObject** ha esito positivo, il plug-in viene incapsulato e aggiunto alla Media Foundation pipeline.

Indipendentemente dalla pipeline, qualsiasi plug-in DSP che consente all'utente di impostare le proprietà deve implementare **ISpecifyPropertyPages**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica degli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Interfacce plug-in DSP**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**Creazione di pacchetti plug-in DSP**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




