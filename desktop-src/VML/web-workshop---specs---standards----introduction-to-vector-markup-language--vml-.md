---
title: Vector Markup Language (VML)
description: Vector Markup Language (VML)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Vector Markup Language (VML), informazioni
- VML (Vector Markup Language),about
- grafica vettoriale, informazioni
- grafica vettoriale, Vector Markup Language (VML)
- Vector Markup Language (VML), World Wide Web Consortium (W3C)
- VML (Vector Markup Language), World Wide Web Consortium (W3C)
- grafica vettoriale, World Wide Web Consortium (W3C)
- grafica vettoriale, vantaggi di VML
- Vector Markup Language (VML), vantaggi
- VML (Vector Markup Language),benefits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6199b481c58bbc5cd769ba43e614f21ae0105b4ef703858b559cdd76ff5516bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596067"
---
# <a name="vector-markup-language-vml"></a>Vector Markup Language (VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!NOTE]
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

Vector Markup Language (VML) è un formato di scambio, modifica e distribuzione basato su XML per la grafica vettoriale di alta qualità sul Web che soddisfa le esigenze degli utenti della produttività e dei professionisti della progettazione grafica. XML è un linguaggio emergente basato su testo semplice, flessibile e aperto che integra il linguaggio HTML. Per informazioni dettagliate [su XML,](/documentation/?frame=true) vedere la sezione XML di MSDN Library.

VML è attualmente supportato da Microsoft Internet Explorer versione 5.0 o successiva.

VmL è stato proposto al W3C come standard per la grafica vettoriale sul Web (vedere [Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-VML)). Microsoft continua a guidare lo sviluppo e l'implementazione di tecnologie basate su XML, collaborando con i principali partner del settore (AutoDesk, Hewlett-Packard, Macromedia, Visio) e W3C per promuovere gli standard basati sul Web. Si prevede di usare W3C per ottenere un formato standard per la grafica vettoriale sul Web.

VML è supportato anche da Microsoft Office 2000 o versioni successive. Microsoft Word, Microsoft Excel e Microsoft PowerPoint possono essere usati per creare grafica VML.

### <a name="using-vml"></a>Uso di VML

Per usare VML nelle pagine Web, usare un elemento di stile per importare il comportamento vml, come illustrato nel codice seguente.

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

Dichiarare quindi lo spazio dei nomi VML, come illustrato nell'esempio di codice seguente.

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

Infine, aggiungere elementi VML per definire gli effetti visivi. Ad esempio, il codice VML seguente crea un ovale rosso.

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> Per ottenere risultati ottimali quando si usano documenti in modalità strict, assicurarsi che il markup sia valido e ben formato. Per altre informazioni, vedere l'oggetto . Pagina di riferimento DOCTYPE.


### <a name="benefits-of-vml"></a>Vantaggi di VML

-   VML semplifica la creazione per utenti e autori di produttività. Facilita lo scambio (tramite taglia e incolla) e la successiva modifica della grafica vettoriale tra un'ampia gamma di applicazioni di produttività e progettazione.
-   VML offre download grafici più veloci e una migliore esperienza utente. Consente la distribuzione di grafica vettoriale di alta qualità, completamente integrata e scalabile al Web, in un formato aperto basato su testo. Invece di fare riferimento alla grafica come file esterni, la grafica VML viene recapitata inline con la pagina HTML, consentendo loro di interagire e ridimensionare con l'interazione dell'utente.
-   VML è aperto e basato su standard. Si tratta di un formato basato su XML. XML 1.0 è un linguaggio aperto, semplice e basato su testo per la descrizione dei dati strutturati sul Web e integra il codice HTML per la visualizzazione. VML supporta anche altri standard W3C, ad esempio Cascading Style Sheets 2.0 (CSS), che specifica informazioni di stile e posizionamento 2D, nonché Document Object Model (DOM), che consente agli sviluppatori di interagire in modo coerente con gli elementi della pagina come oggetti.

### <a name="for-additional-information"></a>Per altre informazioni

Vedere i collegamenti seguenti:

-   Per le risposte alle domande frequenti su VML, vedere le [domande frequenti su VML.](frequently-asked-questions-about-vml.yml)
-   Per un'esercitazione sull'uso di VML nelle pagine Web, vedere [How to Use VML on Web Pages](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)(Come usare VML nelle pagine Web), che integra la specifica [VML](https://www.w3.org/TR/NOTE-datetime.html) inviata al W3C.
-   Per informazioni sui tipi di dati VML, vedere il [documento Tipi VML di](basic-vml-types.md) base.
-   Per informazioni di riferimento complete su VML, incluse informazioni su come usare VML con tag e script, vedere riferimento [a VML](msdn-online-vml-introduction.md).