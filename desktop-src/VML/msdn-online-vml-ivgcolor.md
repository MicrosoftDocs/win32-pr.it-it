---
title: VML IVgColor
description: VML IVgColor
ms.assetid: 6121c5bf-1969-4402-9f45-8891a1538fea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97093d9e9315db1389c71db7e8e21fdbf640353c95c5cf11f607c708e1679166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599516"
---
# <a name="vml-ivgcolor"></a>VML IVgColor

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. È necessario eseguire la migrazione di pagine Web e applicazioni basate su VML a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, raccomandazioni e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center](https://msdn.microsoft.com/ie/).

 

Specifica un colore.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributi</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>string</td>
<td>Stringa. Rappresentazione testuale del colore. Sono supportati i tipi di colore denominati seguenti:
<ul>
<li>Nero (#000000)</li>
<li>Silver (#C0C0C0)</li>
<li>Grigio (#808080)</li>
<li>Bianco (#FFFFFF)</li>
<li>Maroon (#800000)</li>
<li>Rosso (#FF0000)</li>
<li>Viola (#800080)</li>
<li>Fucsia (#FF00FF)</li>
<li>Verde (#008000)</li>
<li>Lime (#00FF00)</li>
<li>Olive (#808000)</li>
<li>Giallo (#FFFF00)</li>
<li>Flotta (#000080)</li>
<li>Blu (#0000FF)</li>
<li>Teal (#008080)</li>
<li>Aqua (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>VgColorType. Tipo di colore. Uno dei tipi seguenti:
<ul>
<li>Mixed</li>
<li>RGB</li>
<li>Schema</li>
<li>denominata</li>
</ul></td>
</tr>
<tr class="odd">
<td>RGB</td>
<td>VgRGBType. Valore RGB (<strong>Long</strong>) del colore. Valido solo se Type è &quot; <strong>RGB.</strong> &quot;</td>
</tr>
<tr class="even">
<td>R</td>
<td><strong>Integer</strong>. Componente rosso del colore. Può essere compreso tra 0 e 255.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><strong>Integer</strong>. Componente verde del colore. Può essere compreso tra 0 e 255.</td>
</tr>
<tr class="even">
<td>B</td>
<td><strong>Integer</strong>. Componente blu del colore. Può essere compreso tra 0 e 255.</td>
</tr>
</tbody>
</table>



 

 

 