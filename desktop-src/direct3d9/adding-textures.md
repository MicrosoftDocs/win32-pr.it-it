---
description: Per aggiungere trame, usare la natura gerarchica del formato di file e aggiungere un oggetto dati TextureFilename facoltativo agli oggetti dati Material.
ms.assetid: 741f4c05-49f8-4c76-be5c-ce5b496124bb
title: Aggiunta di trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee0090b5990c2093a41efbd15eb998401ce2607
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126162"
---
# <a name="adding-textures-direct3d-9"></a>Aggiunta di trame (Direct3D 9)

Per aggiungere trame, usare la natura gerarchica del formato di file e aggiungere un oggetto dati [**TextureFilename**](texturefilename.md) facoltativo agli oggetti dati [**Material**](material.md) . Gli oggetti **Material** sono ora letti come segue:


```
Material RedMaterial {
1.000000;0.000000;0.000000;1.000000;;    // R = 1.0, G = 0.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "tex1.ppm"; }
}

Material GreenMaterial {
0.000000;1.000000;0.000000;1.000000;;     // R = 0.0, G = 1.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "win95.ppm"; }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[File X (legacy)](x-files--legacy-.md)
</dt> </dl>

 

 



