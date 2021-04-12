---
description: In questo argomento vengono fornite alcune linee guida per l'implementazione di un decodificatore o un codificatore come Media Foundation Transform (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Implementazione di un codec MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233748"
---
# <a name="implementing-a-codec-mft"></a>Implementazione di un codec MFT

In questo argomento vengono fornite alcune linee guida per l'implementazione di un decodificatore o un codificatore come Media Foundation Transform (MFT).

-   [Codificatori](#encoders)
    -   [Negoziazione del formato del codificatore](#encoder-format-negotiation)
-   [Decodificatori](#decoders)
    -   [Decodificatori solo transcodificati](#transcode-only-decoders)
    -   [Attributi di telecine](#telecine-attributes)
-   [Argomenti correlati](#related-topics)

## <a name="encoders"></a>Codificatori

### <a name="encoder-format-negotiation"></a>Negoziazione del formato del codificatore

La procedura seguente viene usata per inizializzare un codificatore:

1.  Eseguire una query su MFT per l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .
2.  Chiamare [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) per impostare le proprietà di codifica.
3.  Chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il formato di codifica.
4.  Chiamare [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) per ottenere un elenco di tipi di input compatibili. Questo passaggio potrebbe essere ignorato.
5.  Chiamare [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) per impostare il formato di input non compresso.

Dopo aver impostato il tipo di output nel passaggio 3, il metodo [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) deve restituire un elenco di tipi di input compatibili con il tipo di output corrente. In altre parole, qualsiasi tipo restituito da **GetInputAvailableType** a questo punto deve essere valido per [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

Per i decodificatori, l'ordine in cui vengono impostati i tipi è invertito: il tipo di input è impostato per primo, seguito dal tipo di output. Dopo aver impostato il tipo di input, il metodo [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) deve restituire un elenco di tipi che possono essere passati al metodo [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) .

I codificatori e i decodificatori devono supportare NV12 come formato non compresso comune. Ciò garantisce che i componenti della pipeline possano interagire con le conversioni minime dello spazio dei tipi. Naturalmente, anche altri formati possono essere supportati.

## <a name="decoders"></a>Decodificatori

### <a name="transcode-only-decoders"></a>Decodificatori di Transcode-Only

Alcuni decodificatori sono ottimizzati per la transcodifica (decodifica e Ricodifica di un flusso) e non sono adatti per l'uso durante la riproduzione.

Se un decodificatore MFT è destinato solo alla transcodifica, impostare il flag dell' **\_ enumerazione MFT \_ flag \_ transcode \_ only** quando si registra il MFT. Vedere [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).

Per impostazione predefinita, i decodificatori di transcodifica non vengono restituiti dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) . Per enumerare i decodificatori di transcodifica, chiamare **MFTEnumEx** e impostare il flag di **enumerazione del \_ flag di enumerazione \_ \_ \_ MFT** nel parametro *Flags* . Se utilizzata nella funzione **MFTEnumEx** , questo flag enumera sia i decodificatori transcodificati che altri decodificatori.



| **\_ \_ \_ \_ Solo transcodifica flag di enumerazione MFT** MFTRegister | **\_ \_ \_ \_ Solo transcodifica flag di enumerazione MFT** MFTEnumEx | Il MFT è enumerato? |
|--------------------------------------------------|------------------------------------------------|--------------------|
| 1                                                | 1                                              | Sì                |
| 1                                                | 0                                              | No                 |
| 0                                                | 1                                              | Sì                |
| 0                                                | 0                                              | Sì                |



 

### <a name="telecine-attributes"></a>Attributi di telecine

L'origine multimediale potrebbe alleghi gli attributi di telecine seguenti agli esempi di supporti che fornisce.



| Attributo                                                                                   | Descrizione                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [**\_RepeatFirstField MFSampleExtension**](mfsampleextension-repeatfirstfield-attribute.md) | Equivalente al flag "Repeat First Field" (RFF). |
| [**\_BottomFieldFirst MFSampleExtension**](mfsampleextension-bottomfieldfirst-attribute.md) | Inverso del flag "Top Field First" (TFF).       |



 

Questi flag forniscono un suggerimento al renderer video migliorato (EVR) quando esegue il deinterlacciamento. Un decodificatore deve propagare questi flag downstream copiando gli esempi di output, in modo che raggiungano la EVR.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 
