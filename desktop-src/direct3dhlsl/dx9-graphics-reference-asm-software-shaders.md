---
title: Shader software
description: Gli shader software sono implementati per consentire lo sviluppo di shader senza supporto hardware sottostante. Supportano il set completo di funzionalità. Poiché sono implementate nel software, non produrranno le prestazioni migliori.
ms.assetid: 0153732d-a487-473b-ad77-32ab457979f5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df101edd0362321847fb9c0baf7feb3cc865e2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045386"
---
# <a name="software-shaders"></a>Shader software

Gli shader software sono implementati per consentire lo sviluppo di shader senza supporto hardware sottostante. Supportano il set completo di funzionalità. Poiché sono implementate nel software, non produrranno le prestazioni migliori.



| Versione   | Set di funzionalità                  | Requisiti                                                         |
|-----------|------------------------------|----------------------------------------------------------------------|
| vs \_ 2 \_ SW | Tutte le funzionalità di vs \_ 2 \_ x | Supportato solo dall'elaborazione dei vertici software e da un dispositivo di riferimento. |
| Visual Studio \_ 3 \_ SW | Tutte le funzionalità di vs \_ 3 \_ 0 | Supportato solo dall'elaborazione dei vertici software e da un dispositivo di riferimento. |
| PS \_ 2 \_ SW | Tutte le funzionalità di PS \_ 2 \_ x | Supportato solo da un dispositivo di riferimento.                                |
| PS \_ 3 \_ SW | Tutte le funzionalità di PS \_ 3 \_ 0 | Supportato solo da un dispositivo di riferimento.                                |



 

Alcune convalide sono rilassate per gli shader software. Questa operazione è utile a scopo di debug e creazione di prototipi. Le convalide seguenti sono rilassate: (tutte le altre convalide rimangono invariate)



| Validation type (Tipo di convalida)                                 | Relax                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Conteggi istruzioni:                             | Questo è rilassato per vs \_ 2 \_ SW, vs \_ 3 SW \_ e PS \_ 2 SW \_ , PS \_ 3 \_ SW. Sono consentite istruzioni illimitate.                                                                                                              |
| Conteggi costanti float:                          | Questo è rilassato per vs \_ 2 \_ SW, vs \_ 3 SW \_ e PS \_ 2 SW \_ , PS \_ 3 \_ SW. Sono consentite fino a 8192 costanti.                                                                                                                |
| Conteggi costanti integer:                        | Questo è rilassato per vs \_ 2 \_ SW, vs \_ 3 SW \_ e PS \_ 2 SW \_ , PS \_ 3 \_ SW. Sono consentite fino a 2048 costanti.                                                                                                                |
| Conteggi costanti booleane:                        | Questo è rilassato per vs \_ 2 \_ SW, vs \_ 3 SW \_ e PS \_ 2 SW \_ , PS \_ 3 \_ SW. Sono consentite fino a 2048 costanti.                                                                                                                |
| Profondità lettura dipendente:                           | Questo è rilassato per PS \_ 2 \_ SW. Come in vs \_ 3 \_ 0 e PS \_ 3 \_ 0, sono consentite letture dipendenti illimitate.                                                                                                                |
| Numero di istruzioni ed etichette per il controllo di flusso: | Questo è rilassato per vs \_ 2 \_ SW. Sono consentite istruzioni di controllo di flusso illimitate e fino a 2048 etichette.                                                                                                                |
| Conteggio cicli/avvio/passaggio:                          | Questi sono rilassati per vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW e PS \_ 3 \_ SW. Le dimensioni dei passaggi di inizio e di interoperabilità delle iterazioni per le istruzioni Rep e loop sono con segno a 32 bit. Il numero di interzioni può essere massimo \_ int/64. |
| Limiti di lettura-porta:                               | vs \_ 2 \_ SW, vs \_ 3 \_ SW, PS \_ 2 \_ SW e PS \_ 3 \_ SW non hanno limiti di lettura della porta.                                                                                                                                              |
| Numero di interpolatori:                        | Sono presenti 16 [registri-vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) in vs \_ 3 \_ SW e 10 [PS \_ 3 \_ 0 registri](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# ) per PS \_ 3 \_ SW.     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ASM shader](dx9-graphics-reference-asm.md)
</dt> </dl>

 

 




