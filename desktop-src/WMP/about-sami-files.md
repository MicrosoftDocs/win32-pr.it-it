---
title: Informazioni sui file SAMI
description: Informazioni sui file SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player a oggetti, Synchronized Accessible Media Interchange (SAMI)
- modello a oggetti, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Dispositivi mobili, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Controllo ActiveX mobile,Synchronized Accessible Media Interchange (SAMI)
- ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Synchronized Accessible Media Interchange (SAMI),files
- SAMI (Synchronized Accessible Media Interchange), file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bcb4823ee02a501254218a9b7c4d9aaf347894d895bc193c8ce763658db174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470461"
---
# <a name="about-sami-files"></a>Informazioni sui file SAMI

I file SAMI sono file di testo con estensione smi o sami. Contengono le stringhe di testo usate per sottotitoli codificati sincronizzati, sottotitoli e descrizioni audio. Specificano anche i parametri di temporizzazione usati dal Windows Media Player per sincronizzare il testo di sottotitoli codificati con contenuto audio o video. Quando un file multimediale digitale raggiunge un'ora designata nel file SAMI, il testo cambia di conseguenza nell'area di visualizzazione dei sottotitoli codificati della pagina Web.

A parte un semplice editor di testo (ad esempio Microsoft Blocco note), non è necessario software speciale per creare un file SAMI. SAMI e HTML condividono elementi comuni, ad esempio <HEAD> e <BODY> Tag. Come nel codice HTML, i tag usati nei file SAMI devono essere sempre usati a coppie. Ad esempio, un elemento BODY inizia con <BODY> tag e devono sempre terminare con </BODY> tag .

Un file SAMI di base richiede tre tag fondamentali: <SAMI> , <HEAD>e <BODY>.

Il <SAMI> tag identifica il documento come documento SAMI in modo che altre applicazioni possano riconoscerne il formato di file.

Tra <HEAD> e </HEAD> , si definiscono le linee guida di base e altre informazioni sul formato per il documento SAMI, ad esempio il titolo del documento, le informazioni generali e le proprietà di stile per i sottotitoli codificati. Analogamente al codice HTML, il contenuto dichiarato all'interno dell'elemento HEAD non viene visualizzato come output.

Elementi e attributi definiti tra <BODY> e </BODY> I tag visualizzano il contenuto visualizzato dall'utente. In SAMI l'elemento BODY contiene i parametri per la sincronizzazione e le stringhe di testo usate per i sottotitoli codificati.

Definito all'interno dell'elemento HEAD, l'elemento STYLE fornisce funzionalità aggiuntive in SAMI. Tra i <STYLE> tag </STYLE> e è possibile definire diversi selettori CSS (Cascading Style Sheet) per lo stile e il layout. Le proprietà di stile, ad esempio tipi di carattere, dimensioni e allineamento, possono essere personalizzate per offrire un'esperienza utente più ricca, promuovendo al tempo stesso l'accessibilità. Ad esempio, la definizione di una classe di stile per caratteri di testo di grandi dimensioni può migliorare la leggibilità per gli utenti che hanno difficoltà a leggere testo di piccole dimensioni. Inoltre, definendo diverse classi di linguaggio, è possibile aiutare gli utenti internazionali a comprendere meglio il contenuto multimediale digitale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Aggiunta di sottotitoli codificati a supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




