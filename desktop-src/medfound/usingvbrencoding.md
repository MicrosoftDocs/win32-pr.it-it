---
description: Questa sezione descrive come configurare i flussi VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Uso della codifica VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a9e1a61baf0539c0597e68f24dfad1496918012e52f778a1b7a64de27e5faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871230"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a>Uso della codifica VBR (Microsoft Media Foundation)

Come descritto in dettaglio nell'argomento [Metodi](encodingmethods.md) di codifica, la codifica VBR (Variable Bit Rate) viene usata per migliorare la coerenza della qualità del contenuto. I flussi VBR vengono configurati nello stesso modo in cui si codificano i flussi CBR (Constant Bit Rate), ad eccezione dei parametri del buffer (velocità in bit e finestra del buffer). Questa sezione descrive come configurare i flussi VBR.

## <a name="configuring-quality-based-vbr"></a>Configurazione di VBR basato sulla qualità

La codifica con il metodo VBR basato sulla qualità non richiede parametri di buffer predefiniti. Si specifica invece un livello di qualità (da 0 a 100) che il codificatore usa per determinare dinamicamente i parametri del buffer appropriati. Questa modalità di codifica usa un solo passaggio di codifica.

È possibile enumerare i tipi di output VBR basati sulla qualità supportati per i codec audio. È necessario usare uno dei tipi restituiti dall'DMO quando si imposta il tipo di output. Per altre informazioni, vedere [Enumerazione di tipi audio per modalità di codifica specifiche.](enumeratingaudiotypesforspecificencodingmodes.md)

Per configurare un flusso video VBR basato sulla qualità, è necessario impostare le proprietà elencate nella tabella seguente.



| Proprietà                                            | Descrizione                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Impostare su VARIANT \_ TRUE.                                                                                                                                   |
| [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md) | Impostare sul valore di qualità desiderato, da 0 a 100. Non tutti i valori di qualità rappresentano impostazioni discrete. Per altre informazioni, vedere la descrizione della proprietà. |



 

## <a name="configuring-unconstrained-vbr"></a>Configurazione di VBR senza vincoli

La codifica VBR senza vincoli consente al codificatore di variare le dimensioni dei singoli campioni senza limiti espliciti del buffer. Tuttavia, la velocità in bit media per la durata del contenuto risultante deve essere minore o uguale al valore specificato. VbR senza vincoli richiede due passaggi di codifica.

È possibile enumerare i tipi di output VBR a due passi supportati per i codec audio. È necessario usare uno dei tipi restituiti dall'DMO quando si imposta il tipo di output. Per altre informazioni, vedere [Enumerazione di tipi audio per modalità di codifica specifiche.](enumeratingaudiotypesforspecificencodingmodes.md)

Per configurare un flusso video VBR senza vincoli, è necessario impostare le proprietà elencate nella tabella seguente.



| Proprietà                                            | Descrizione                          |
|-----------------------------------------------------|--------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Impostare su VARIANT \_ TRUE.                |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Impostare su 2.                            |
| [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)             | Impostare sulla velocità in bit media desiderata. |



 

## <a name="configuring-peak-constrained-vbr"></a>Configurazione di Peak-Constrained VBR

VbR con vincoli di picco è simile a VBR senza vincoli in quanto è limitato a una velocità in bit media per la durata del flusso. Inoltre, la funzione VBR con vincoli di picco è conforme a un buffer di picco. Questo buffer viene descritto usando una velocità in bit di picco e una finestra di picco del buffer, proprio come un buffer CBR è descritto da una velocità in bit media e da una finestra del buffer. Questa modalità offre al codificatore flessibilità nel modo in cui codifica singoli campioni rispettando le limitazioni di picco. Ciò è particolarmente utile quando la decodifica viene eseguita da un chip in un dispositivo, ad esempio un lettore DVD, in cui è necessario considerare alcune limitazioni hardware.

I tipi di output del codificatore audio VBR con limiti di picco supportati sono gli stessi tipi enumerati per VBR senza vincoli. Impostare i valori di picco nella DMO e usare il tipo recapitato. Per altre informazioni, vedere [Enumerazione di tipi audio per modalità di codifica specifiche.](enumeratingaudiotypesforspecificencodingmodes.md)

Per configurare un flusso video VBR con limiti di picco, è necessario impostare le proprietà elencate nella tabella seguente usando il **metodo IPropertyBag::Write.**



| Proprietà                                            | Descrizione                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md) | Impostare su VARIANT \_ TRUE.                                           |
| [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) | Impostare su 2.                                                       |
| [MFPKEY \_ RAVG](mfpkey-ravgproperty.md)             | Impostare sulla velocità in bit media desiderata.                            |
| [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)             | Impostare sulla velocità in bit di picco desiderata.                               |
| [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)             | Impostare sulla finestra del buffer che corrisponde alla velocità in bit di picco. |



 

> [!Note]  
> È consigliabile impostare la velocità in bit di picco su almeno il doppio della velocità in bit media. Impostando la frequenza di picco su un valore inferiore, il codec potrebbe codificare il contenuto come CBR a due passi invece di VBR con vincoli di picco.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> <dt>

[Uso Two-Pass codifica](usingtwoencodingpasses.md)
</dt> <dt>

[Uso dell'audio](workingwithaudio.md)
</dt> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 



