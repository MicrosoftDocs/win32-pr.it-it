---
description: Una mappa di rilievo è un oggetto IDirect3DTexture9 che usa un formato pixel specializzato.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Formati di pixel della mappa di rilievo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f627ce95151207c25e2365d2e467fb94b93cfb5c1bf54ce0c3df401891fcafc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805726"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a>Formati di pixel della mappa di rilievo (Direct3D 9)

Una mappa di rilievo è [**un oggetto IDirect3DTexture9**](/windows/desktop/api) che usa un formato pixel specializzato. Invece di archiviare i componenti di colore rosso, verde e blu, ogni pixel in una mappa di rilievo archivia i valori differenziali per l'utente e v (D<sub>U</sub> e D<sub>V)</sub>e talvolta un componente di luminance, L. Questi valori vengono applicati dal sistema come descritto [nell'argomento Bump Mapping Formulas (Direct3D 9) (Formule di bump mapping - Direct3D 9).](bump-mapping-formulas.md)

È possibile specificare un formato pixel mappa di rilievo impostando il formato su uno dei seguenti: D3DFMT \_ CxV8U8, \_ D3DFMT V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8V8U8, D3DFMT \_ Q8W8V8U8 o D3DFMT \_ V16U16. Per le descrizioni, vedere [D3DFORMAT.](d3dformat.md)

I componenti D<sub>U</sub> e D<sub>V</sub> di un pixel sono valori con segno che vanno da - 1.0 a +1.0. Il componente luminance, se usato, è un valore intero senza segno compreso tra 0 e 255.

> [!Note]  
> Prima di selezionare un formato pixel della mappa di rilievo, verificare se il formato specifico è supportato. Per altre informazioni, vedere [Using Bump Mapping (Direct3D 9) (Uso di Bump Mapping (Direct3D 9)](using-bump-mapping.md)).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bump Mapping](bump-mapping.md)
</dt> </dl>

 

 



