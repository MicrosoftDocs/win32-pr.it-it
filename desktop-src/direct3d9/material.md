---
description: Definisce un colore di materiale di base che può essere applicato a una mesh completa o ai singoli visi di una mesh. La potenza è l'esponente speculare del materiale.
ms.assetid: vs|directx_sdk|~\material.htm
title: Materiale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d4dcb1cef7597ff7c02d16f1db311287511166c9259c89a0ea60a0c49fb7bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798968"
---
# <a name="material"></a>Materiale

Definisce un colore di materiale di base che può essere applicato a una mesh completa o ai singoli visi di una mesh. La potenza è l'esponente speculare del materiale.

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

Dove:

-   faceColor: colore del viso. Un modello ColorRGBA. Vedere [**ColorRGBA.**](colorrgba.md)
-   power : esponente di colore speculare materiale.
-   specularColor: colore speculare materiale. Un modello ColorRGB. Vedere [**ColorRGB.**](colorrgb.md)
-   emissiveColor: colore emissivo materiale. Un modello ColorRGB. Vedere [**ColorRGB.**](colorrgb.md)

> [!Note]  
> Il colore di ambiente richiede un componente alfa.

 

[**TextureFilename è**](texturefilename.md) un oggetto dati facoltativo. Se questo oggetto non è presente, il viso non viene visualizzato come testo.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



