---
title: Interfacce obbligatorie (Windows Media Player SDK)
description: Interfacce obbligatorie
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Plug-in di Windows Media Player, interfacce
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- Plug-in DSP, interfacce
- interfacce, plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9c6923af513f2d241955b508f0872f85a4b020
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873217"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Interfacce obbligatorie (Windows Media Player SDK)

Windows Media Player esegue il rendering di audio e video utilizzando una delle seguenti pipeline.

-   DirectShow
-   Media Foundation

In Microsoft Windows XP e versioni precedenti, il lettore utilizza DirectShow. In Windows Vista, il lettore talvolta utilizza DirectShow e talvolta utilizza Media Foundation.

Un plug-in DSP implementa alcune o tutte le interfacce seguenti:

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **IMFTransform**
-   **IMFGetService**
-   **ISpecifyPropertyPages**

Un plug-in che implementa **IMediaObject** e **IWMPPluginEnable** può essere eseguito nella pipeline DirectShow. Può anche essere eseguito nella pipeline Media Foundation all'interno di un wrapper fornito da Media Foundation. Un plug-in di questo tipo è denominato Microsoft DirectX Media Object (DMO). È comune pensare a un DMO come analogo a un oggetto filtro in DirectShow. La documentazione DMO si trova nella sezione DirectShow del Windows SDK.

Un plug-in che implementa **IMFTransform** e **IMFGetService** può essere eseguito in modalità nativa (nessun wrapper necessario) nella pipeline Media Foundation. Un plug-in di questo tipo è denominato trasformazione Media Foundation (MFT). La documentazione di MFT si trova nella sezione Media Foundation della Windows SDK.

Un plug-in che implementa **IMediaObject**, **IWMPPluginEnable**, **IMFTransform** e **IMFGetService** può essere eseguito nella pipeline DirectShow e può anche essere eseguito in modalità nativa nella pipeline Media Foundation. Questo tipo di plug-in, noto come *plug-in DSP Dual Mode*, può svolgere il ruolo di DMO o MFT.

Quando Windows Media Player usa un plug-in DSP in modalità duale nella pipeline Media Foundation, esegue prima una query per l'interfaccia **IMFTransform** . Se la query ha esito negativo, Windows Media Player query per l'interfaccia **IMediaObject** . Se la query **IMediaObject** ha esito positivo, il plug-in viene incapsulato e aggiunto alla pipeline Media Foundation.

Indipendentemente dalla pipeline, qualsiasi plug-in DSP che consente all'utente di impostare le proprietà deve implementare **ISpecifyPropertyPages**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**Interfacce plug-in DSP**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**Creazione del pacchetto di plug-in DSP**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




