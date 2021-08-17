---
title: direttiva pragma pack_matrix
description: Direttiva pragma che specifica l'allineamento di tabulazione per le matrici.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix pragma HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c12129b6840197b21d1d259cc13bd07e75620176bdc797e6828c10d71e1c95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514784"
---
# <a name="pack_matrix-pragma-directive"></a>Direttiva pragma \_ pack matrix

Direttiva pragma che specifica l'allineamento di tabulazione per le matrici.



| \#pragma pack \_ matrix( *alignment* ) |
|--------------------------------------|



 

## <a name="parameters"></a>Parametri



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="alignment"></span><span id="ALIGNMENT"></span><em>Allineamento</em><br/></td>
<td>Allineamento da impostare per le matrici. Questo parametro può assumere uno dei valori elencati nella tabella seguente. <br/> 
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>column_major</td>
<td>Valore predefinito. Imposta l'allineamento di tabulazione della matrice sulla colonna principale.</td>
</tr>
<tr class="even">
<td>row_major</td>
<td>Imposta l'allineamento di tabulazione della matrice su row major.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene impostato l'allineamento dei caratteri di tabulazione della matrice su row major.


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Direttiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





