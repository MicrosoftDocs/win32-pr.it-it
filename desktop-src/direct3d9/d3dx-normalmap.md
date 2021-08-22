---
description: Costanti normali per la generazione di mappe.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d3a3d2f35fa409e4432dd7600cb544df25110d10aa9af7f5ee18fd622ea1309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374951"
---
# <a name="d3dx_normalmap"></a>D3DX \_ NORMALMAP

Costanti normali per la generazione di mappe.



| \#Definire                            | Descrizione                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DX \_ NORMALMAP \_ MIRROR \_ U          | Indica che i pixel all'esterno del bordo della trama sull'asse u devono essere speculari, senza ritorno a capo.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR \_ V          | Indica che è necessario eseguire il mirroring dei pixel all'esterno del bordo della trama sull'asse v, senza eseguire il wrapping.                                                                                                   |
| D3DX \_ NORMALMAP \_ MIRROR             | Uguale alla specifica di D3DX \_ NORMALMAP \_ MIRROR U \_ \| D3DX \_ NORMALMAP MIRROR \_ \_ V.                                                                                                                       |
| D3DX \_ NORMALMAP \_ INVERTSIGN         | Inverte la direzione di ogni normale.                                                                                                                                                              |
| OCCLUSIONE CALCOLO D3DX \_ NORMALMAP \_ \_ | Calcola il termine di occlusione per pixel e lo codifica in alfa. Un valore alfa di 1 indica che il pixel non viene nascosto in alcun modo e un valore alfa 0 indica che il pixel è completamente nascosto. |



 

## <a name="constant-information"></a>Informazioni sulle costanti



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

 

 



