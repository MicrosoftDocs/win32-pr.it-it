---
title: Configurazione dei flussi video
description: Configurazione dei flussi video
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- flussi, configurazione di flussi video
- codec, configurazione dei flussi video
- flussi video, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299384"
---
# <a name="configuring-video-streams"></a>Configurazione dei flussi video

La configurazione dei flussi video è più flessibile rispetto ai flussi audio. Questo perché le proprietà dei frame che compongono il video possono variare notevolmente da un file a quello successivo. Quando si recupera il formato di codec per il codec in uso, è necessario impostare i valori seguenti per gli oggetti di configurazione del flusso video.



| Valore                                 | Descrizione                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Velocità in bit                              | Chiamare [**IWMStreamConfig:: bitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) per impostare sul valore desiderato. Il codec video tenterà di comprimere il supporto per soddisfare le specifiche. Se i valori sono troppo bassi, il video compresso risultante sarà molto degradato.           |
| Finestra buffer                         | Chiamare [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) per impostare sul valore desiderato. Il codec video tenterà di comprimere il supporto per soddisfare le specifiche. Se i valori sono troppo bassi, il video compresso risultante sarà molto degradato. |
| **WMVIDEOINFOHEADER.rcSource**        | L'angolo superiore sinistro deve essere impostato su 0, 0. È necessario impostare l'angolo inferiore destro sulle dimensioni del frame. Ad esempio, in un flusso 640x480 queste impostazioni saranno pari a 0, 0640480.                                                                                                |
| **WMVIDEOINFOHEADER.rcTarget**        | Deve corrispondere a **rcSource**.                                                                                                                                                                                                                                                    |
| **WMVIDEOINFOHEADER.dwBitRate**       | Deve corrispondere alla velocità in bit impostata per il flusso.                                                                                                                                                                                                                                 |
| **WMVIDEOINFOHEADER. AvgTimePerFrame** | Impostare sull'ora approssimativa per fotogramma.                                                                                                                                                                                                                                      |
| **BITMAPINFOHEADER. biWidth**          | Impostare sulla larghezza, in pixel, della dimensione del fotogramma desiderata.                                                                                                                                                                                                                     |
| **BITMAPINFOHEADER. biHeight**         | Impostare sull'altezza, in pixel, della dimensione del fotogramma desiderata.                                                                                                                                                                                                                    |



 

Il contenuto video non viene eseguito correttamente a meno che non sia codificato con una dimensione che rappresenta un multiplo di quattro per larghezza e altezza. L'eccezione è il video non compresso [*RGB*](wmformat-glossary.md) , che può essere qualsiasi dimensione. Se si tenta di impostare una dimensione che non è un multiplo di quattro, uno degli errori seguenti verrà restituito dal writer:

-   \_formato di input NS E \_ non valido \_ \_
-   \_formato di output NS E \_ non valido \_ \_
-   NS \_ E \_ INVALIDPROFILE

Se si utilizza la codifica della velocità in bit variabile, potrebbe essere necessario apportare altre modifiche. Per ulteriori informazioni, vedere [configurazione dei flussi VBR](configuring-vbr-streams.md).

Alcuni Windows Media Video codec supportano più livelli di complessità. I livelli di complessità determinano gli algoritmi che il codec userà per la codifica di un flusso video. L'utilizzo di un livello di complessità elevato richiede una maggiore potenza di elaborazione per la codifica e la decodifica.

Ogni codec che supporta le impostazioni di complessità espone le impostazioni seguenti che è possibile recuperare con il metodo [**IWMCodecInfo3:: GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) .



| Impostazione                 | Descrizione                                         |
|-------------------------|-----------------------------------------------------|
| g \_ wszComplexityMax     | Livello di qualità massimo supportato dal codec.   |
| g \_ wszComplexityOffline | Livello di qualità suggerito per la riproduzione offline.   |
| g \_ wszComplexityLive    | Livello di qualità suggerito per la riproduzione del flusso. |



 

Per impostare la complessità per un flusso video in un profilo, usare il metodo [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) usando la proprietà g \_ wszComplexity. Il valore impostato deve essere minore o uguale alla complessità massima supportata per il codec.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> <dt>

[**Impostazioni di complessità video**](video-complexity-settings.md)
</dt> </dl>

 

 




