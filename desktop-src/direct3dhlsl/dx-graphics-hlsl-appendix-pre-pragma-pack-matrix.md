---
title: pack_matrix direttiva pragma
description: Direttiva pragma che specifica l'allineamento di compressione per le matrici.
ms.assetid: e77dc007-d915-4d78-9fff-d44d4999e4da
keywords:
- pack_matrix direttiva pragma HLSL
topic_type:
- apiref
api_name:
- pack_matrix pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4bb5474702a1caba3f772002c34677601715caff
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045739"
---
# <a name="pack_matrix-pragma-directive"></a>Pack \_ matrice pragma (direttiva)

Direttiva pragma che specifica l'allineamento di compressione per le matrici.



| \#tabella pragma pack \_ ( *Alignment* ) |
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
<td><span id="alignment"></span><span id="ALIGNMENT"></span><em>allineamento</em><br/></td>
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
<td>Valore predefinito. Imposta l'allineamento della compressione della matrice sulla colonna Major.</td>
</tr>
<tr class="even">
<td>row_major</td>
<td>Imposta l'allineamento della compressione della matrice sulla riga principale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene impostato l'allineamento della compressione della matrice sulla riga principale.


```
#pragma pack_matrix( row_major )
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#pragma (direttiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





