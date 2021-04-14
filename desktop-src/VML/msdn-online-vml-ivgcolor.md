---
title: IVgColor la
description: IVgColor la
ms.assetid: 6121c5bf-1969-4402-9f45-8891a1538fea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d4800fbb99557acfbd3fd6e0dbbd893f30158f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473462"
---
# <a name="vml-ivgcolor"></a>IVgColor la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

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
<td>Stringa. Rappresentazione testuale del colore. Sono supportati i seguenti tipi di colori denominati:
<ul>
<li>Nero (#000000)</li>
<li>Argento (#C0C0C0)</li>
<li>Grigio (#808080)</li>
<li>Bianco (#FFFFFF)</li>
<li>Marrone (#800000)</li>
<li>Rosso (#FF0000)</li>
<li>Viola (#800080)</li>
<li>Fucsia (#FF00FF)</li>
<li>Verde (#008000)</li>
<li>Lime (#00FF00)</li>
<li>Olive (#808000)</li>
<li>Giallo (#FFFF00)</li>
<li>Navy (#000080)</li>
<li>Blu (#0000FF)</li>
<li>Verde acqua (#008080)</li>
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
<td>VgRGBType. Valore RGB (<strong>Long</strong>) del colore. Valido solo se il tipo è &quot; <strong>RGB</strong> &quot; .</td>
</tr>
<tr class="even">
<td>R</td>
<td><strong>Integer</strong>. Componente rosso del colore. Può variare da 0 a 255.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><strong>Integer</strong>. Componente verde del colore. Può variare da 0 a 255.</td>
</tr>
<tr class="even">
<td>B</td>
<td><strong>Integer</strong>. Componente blu del colore. Può variare da 0 a 255.</td>
</tr>
</tbody>
</table>



 

 

 