---
description: In questo argomento viene descritta la differenza tra i tipi di supporto completi e i tipi di supporti parziali.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Tipi di supporti completi e parziali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530523"
---
# <a name="complete-and-partial-media-types"></a>Tipi di supporti completi e parziali

In questo argomento viene descritta la differenza tra i tipi di supporto completi e i tipi di supporti parziali.

## <a name="complete-media-types"></a>Tipi di supporto completi

Un tipo di supporto *completo* è uno che definisce completamente il formato del flusso multimediale. Dato un tipo di supporto completo, un componente della pipeline può analizzare i dati del flusso associati al tipo di supporto senza ambiguità.

Per i formati non compressi, gli argomenti seguenti definiscono gli attributi necessari per un tipo di supporto completo:

-   Audio: [tipi di supporti audio non compressi](uncompressed-audio-media-types.md)
-   Video: [tipi di supporti video non compressi](uncompressed-video-media-types.md)

Per i flussi compressi (o *codificati*), la definizione di un tipo di supporto completo è definita dal codec. Tuttavia, se sono noti attributi di tipo non compressi per il flusso compresso, questi valori devono essere inclusi nel tipo di supporto per il flusso compresso. Se, ad esempio, le dimensioni del frame sono note, impostare l'attributo [**MF \_ mt \_ frame \_ size**](mf-mt-frame-size-attribute.md) sul tipo di supporto, anche se tecnicamente un flusso compresso non ha una dimensione del frame.

## <a name="partial-media-types"></a>Tipi di supporti parziali

Un tipo di supporto *parziale* non dispone di uno o più attributi necessari per un tipo di supporto completo. Quando si enumerano i tipi di supporti possibili, un componente Microsoft Media Foundation può lasciare un valore non impostato, per indicare che è in grado di gestire qualsiasi valore. Ad esempio, un processore video potrebbe lasciare invariato l'attributo della [**\_ \_ \_ frequenza dei fotogrammi MF mt**](mf-mt-frame-rate-attribute.md) per indicare che è in grado di gestire qualsiasi frequenza dei fotogrammi e di eseguire una conversione della frequenza dei fotogrammi, se necessario.

Se si crea un tipo di supporto parziale, è comunque necessario includere tutte le informazioni che si conoscono. Tuttavia, un tipo di supporto non deve includere informazioni non sicure. È preferibile che le informazioni siano mancanti rispetto a quelle errate.

Come minimo, un tipo di supporto parziale deve includere solo due attributi: [**il \_ \_ \_ tipo principale MF mt**](mf-mt-major-type-attribute.md) e il [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md).

A volte Media Foundation componenti deve fornire tipi di supporto completi:

-   Le origini multimediali devono fornire tipi di output completi.
-   I decodificatori devono fornire tipi di output completi, dopo l'impostazione del tipo di input. Prima di impostare il tipo di input, un decodificatore potrebbe fornire un tipo di output parziale.
-   I codificatori devono fornire tipi di input completi, dopo che è stato impostato il tipo di output. Prima di impostare il tipo di output, è possibile che un codificatore fornisca un tipo di input parziale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporto](media-types.md)
</dt> </dl>

 

 



