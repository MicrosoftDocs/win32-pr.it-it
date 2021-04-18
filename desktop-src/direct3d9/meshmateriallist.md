---
description: Utilizzato in un oggetto mesh per specificare il materiale da applicare ai visi. Il membro nMaterials specifica il numero di materiali presenti e i materiali specificano il materiale da applicare.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b746802dc3ef54a8feacc8ddfdaa0db1e45112b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303721"
---
# <a name="meshmateriallist"></a>MeshMaterialList

Utilizzato in un oggetto mesh per specificare il materiale da applicare ai visi. Il membro nMaterials specifica il numero di materiali presenti e i materiali specificano il materiale da applicare.

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

Dove:

-   nMaterials-un valore DWORD. Il numero di materiali.
-   nFaceIndexes-un valore DWORD. Numero di indici.
-   faceIndexes \[ nFaceIndexes \] : matrice di DWORD contenenti gli indici dei volti.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



