---
description: Usato in un oggetto mesh per specificare il materiale da applicare ai visi. Il membro nMaterials specifica quanti materiali sono presenti e i materiali specificano il materiale da applicare.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ef1d200e5f6a6913f996c186e121a8390de01e8f3347b6dcbaeac8eeefa708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798787"
---
# <a name="meshmateriallist"></a>MeshMaterialList

Usato in un oggetto mesh per specificare il materiale da applicare ai visi. Il membro nMaterials specifica quanti materiali sono presenti e i materiali specificano il materiale da applicare.

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

-   nMaterials: valore DWORD. Numero di materiali.
-   nFaceIndexes: valore DWORD. Numero di indici.
-   faceIndexes \[ nFaceIndexes: \] matrice di valori DWORD contenente gli indici del viso.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



