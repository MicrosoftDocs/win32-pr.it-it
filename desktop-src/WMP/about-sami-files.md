---
title: Informazioni sui file SAMI
description: Informazioni sui file SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Modello a oggetti di Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- modello a oggetti, interscambio multimediale accessibile sincronizzato (SAMI)
- Windows Media Player Mobile, Media Interchange accessibile sincronizzato (SAMI)
- Controllo ActiveX Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Windows Media Player Mobile ActiveX Control, Synchronized Accessible Media Interchange (SAMI)
- Controllo ActiveX, interscambio multimediale accessibile sincronizzato (SAMI)
- SAMI (Synchronized Accessible Media Interchange), file
- SAMI (interscambio multimediale accessibile sincronizzato), file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856266"
---
# <a name="about-sami-files"></a>Informazioni sui file SAMI

I file SAMI sono file di testo con estensione SMI o Sami. Contengono le stringhe di testo usate per le didascalie chiuse, i sottotitoli e le descrizioni audio sincronizzati. Specificano anche i parametri di intervallo usati dal controllo Media Player Windows per sincronizzare il testo della didascalia chiusa con contenuto audio o video. Quando un file multimediale digitale raggiunge un'ora designata nel file SAMI, il testo viene modificato di conseguenza nell'area di visualizzazione didascalia chiusa della pagina Web.

Oltre a un semplice editor di testo, ad esempio Microsoft Notepad, non è necessario un software speciale per creare un file SAMI. SAMI e HTML condividono elementi comuni, ad esempio i <HEAD> <BODY> tag e. Come in HTML, i tag usati nei file SAMI devono essere sempre usati in coppie. Ad esempio, un elemento BODY inizia con un <BODY> tag e deve terminare sempre con un </BODY> tag.

Un file SAMI di base richiede tre tag fondamentali: <SAMI> , <HEAD> e <BODY> .

Il <SAMI> tag identifica il documento come documento Sami, in modo che le altre applicazioni possano riconoscere il formato del file.

Tra i tag <HEAD> e </HEAD> si definiscono le linee guida di base e altre informazioni sul formato per il documento Sami, ad esempio il titolo del documento, le informazioni generali e le proprietà di stile per i sottotitoli codificati. Analogamente al codice HTML, il contenuto dichiarato all'interno dell'elemento HEAD non viene visualizzato come output.

Gli elementi e gli attributi definiti tra i tag <BODY> e </BODY> visualizzano il contenuto visualizzato dall'utente. In SAMI l'elemento BODY contiene i parametri per la sincronizzazione e le stringhe di testo utilizzate per le didascalie chiuse.

Definito all'interno dell'elemento HEAD, l'elemento STYLE fornisce la funzionalità aggiuntiva in SAMI. Tra i tag <STYLE> e </STYLE> è possibile definire diversi selettori CSS (CSS) per lo stile e il layout. È possibile personalizzare le proprietà di stile, ad esempio tipi di carattere, dimensioni e allineamento, per offrire un'esperienza utente avanzata e promuovere anche l'accessibilità. Ad esempio, la definizione di una classe di stile del tipo di carattere testo di grandi dimensioni può migliorare la leggibilità per gli utenti che hanno difficoltà a leggere testo di piccole dimensioni. Inoltre, definendo diverse classi di linguaggio, è possibile aiutare gli utenti internazionali a comprendere meglio il contenuto multimediale digitale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Aggiunta di didascalie chiuse a file multimediali digitali**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




