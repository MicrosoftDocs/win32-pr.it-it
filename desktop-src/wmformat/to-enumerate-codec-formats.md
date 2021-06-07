---
title: Per enumerare i formati di codec
description: Per enumerare i formati di codec
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- flussi, enumerazione dei formati di codec
- codec, enumerazioni
- flussi, formati di codec
- codec, formati
- codecs,interfaccia IWMCodecInfo
- IWMCodecInfo,formati codec
- codecs,interfaccia IWMCodecInfo3
- IWMCodecInfo3,formati codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a00c9afdbeba5a187be4b992a19d4c9bdb138e1
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444782"
---
# <a name="to-enumerate-codec-formats"></a>Per enumerare i formati di codec

Un formato codec è un oggetto di configurazione del flusso popolato con i dati di un codec. Ogni formato di codec contiene una configurazione multimediale supportata dal codec. La maggior parte dei codec audio supporta un numero finito di formati, ognuno dei quali viene enumerato dal codec ed è accessibile tramite i metodi [**di IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo). I codec video, d'altra parte, forniscono un solo formato. Questo perché i flussi video hanno variabili, come le dimensioni dei fotogrammi, più flessibili rispetto alle impostazioni di un flusso audio. Con un flusso video, è necessario compilare alcuni dei valori di configurazione del flusso. Le configurazioni del flusso audio devono essere modificate solo per assegnare un nome, un nome di connessione e un numero di flusso. Per altre informazioni, vedere [Configurazione comune a tutti i flussi.](configuration-common-to-all-streams.md)

I formati di codec enumerati dipendono dalle impostazioni correnti dell'enumerazione dei codec, impostate tramite [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting). Attualmente sono supportate solo due proprietà del codec: g wszNumPasses, che specifica il numero di passaggi di codifica che il codec eseguirà, e \_ g wszVBREnabled, che specifica se il codec userà la codifica a velocità in \_ bit variabile. Il numero massimo di passaggi di codifica supportati da uno dei codec è due, quindi sono disponibili quattro configurazioni distinte per cui è possibile recuperare i codec, come illustrato nella tabella seguente.



|    &nbsp;    | Flusso CBR (Constant Bit Rate) | Flusso CBR a 2 passi | Flusso VBR (Quality-Based Variable Bit Rate) | Flusso VBR basato su velocità in bit (vincolato o senza vincoli) |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| g \_ wszVBREnabled | FALSE                          | FALSE             | TRUE                                         | true                                                     |
| g \_ wszNumPasses  | 1                              | 2                 | 1                                            | 2                                                        |



 

Per enumerare i formati supportati per un codec, usare [**IWMCodecInfo::GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) per trovare il numero di codec supportati. Chiamare quindi [**IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) per ogni formato. Gli indici di formato vanno da zero a uno minore del numero totale di formati supportati. È possibile recuperare una descrizione del formato chiamando [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc). Quando si **usa GetCodecFormatDesc**, non è necessario usare **GetCodecFormat**, perché l'oggetto di configurazione del flusso viene recuperato da entrambi i metodi. I formati di codec video non includono una descrizione. Ogni codec video ha un solo formato usato per tutti i flussi di quel tipo.

Quando si recupera un formato codec, si ottiene [**l'interfaccia IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) di un oggetto di configurazione del flusso contenente le impostazioni del formato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Recupero delle informazioni di configurazione del flusso dai codec**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




