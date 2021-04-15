---
title: Appendice (la)
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Workshop Web, spazi dei nomi
- Workshop Web, stili di comportamento
- progettazione di pagine Web, spazi dei nomi
- progettazione di pagine Web, stili di comportamento
- Vector Markup Language (la), spazi dei nomi
- LA (Vector Markup Language), spazi dei nomi
- grafica vettoriale, spazi dei nomi
- Vector Markup Language (la), stili di comportamento
- LA (Vector Markup Language), stili di comportamento
- grafica vettoriale, stili di comportamento
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d4e7a6a7e44671b7ee835eea263d9ce36a27d8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400135"
---
# <a name="appendix-vml"></a>Appendice (la)

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Per fare in modo che i browser sappiano come passare i dati a un processore specifico di la, è necessario digitare alcune informazioni, ad esempio gli spazi dei nomi e gli stili di comportamento. È quindi possibile usare la per digitare elementi grafici nell' `<BODY>` area.

In questo argomento

-   [Namespaces](#namespaces) (Spazi dei nomi)
-   [Stili di comportamento](#behavior-styles)

## <a name="namespaces"></a>Spazi dei nomi

Un meccanismo XML indica lo spazio dei nomi da cui deriva un elemento. Se si passa dall'analisi in HTML all'analisi in XML, questo meccanismo indica l'opzione all'interno del linguaggio HTML.

Chiedere al fornitore del processore la quali informazioni sono necessarie per lo spazio dei nomi XML.

Se si utilizza Microsoft Internet Explorer per eseguire il rendering di la, digitare sempre la riga seguente nel `<HTML>` Tag:


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



Queste informazioni indicano a Internet Explorer di passare allo spazio dei nomi "urn: schemas-microsoft-com: la" durante l'analisi di un tag XML con un prefisso `v:` e di passare i dati risultanti al processore la.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="behavior-styles"></a>Stili di comportamento

LA è definito in Microsoft Internet Explorer come comportamento predefinito.

Per eseguire il rendering di la, digitare sempre le righe seguenti nell' `<HEAD>` area:


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



LA viene implementato in Internet Explorer tramite VGX.DLL. Se l'installazione iniziale del browser non include il comportamento di la, potrebbe essere necessario aggiungerlo come opzione. Non è necessario aggiungere un `<object>` tag.

 

 
