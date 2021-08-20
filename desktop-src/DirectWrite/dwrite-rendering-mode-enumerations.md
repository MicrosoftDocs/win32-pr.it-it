---
title: DWRITE_RENDERING_MODE di dati
description: A partire da Windows 8, l'enumerazione DWRITE \_ RENDERING MODE ha aggiunto nuovi valori di enumerazione e ne ha \_ deprecati altri.
ms.assetid: 3EA568B4-310D-4F70-9530-5916419282E5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1b44de30c50aab1015c0fefa3515e3cc9c9281df41b641b3bc96ce231c4567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816639"
---
# <a name="dwrite_rendering_mode-enumerations"></a>Enumerazioni DWRITE \_ RENDERING \_ MODE

A partire da Windows 8, **l'enumerazione DWRITE \_ RENDERING \_ MODE** ha aggiunto nuovi valori di enumerazione e ne ha deprecati altri.

A partire da Windows 8, [**l'enumerazione DWRITE \_ TEXT \_ ANTIALIAS \_ MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) determina se il rendering del testo viene eseguito tramite ClearType. Di conseguenza, tutte le modalità di rendering ClearType **nell'enumerazione DWRITE \_ RENDERING \_ MODE** sono deprecate. Questi valori di enumerazione vengono ora mappati alle nuove modalità di rendering.

La tabella seguente mostra i valori di enumerazione precedente e i nuovi valori a cui sono mappati. Per le descrizioni dei nuovi valori, vedere [**DWRITE \_ RENDERING \_ MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).



| Modalità precedente                                                                                | Nuova modalità                                                                                |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**MODALITÀ DI RENDERING DWRITE \_ \_ \_ CLEARTYPE \_ GDI \_ CLASSIC**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [**MODALITÀ DI RENDERING DWRITE \_ \_ \_ GDI \_ CLASSIC**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [**MODALITÀ DI RENDERING DWRITE \_ \_ \_ CLEARTYPE \_ GDI \_ NATURAL**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [**DWRITE \_ RENDERING \_ MODE \_ GDI \_ NATURAL**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [**MODALITÀ DI RENDERING DWRITE \_ \_ \_ CLEARTYPE \_ NATURAL**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            | [**MODALITÀ DI RENDERING DWRITE \_ \_ \_ CLEARTYPE \_ NATURAL**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            |
| [**MODALITÀ DI RENDERING DWRITE \_ \_ \_ CLEARTYPE \_ NATURAL \_ SYMMETRIC**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) | [**MODALITÀ DI RENDERING DWRITE \_ \_ \_ CLEARTYPE \_ NATURAL \_ SYMMETRIC**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) |



 

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE (Windows 8 e versioni successive)</strong></a><br/></td>
<td>Rappresenta un metodo di rendering dei glifi. <br/>
<blockquote>
[!Note]<br />
Questo argomento illustra le <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> in Windows 8 e versioni successive. Per informazioni sulla versione precedente, vedere <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>questo argomento.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a><br/></td>
<td>Rappresenta un metodo di rendering dei glifi. <br/>
<blockquote>
[!Note]<br />
Questo argomento riguarda le <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> precedenti a Windows 8 e versioni successive. Per informazioni sulla versione più recente, vedere <strong>questo argomento.</strong>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 





