---
description: Una mappa Bump è un oggetto IDirect3DTexture9 che usa un formato pixel specializzato.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Formati di pixel della mappa Bump (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049253"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a>Formati di pixel della mappa Bump (Direct3D 9)

Una mappa Bump è un oggetto [**IDirect3DTexture9**](/windows/desktop/api) che usa un formato pixel specializzato. Anziché archiviare i componenti di colore rosso, verde e blu, ogni pixel in una mappa Bump archivia i valori delta per l'utente e v (D<sub>U</sub> e d<sub>v</sub>) e talvolta un componente di luminanza, L. Questi valori vengono applicati dal sistema come descritto nell'argomento relativo alle [formule di mapping Bump (Direct3D 9)](bump-mapping-formulas.md) .

È possibile specificare un formato pixel di mappa a urto impostando il formato su uno dei seguenti elementi: D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT X8L8V8U8, \_ D3DFMT \_ Q8W8V8U8 o D3DFMT V16U16 \_ . Per le descrizioni, vedere [D3DFORMAT](d3dformat.md).

I componenti D<sub>U</sub> e d<sub>V</sub> di un pixel sono valori con segno compreso tra-1,0 e + 1,0. Il componente luminanza, se usato, è un valore Unsigned Integer compreso tra 0 e 255.

> [!Note]  
> Prima di selezionare un formato pixel per la mappa Bump, verificare che il formato specifico sia supportato. Per altre informazioni, vedere [uso di bump mapping (Direct3D 9)](using-bump-mapping.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bump mapping](bump-mapping.md)
</dt> </dl>

 

 



