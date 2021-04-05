---
title: Per enumerare i formati di codec
description: Per enumerare i formati di codec
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- flussi, enumerazione dei formati di codec
- codec, enumerazioni
- flussi, formati di codec
- codec, formati
- codec, interfaccia IWMCodecInfo
- IWMCodecInfo, formati di codec
- codec, interfaccia IWMCodecInfo3
- IWMCodecInfo3, formati di codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea062723ec1480a82b45fd025fb7a8c37020d5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046430"
---
# <a name="to-enumerate-codec-formats"></a>Per enumerare i formati di codec

Un formato di codec è un oggetto di configurazione del flusso popolato con i dati di un codec. Ogni formato di codec contiene una configurazione multimediale supportata dal codec. La maggior parte dei codec audio supporta un numero finito di formati, ciascuno dei quali è enumerato dal codec ed è possibile accedervi usando i metodi di [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo). I codec video, d'altra parte, forniscono un unico formato. Ciò è dovuto al fatto che i flussi video presentano variabili, ad esempio le dimensioni del frame, più flessibili rispetto alle impostazioni di un flusso audio. Con un flusso video, è necessario compilare alcuni valori di configurazione del flusso. è necessario modificare le configurazioni del flusso audio solo per assegnare un nome, un nome di connessione e un numero di flusso. Per altre informazioni, vedere [configurazione comune a tutti i flussi](configuration-common-to-all-streams.md).

I formati di codec enumerati dipendono dalle impostazioni correnti di enumerazione dei codec, che vengono impostate usando [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting). Attualmente sono supportate solo due proprietà del codec: g \_ wszNumPasses, che specifica il numero di sessioni di codifica che verranno eseguite dal codec e g \_ wszVBREnabled, che specifica se il codec userà la codifica della velocità in bit variabile. Il numero massimo di passaggi di codifica supportati da uno qualsiasi dei codec è due, quindi sono disponibili quattro configurazioni distinte per le quali è possibile recuperare i codec, come illustrato nella tabella seguente.



|                  | Flusso di velocità in bit costante (CBR) | flusso CBR 2-pass | Flusso della velocità in bit della variabile basata sulla qualità (VBR) | Flusso VBR basato sulla velocità in bit (vincolato o non vincolato) |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| g \_ wszVBREnabled | FALSE                          | FALSE             | TRUE                                         | true                                                     |
| g \_ wszNumPasses  | 1                              | 2                 | 1                                            | 2                                                        |



 

Per enumerare i formati supportati per un codec, usare [**IWMCodecInfo:: GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) per trovare il numero di codec supportati. Chiamare quindi [**IWMCodecInfo:: GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) per ogni formato. Gli indici di formato variano da zero a uno inferiore al numero totale di formati supportati. È possibile recuperare una descrizione del formato chiamando [**IWMCodecInfo2:: GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc). Quando si usa **GetCodecFormatDesc**, non è necessario usare **GetCodecFormat**, perché l'oggetto di configurazione del flusso viene recuperato da entrambi i metodi. I formati di codec video non includono una descrizione. Ogni codec video ha un solo formato utilizzato per tutti i flussi di quel tipo.

Quando si recupera un formato di codec, si ottiene l'interfaccia [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) di un oggetto di configurazione del flusso contenente le impostazioni di formato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Recupero delle informazioni di configurazione dei flussi dai codec**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




