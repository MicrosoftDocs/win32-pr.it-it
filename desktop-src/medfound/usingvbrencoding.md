---
description: In questa sezione viene descritto come configurare i flussi VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Uso della codifica VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226496"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a>Uso della codifica VBR (Microsoft Media Foundation)

Come descritto in dettaglio nell'argomento [metodi di codifica](encodingmethods.md) , viene usata la codifica con velocità in bit variabile (VBR) per migliorare la coerenza della qualità del contenuto. Si configurano i flussi VBR nello stesso modo in cui si codificano i flussi di velocità in bit costante (CBR), ad eccezione dei parametri del buffer (velocità in bit e finestra del buffer). In questa sezione viene descritto come configurare i flussi VBR.

## <a name="configuring-quality-based-vbr"></a>Configurazione di VBR basato sulla qualità

La codifica tramite il metodo VBR basato sulla qualità non richiede parametri del buffer predefiniti. Si specifica invece un livello di qualità (da 0 a 100) che il codificatore utilizza per determinare dinamicamente i parametri del buffer appropriati. Questa modalità di codifica utilizza un solo passaggio di codifica.

È possibile enumerare i tipi di output VBR basati sulla qualità supportati per i codec audio. È necessario utilizzare uno dei tipi restituiti da DMO quando si imposta il tipo di output. Per altre informazioni, vedere [enumerazione di tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md).

Per configurare un flusso video VBR basato sulla qualità, è necessario impostare le proprietà elencate nella tabella seguente.



| Proprietà                                            | Descrizione                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_VBRENABLED MFPKEY](mfpkey-vbrenabledproperty.md) | Impostare su VARIANT \_ true.                                                                                                                                   |
| [\_VBRQUALITY MFPKEY](mfpkey-vbrqualityproperty.md) | Impostare sul valore di qualità desiderato, da 0 a 100. Non tutti i valori di qualità rappresentano impostazioni discrete. Per ulteriori informazioni, vedere la descrizione della proprietà. |



 

## <a name="configuring-unconstrained-vbr"></a>Configurazione di un VBR non vincolato

La codifica VBR non vincolata consente al codificatore di variare le dimensioni dei singoli campioni senza limiti di buffer espliciti. Tuttavia, la velocità in bit media per la durata del contenuto risultante deve essere minore o uguale al valore specificato. Il VBR non vincolato richiede due sessioni di codifica.

È possibile enumerare i tipi di output di VBR a due passaggi supportati per i codec audio. È necessario utilizzare uno dei tipi restituiti da DMO quando si imposta il tipo di output. Per altre informazioni, vedere [enumerazione di tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md).

Per configurare un flusso video VBR non vincolato, è necessario impostare le proprietà elencate nella tabella seguente.



| Proprietà                                            | Descrizione                          |
|-----------------------------------------------------|--------------------------------------|
| [\_VBRENABLED MFPKEY](mfpkey-vbrenabledproperty.md) | Impostare su VARIANT \_ true.                |
| [\_PASSESUSED MFPKEY](mfpkey-passesusedproperty.md) | Impostare su 2.                            |
| [\_RAVG MFPKEY](mfpkey-ravgproperty.md)             | Impostare sulla velocità in bit media desiderata. |



 

## <a name="configuring-peak-constrained-vbr"></a>Configurazione di Peak-Constrained VBR

Il numero di VBR con vincoli di picco è simile a quello di VBR non vincolato, perché è limitato a una velocità in bit media per la durata del flusso. Inoltre, la funzionalità VBR con vincoli di picco è conforme a un buffer di picco. Questo buffer viene descritto usando una velocità in bit massima e una finestra del buffer di picco, così come un buffer CBR viene descritto da una velocità in bit media e da una finestra del buffer. Questa modalità offre alla flessibilità del codificatore la modalità di codifica dei singoli campioni rispettando al massimo le limitazioni. Questa operazione è particolarmente utile quando la decodifica viene eseguita da un chip in un dispositivo, ad esempio un lettore DVD, in cui sono presenti limitazioni hardware che devono essere prese in considerazione.

I tipi di output supportati del codificatore audio VBR con vincoli di picco sono gli stessi tipi enumerati per VBR non vincolato. Impostare i valori di picco su DMO e utilizzare il tipo recapitato. Per altre informazioni, vedere [enumerazione di tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md).

Per configurare un flusso video VBR con vincoli di picco, è necessario impostare le proprietà elencate nella tabella seguente usando il metodo **IPropertyBag:: Write** .



| Proprietà                                            | Descrizione                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [\_VBRENABLED MFPKEY](mfpkey-vbrenabledproperty.md) | Impostare su VARIANT \_ true.                                           |
| [\_PASSESUSED MFPKEY](mfpkey-passesusedproperty.md) | Impostare su 2.                                                       |
| [\_RAVG MFPKEY](mfpkey-ravgproperty.md)             | Impostare sulla velocità in bit media desiderata.                            |
| [\_Rmax MFPKEY](mfpkey-rmaxproperty.md)             | Impostare sulla velocità in bit massima desiderata.                               |
| [\_BMAX MFPKEY](mfpkey-bmaxproperty.md)             | Impostare sulla finestra del buffer che corrisponde alla velocità in bit del picco. |



 

> [!Note]  
> È consigliabile impostare la velocità in bit massima su almeno il doppio della velocità in bit media. Impostando la velocità di picco su un valore inferiore, il codec può codificare il contenuto come CBR a due passaggi invece che con il picco di VBR.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> <dt>

[Uso della codifica Two-Pass](usingtwoencodingpasses.md)
</dt> <dt>

[Utilizzo di audio](workingwithaudio.md)
</dt> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 



