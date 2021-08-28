---
title: Informazioni sui file SAMI
description: Informazioni sui file SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player a oggetti, Synchronized Accessible Media Interchange (SAMI)
- modello a oggetti,Interscambio multimediale accessibile sincronizzato (SAMI)
- Windows Media Player Mobile,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Windows Media Player Controllo ActiveX mobile,Interscambio multimediale accessibile sincronizzato (SAMI)
- ActiveX,Synchronized Accessible Media Interchange (SAMI)
- Synchronized Accessible Media Interchange (SAMI), files
- SAMI (Synchronized Accessible Media Interchange),files
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f03d3e4079a117831ed8afb53648abf6a128ee
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880535"
---
# <a name="about-sami-files"></a>Informazioni sui file SAMI

I file SAMI sono file di testo con estensione smi o sami. Contengono le stringhe di testo usate per sottotitoli codificati sincronizzati, sottotitoli e descrizioni audio. Specificano anche i parametri di temporizzazione usati dal controllo Windows Media Player per sincronizzare il testo di sottotitoli codificati con contenuto audio o video. Quando un file multimediale digitale raggiunge un'ora designata nel file SAMI, il testo cambia di conseguenza nell'area di visualizzazione dei sottotitoli codificati della pagina Web.

Oltre a un semplice editor di testo (ad esempio Microsoft Blocco note), non è necessario software speciale per creare un file SAMI. SAMI e HTML condividono elementi comuni, ad esempio <HEAD> e &lt; i &gt; tag BODY. Come nel codice HTML, i tag usati nei file SAMI devono sempre essere usati in coppie. Ad esempio, un elemento BODY inizia con un tag BODY e &lt; &gt; deve sempre terminare con un tag &lt; &gt; /BODY.

Un file SAMI di base richiede tre tag fondamentali: &lt; SAMI &gt; , <HEAD>e &lt; BODY &gt; .

Il tag SAMI identifica il documento come documento SAMI in modo che &lt; &gt; altre applicazioni possano riconoscerne il formato di file.

Tra i due <HEAD> e </HEAD> tag, si definiscono linee guida di base e altre informazioni sul formato per il documento SAMI, ad esempio il titolo del documento, le informazioni generali e le proprietà di stile per i sottotitoli codificati. Come HTML, il contenuto dichiarato all'interno dell'elemento HEAD non viene visualizzato come output.

Gli elementi e gli attributi definiti tra i tag BODY e /BODY visualizzano &lt; &gt; il contenuto visualizzato &lt; &gt; dall'utente. In SAMI l'elemento BODY contiene i parametri per la sincronizzazione e le stringhe di testo usate per i sottotitoli codificati.

Definito all'interno dell'elemento HEAD, l'elemento STYLE fornisce funzionalità aggiuntive in SAMI. Tra i tag STYLE e , è possibile definire diversi selettori &lt; &gt; CSS </STYLE> (Cascading Style Sheet) per lo stile e il layout. Le proprietà di stile, ad esempio tipi di carattere, dimensioni e allineamenti, possono essere personalizzate per offrire un'esperienza utente ottimale, promuovendo al tempo stesso l'accessibilità. Ad esempio, la definizione di una classe di stile carattere di testo di grandi dimensioni può migliorare la leggibilità per gli utenti che hanno difficoltà a leggere testo di piccole dimensioni. Inoltre, definendo diverse classi linguistiche, è possibile aiutare gli utenti internazionali a comprendere meglio il contenuto multimediale digitale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Aggiunta di sottotitoli codificati ai supporti digitali**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




