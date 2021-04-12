---
description: Definisce un colore di materiale di base che può essere applicato a una mesh completa o ai singoli visi della mesh. La potenza è l'esponente speculare del materiale.
ms.assetid: vs|directx_sdk|~\material.htm
title: Materiale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480701"
---
# <a name="material"></a>Materiale

Definisce un colore di materiale di base che può essere applicato a una mesh completa o ai singoli visi della mesh. La potenza è l'esponente speculare del materiale.

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

-   faceColor-colore della faccia. Modello ColorRGBA. Vedere [**ColorRGBA**](colorrgba.md).
-   esponente di colore speculare del materiale di alimentazione.
-   specularColor-colore speculare materiale. Modello ColorRGB. Vedere [**ColorRGB**](colorrgb.md).
-   emissiveColor-colore emissivo materiale. Modello ColorRGB. Vedere [**ColorRGB**](colorrgb.md).

> [!Note]  
> Il colore di ambiente richiede un componente alfa.

 

[**TextureFilename**](texturefilename.md) è un oggetto dati facoltativo. Se questo oggetto non è presente, il volto è senza trame.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



