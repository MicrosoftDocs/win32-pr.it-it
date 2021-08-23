---
title: Appendice (VML)
description: Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Web workshop, spazi dei nomi
- Web workshop,stili di comportamento
- progettazione di pagine Web, spazi dei nomi
- progettazione di pagine Web, stili di comportamento
- Vector Markup Language (VML), spazi dei nomi
- VML (Vector Markup Language),spazi dei nomi
- grafica vettoriale, spazi dei nomi
- Vector Markup Language (VML), stili di comportamento
- VML (Vector Markup Language),stili di comportamento
- grafica vettoriale, stili di comportamento
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640de79138adcc345d4352ead814195007b88e0714a0f89816819d545e6e1ef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512611"
---
# <a name="appendix-vml"></a>Appendice (VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Per consentire ai browser di sapere come consegnare i dati a un processore specifico di VML, è necessario digitare alcune informazioni, ad esempio spazi dei nomi e stili di comportamento. È quindi possibile usare VML per digitare grafica `<BODY>` nell'area.

In questo argomento

-   [Namespaces](#namespaces) (Spazi dei nomi)
-   [Stili di comportamento](#behavior-styles)

## <a name="namespaces"></a>Spazi dei nomi

Un meccanismo XML indica lo spazio dei nomi da cui proviene un elemento. Se si passa dall'analisi in HTML all'analisi in XML, questo meccanismo indica il passaggio all'interno del codice HTML.

Chiedere al processore VML quali informazioni sono necessarie per lo spazio dei nomi XML.

Se si usa Microsoft Internet Explorer per eseguire il rendering di VML, digitare sempre la riga seguente nel `<HTML>` tag :


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



Queste informazioni Internet Explorer di passare allo spazio dei nomi "urn:schemas-microsoft-com:vml" durante l'analisi di un tag XML con un prefisso e di passare i dati risultanti al processore `v:` VML.

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="behavior-styles"></a>Stili di comportamento

VML è definito in Microsoft Internet Explorer come comportamento predefinito.

Per eseguire il rendering di VML, digitare sempre le righe `<HEAD>` seguenti nell'area:


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



VML viene implementato in Internet Explorer tramite VGX.DLL. Se l'installazione iniziale del browser non includeva il comportamento VML, potrebbe essere necessario aggiungerlo come opzione. Non è necessario aggiungere un `<object>` tag.

 

 
