---
description: Utilizzato per definire la topologia di trama di ogni faccia in un ritorno a capo. Il valore del membro nFaceWrapValues deve essere uguale al numero di visi in una mesh.
ms.assetid: f4aa356c-8f91-462f-9fc7-869b186b6c27
title: MeshFaceWraps
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9ba55db3dc2c0733d66f5a9e4589937258324b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520482"
---
# <a name="meshfacewraps"></a>MeshFaceWraps

Utilizzato per definire la topologia di trama di ogni faccia in un ritorno a capo. Il valore del membro nFaceWrapValues deve essere uguale al numero di visi in una mesh.

``` syntax
template MeshFaceWraps
{
    < ED1EC5C0-C0A8-11D0-941C-0080C80CFA7B >
    DWORD nFaceWrapValues;
    array Boolean2d faceWrapValues[nFaceWrapValues];
} 
```

Questo modello non viene più utilizzato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



