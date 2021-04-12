---
description: Viene creata un'istanza di questo modello in base a mesh solo in mesh che contengono informazioni di skinning esportate. Lo scopo di questo modello è fornire informazioni sulla natura delle informazioni di skinning esportate.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306f8c183086846fca020040af00b9ccef2665cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401291"
---
# <a name="xskinmeshheader"></a>XSkinMeshHeader

Viene creata un'istanza di questo modello in base a mesh solo in mesh che contengono informazioni di skinning esportate. Lo scopo di questo modello è fornire informazioni sulla natura delle informazioni di skinning esportate.

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

Dove:

-   nMaxSkinWeightsPerVertex: numero massimo di trasformazioni che interessano un vertice nella mesh.
-   nMaxSkinWeightsPerFace: numero massimo di trasformazioni univoche che interessano i tre vertici di qualsiasi faccia.
-   nBones: numero di ossa che interessano i vertici in questa mesh.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



