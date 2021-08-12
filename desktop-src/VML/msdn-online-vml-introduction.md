---
title: Introduzione a VML
description: Introduzione a VML
ms.assetid: 8b603e95-3f02-47d6-9c5c-c781fa5d8459
keywords:
- Vector Markup Language (VML), informazioni di riferimento
- VML (Vector Markup Language),reference
- grafica vettoriale, informazioni di riferimento su VML
- grafica vettoriale, Vector Markup Language (VML)
- informazioni di riferimento Vector Markup Language (VML)
- Informazioni di riferimento su VML
- Vector Markup Language (VML),elemento Shape
- VML (Vector Markup Language),Elemento Shape
- grafica vettoriale, elemento Shape
- Elemento Shape
- Elementi VML, Forma
- Vector Markup Language (VML),VBScript
- VML (Vector Markup Language),VBScript
- Vector Markup Language (VML),Javascript
- VML (Vector Markup Language),Javascript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c694f87cab48a3f5da78db0e32ea576b889dbc3f6e49ba886c56d46b6ca244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600147"
---
# <a name="vml-introduction"></a>Introduzione a VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Questo documento fornisce un riferimento dettagliato completo all'implementazione del Vector Markup Language (VML) fornito con Microsoft Office 2000. Altre implementazioni possono variare. Per altre informazioni su VML come standard, vedere la specifica [VML.](https://www.w3.org/TR/NOTE-datetime.html)

VmL è definito come un set di elementi XML e gli attributi corrispondenti per ogni elemento. Poiché **l'elemento Shape** è il blocco predefinito di base di VML, fare clic [qui](shape-element--vml.md) per iniziare il riferimento.

Si noti che questo riferimento contiene diversi esempi e demo. Per visualizzare il vml live, è necessario che sia installato Microsoft Internet Explorer 5.0 o versione successiva.

Oltre alle informazioni sull'uso di elementi e attributi come tag XML che estendono HTML, questo riferimento contiene sintassi ed esempi che illustrano come usare gli script e le funzionalità Document Object Model di Internet Explorer 5 o versione successiva. L'uso di script con VML consente di creare elementi "in tempo reale" e modificare gli attributi in tempo reale.

Questo esempio in questo riferimento usa VBScript e JavaScript. Se si usa un linguaggio di scripting diverso da quello illustrato in un esempio, è necessario trovare la corrispondenza con la distinzione tra maiuscole e minuscole per tutti i nomi di elementi e attributi. Il riferimento fornisce una sintassi di scripting corretta per i linguaggi con distinzione tra maiuscole e minuscole, ad esempio JavaScript. In caso di dubbi sulla corretta distinzione tra maiuscole e minuscole, usare un visualizzatore oggetti (ad esempio OLEView) per esplorare il VGX.DLL per determinare la distinzione esatta tra maiuscole e minuscole di un elemento o di un attributo. Si noti che quando VML viene usato come tag XML, la distinzione tra maiuscole e minuscole dipende dal tipo di documento del documento sottostante. Se si usa una modalità strict , DOCTYPE, gli elementi e gli attributi fa distinzione tra maiuscole e minuscole.

[Informazioni di riferimento su VML](shape-element--vml.md)

 

 