---
description: Viene creata un'istanza di questo modello per ogni mesh solo nelle mesh che contengono informazioni di skinning esportate. Lo scopo di questo modello è fornire informazioni sulla natura delle informazioni di skinning esportate.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c86127e46809cd1415b191a769b25e09535405e6500e511df6248e6174888d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796855"
---
# <a name="xskinmeshheader"></a>XSkinMeshHeader

Viene creata un'istanza di questo modello per ogni mesh solo nelle mesh che contengono informazioni di skinning esportate. Lo scopo di questo modello è fornire informazioni sulla natura delle informazioni di skinning esportate.

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
-   nMaxSkinWeightsPerFace: numero massimo di trasformazioni univoche che influiscono sui tre vertici di qualsiasi viso.
-   nBones : numero di esche che influiscono sui vertici in questa mesh.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



