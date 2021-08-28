---
description: Flag di funzionalità del driver.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb3ed10a4a12602e8586bbd0e941641287346a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627997"
---
# <a name="d3denum"></a>D3DENUM

Flag di funzionalità del driver.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definire</td>
<td>Valore</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DENUM_WHQL_LEVEL</td>
<td>0x00000002L</td>
<td>Test del driver Microsoft Windows Hardware Quality Labs (WHQL). Si tratta di un test dispendioso in termini di tempo che richiede una penalità di un secondo o di due secondi. Questa costante viene usata dal membro WHQLLevel <a href="d3dadapter-identifier9.md"><strong>di D3DADAPTER_IDENTIFIER9</strong></a>.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> D3DENUM_WHQL_LEVEL è deprecato per Direct3D9Ex in esecuzione in Windows Vista, Windows Server 2008, Windows 7 e Windows Server 2008 R2 (o più sistema operativo corrente). Uno di questi sistemi operativi restituisce 1 per il livello WHQL senza controllare lo stato del driver. <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a>Informazioni costanti



| Requisito                         | Valore           |
|--------------------------|------------|
| Intestazione                   | d3d9.h     |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




