---
title: Configurazione di video Flussi
description: Configurazione di video Flussi
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- flussi, configurazione di flussi video
- codec, configurazione di flussi video
- flussi video, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bc6e011f32d1ea9a9905c718ad8ff0c13f7d57650a30316ecfec6332978fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809591"
---
# <a name="configuring-video-streams"></a>Configurazione di video Flussi

I flussi video sono più flessibili nella configurazione rispetto ai flussi audio. Ciò è dovuto al fatto che le proprietà dei fotogrammi che costituiscono il video possono variare notevolmente da un file a quello successivo. Quando si recupera il formato del codec per il codec in uso, è necessario impostare i valori seguenti per gli oggetti di configurazione del flusso video.



| Valore                                 | Descrizione                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Velocità in bit                              | Chiamare [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) per impostare sul valore desiderato. Il codec video tenterà di comprimere i file multimediali in base alle specifiche. Se i valori sono troppo bassi, il video compresso risultante sarà molto danneggiato.           |
| Finestra Buffer                         | Chiamare [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) per impostare sul valore desiderato. Il codec video tenterà di comprimere i file multimediali in base alle specifiche. Se i valori sono troppo bassi, il video compresso risultante sarà molto danneggiato. |
| **WMVIDEOINFOHEADER.rcSource**        | L'angolo superiore sinistro deve essere impostato su 0,0. L'angolo inferiore destro deve essere impostato in base alle dimensioni del frame. Ad esempio, in un flusso 640x480 queste impostazioni saranno 0,0,640,480.                                                                                                |
| **WMVIDEOINFOHEADER.rcTarget**        | Deve corrispondere a **rcSource.**                                                                                                                                                                                                                                                    |
| **WMVIDEOINFOHEADER.dwBitRate**       | Deve corrispondere alla velocità in bit impostata per il flusso.                                                                                                                                                                                                                                 |
| **WMVIDEOINFOHEADER. AvgTimePerFrame** | Impostare sul tempo approssimativo per fotogramma.                                                                                                                                                                                                                                      |
| **BITMAPINFOHEADER.biWidth**          | Impostare la larghezza, in pixel, delle dimensioni del frame desiderate.                                                                                                                                                                                                                     |
| **BITMAPINFOHEADER.biHeight**         | Impostare sull'altezza, in pixel, delle dimensioni del frame desiderate.                                                                                                                                                                                                                    |



 

Il contenuto video non viene riprodotto correttamente a meno che non sia codificato in una dimensione che sia un multiplo di quattro sia per larghezza che per altezza. L'eccezione è il video [*RGB*](wmformat-glossary.md) non compresso, che può essere di qualsiasi dimensione. Se si tenta di impostare una dimensione che non è un multiplo di quattro, uno degli errori seguenti verrà restituito dal writer:

-   FORMATO DI \_ INPUT NS E \_ NON \_ \_ VALIDO
-   FORMATO DI \_ OUTPUT NS E \_ NON \_ \_ VALIDO
-   NS \_ E \_ INVALIDPROFILE

Se si usa la codifica a velocità in bit variabile, potrebbe essere necessario apportare altre modifiche. Per altre informazioni, vedere [Configuring VBR Flussi](configuring-vbr-streams.md).

Alcuni Windows codec Video multimediali supportano più livelli di complessità. I livelli di complessità determinano gli algoritmi che verranno utilizzati dal codec durante la codifica di un flusso video. L'uso di un livello di complessità elevato richiede una maggiore potenza di elaborazione per la codifica e la decodifica.

Ogni codec che supporta le impostazioni di complessità espone le impostazioni seguenti che è possibile recuperare con il [**metodo IWMCodecInfo3::GetCodecProp.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop)



| Impostazione                 | Descrizione                                         |
|-------------------------|-----------------------------------------------------|
| g \_ wszComplexityMax     | Livello di qualità massimo supportato dal codec.   |
| g \_ wszComplexityOffline | Livello di qualità suggerito per la riproduzione offline.   |
| g \_ wszComplexityLive    | Livello di qualità suggerito per la riproduzione in streaming. |



 

Per impostare la complessità di un flusso video in un profilo, usare il metodo [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) usando la proprietà g \_ wszComplexity. Il valore impostato deve essere minore o uguale alla complessità massima supportata per il codec.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i Flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di Flussi**](configuring-streams.md)
</dt> <dt>

[**Problemi di Impostazioni**](video-complexity-settings.md)
</dt> </dl>

 

 




