---
description: Usato per definire la topologia di trama di ogni viso in un ritorno a capo. Il valore del membro nFaceWrapValues deve essere uguale al numero di visi in una mesh.
ms.assetid: f4aa356c-8f91-462f-9fc7-869b186b6c27
title: MeshFaceWraps
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0878754b9e9e58e0f508be26ab30ac44112b1a2e8d8ba0f7e597591b2ebdab81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746971"
---
# <a name="meshfacewraps"></a>MeshFaceWraps

Usato per definire la topologia di trama di ogni viso in un ritorno a capo. Il valore del membro nFaceWrapValues deve essere uguale al numero di visi in una mesh.

``` syntax
template MeshFaceWraps
{
    < ED1EC5C0-C0A8-11D0-941C-0080C80CFA7B >
    DWORD nFaceWrapValues;
    array Boolean2d faceWrapValues[nFaceWrapValues];
} 
```

Questo modello non viene più usato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



