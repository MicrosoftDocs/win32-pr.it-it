---
description: Costanti di generazione normali delle mappe.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4263237cedf92a5e322f2fe139e9afe2297f6b9b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342856"
---
# <a name="d3dx_normalmap"></a>D3DX \_ NORMALMAP

Costanti di generazione normali delle mappe.



| \#Definire                            | Descrizione                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ NORMALMAP \_ MIRROR \_ U          | Indica che i pixel al di fuori del bordo della trama sull'asse u devono essere speculari, senza eseguire il wrapping.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR \_ V          | Indica che è necessario eseguire il mirroring dei pixel al di fuori del bordo della trama sull'asse v, senza eseguire il wrapping.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR             | Come specificare D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.                                                                                                                       |
| D3DX \_ NORMALMAP \_ INVERTSIGN         | Inverte la direzione di ogni normale.                                                                                                                                                              |
| OCCLUSIONE DI CALCOLO D3DX \_ NORMALMAP \_ \_ | Calcola il termine di occlusione per pixel e lo codifica in alfa. Un valore alfa 1 indica che il pixel non viene nascosto in alcun modo e un valore alfa 0 indica che il pixel è completamente nascosto. |



 

## <a name="constant-information"></a>Informazioni costanti



| Requisito                         | Valore           |
|--------------------------|------------|
| Intestazione                   | d3dx9tex.h |
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[**D3DXComputeNormalMap**](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



