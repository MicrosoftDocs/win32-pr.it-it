---
title: Enumerazioni di DWRITE_RENDERING_MODE
description: A partire da Windows 8, l' \_ enumerazione della modalità di rendering DWrite ha \_ aggiunto nuovi valori di enumerazione e ne è stato deprecato altri.
ms.assetid: 3EA568B4-310D-4F70-9530-5916419282E5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fa79cf34a03960ddb42a8a80221e99d47be847
ms.sourcegitcommit: d1b8f5ed3d6e35e93cb254efc49428a072d7ef9a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/12/2019
ms.locfileid: "103955038"
---
# <a name="dwrite_rendering_mode-enumerations"></a>\_Enumerazioni della modalità di rendering DWrite \_

A partire da Windows 8, l'enumerazione della **\_ \_ modalità di rendering DWrite** ha aggiunto nuovi valori di enumerazione e ne è stato deprecato altri.

A partire da Windows 8, l'enumerazione [**DWrite \_ Text \_ antialias \_ mode**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode) determina se il rendering del testo viene eseguito con ClearType. Di conseguenza, tutte le modalità di rendering ClearType nell'enumerazione **della \_ \_ modalità di rendering DWrite** sono deprecate. Questi valori di enumerazione ora vengono mappati alle nuove modalità di rendering.

La tabella seguente mostra i valori di enumerazione precedenti e i nuovi valori a cui viene eseguito il mapping. Per le descrizioni dei nuovi valori, vedere [**\_ \_ modalità di rendering DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode).



| Modalità precedente                                                                                | Nuova modalità                                                                                |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DWRITE \_ modalità di rendering \_ \_ CLEARTYPE \_ GDI \_ classico**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [**\_modalità di rendering DWrite \_ \_ GDI \_ classico**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [**\_modalità di rendering DWrite \_ \_ CLEARTYPE \_ GDI \_ naturale**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)       | [**\_modalità di rendering DWrite \_ \_ GDI \_ Natural**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)                  |
| [**DWRITE \_ modalità di rendering \_ \_ CLEARTYPE \_ naturale**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            | [**DWRITE \_ modalità di rendering \_ \_ CLEARTYPE \_ naturale**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)            |
| [**\_modalità di rendering DWrite \_ \_ CLEARTYPE \_ naturale \_ simmetrica**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) | [**\_modalità di rendering DWrite \_ \_ CLEARTYPE \_ naturale \_ simmetrica**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode) |



 

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
Questo argomento riguarda <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> in Windows 8 e versioni successive. Per informazioni sulla versione precedente, vedere <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>questo argomento</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a><br/></td>
<td>Rappresenta un metodo di rendering dei glifi. <br/>
<blockquote>
[!Note]<br />
Questo argomento riguarda <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode"><strong>DWRITE_RENDERING_MODE</strong></a> precedente a Windows 8 e versioni successive. Per informazioni sulla versione più recente, vedere <strong>questo argomento</strong>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 





