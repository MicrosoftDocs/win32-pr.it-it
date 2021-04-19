---
title: Vector Markup Language (la)
description: Vector Markup Language (la)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Vector Markup Language (la), informazioni
- LA (Vector Markup Language), informazioni
- grafica vettoriale, informazioni
- grafica vettoriale, Vector Markup Language (la)
- Vector Markup Language (la), World Wide Web Consortium (W3C)
- LA (Vector Markup Language), World Wide Web Consortium (W3C)
- grafica vettoriale, World Wide Web Consortium (W3C)
- grafica vettoriale, vantaggi la
- Vector Markup Language (la), vantaggi
- LA (Vector Markup Language), vantaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ba51fd041f36915eaafe20201876653f597e04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320317"
---
# <a name="vector-markup-language-vml"></a>Vector Markup Language (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!NOTE]
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

Vector Markup Language (la) è un formato basato su XML per lo scambio, la modifica e il recapito per la grafica vettoriale di alta qualità sul Web che soddisfa le esigenze di utenti di produttività e professionisti di progettazione grafica. XML è un linguaggio basato su testo semplice, flessibile e aperto che integra il codice HTML. Per informazioni dettagliate su XML, vedere la [sezione XML](/documentation/?frame=true) di MSDN Library.

LA è attualmente supportato da Microsoft Internet Explorer versione 5,0 o successiva.

LA è stato proposto al W3C come standard per la grafica vettoriale sul Web (vedere [Vector Markup Language (la)](https://www.w3.org/TR/NOTE-VML)). Microsoft sta continuando a sostenere l'addebito per lo sviluppo e l'implementazione di tecnologie basate su XML, collaborando con i principali partner del settore (AutoDesk, Hewlett-Packard, Macromedia, Visio) e W3C per promuovere gli standard basati sul Web. Si prevede di usare il W3C per eseguire la trasmissione in un formato standard per la grafica vettoriale sul Web.

LA è supportato anche da Microsoft Office 2000 o versione successiva. Microsoft Word, Microsoft Excel e Microsoft PowerPoint possono essere usati per creare grafica la.

### <a name="using-vml"></a>Uso di la

Per usare la nelle pagine Web, usare un elemento Style per importare il comportamento di la, come illustrato nel codice seguente.

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

Dichiarare quindi lo spazio dei nomi la, come illustrato nell'esempio di codice seguente.

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

Infine, aggiungere gli elementi la per definire gli effetti degli oggetti visivi. Ad esempio, il codice la seguente crea un ovale rosso.

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> Per ottenere risultati ottimali quando si usano i documenti in modalità Strict, assicurarsi che il markup sia valido e ben formato. Per ulteriori informazioni, vedere. Pagina di riferimento DOCTYPE.


### <a name="benefits-of-vml"></a>Vantaggi di la

-   LA semplifica la creazione di utenti e autori della produttività. Semplifica lo scambio (tramite taglia e incolla) e la successiva modifica della grafica vettoriale tra una vasta gamma di applicazioni di produttività e progettazione.
-   LA fornisce download grafici più veloci e un'esperienza utente migliore. Consente la distribuzione di una grafica vettoriale scalabile, completamente integrata e di alta qualità sul Web, in un formato basato su testo aperto. Anziché fare riferimento a elementi grafici come file esterni, i grafici la vengono forniti inline con la pagina HTML, consentendo loro di interagire e ridimensionarsi con l'interazione dell'utente.
-   LA è aperto e basato su standard. Si tratta di un formato basato su XML. XML 1,0 è un linguaggio aperto, semplice e basato su testo per la descrizione dei dati strutturati sul Web e integra il codice HTML per la visualizzazione. LA supporta anche altri standard W3C, ad esempio Cascading Style Sheets 2,0 (CSS), che specifica le informazioni sullo stile e il posizionamento 2D, nonché il Document Object Model (DOM), che consente agli sviluppatori di interagire in modo coerente con gli elementi della pagina come oggetti.

### <a name="for-additional-information"></a>Per ulteriori informazioni

Vedere i collegamenti seguenti:

-   Per le risposte alle domande più frequenti su la, vedere le domande [frequenti su la](frequently-asked-questions-about-vml.md).
-   Per un'esercitazione sull'uso di la nelle pagine Web, vedere [How to use la on Web Pages](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), che è complementare alla [specifica la](https://www.w3.org/TR/NOTE-datetime.html) inviata a W3C.
-   Per informazioni sui tipi di dati la, vedere il documento di [base sui tipi di la](basic-vml-types.md) .
-   Per informazioni di riferimento complete su la, incluse informazioni su come usare la con tag e scripting, vedere la Guida di [riferimento a la](msdn-online-vml-introduction.md).