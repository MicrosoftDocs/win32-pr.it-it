---
description: Enumerazione usata per indicare il motivo per cui un pixel è stato rifiutato.
MS-HAID: vspixengine.PIXELKILLREASON
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione PIXELKILLREASON
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 43836288-554B-430C-861D-AAC58DE3B282
api_name:
- PIXELKILLREASON
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58ead08f81c8dee1644e431ae100c5100551e9907ab9a9d5bf00f6aae3532abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119325"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>Enumerazione PIXELKILLREASON

Enumerazione usata per indicare il motivo per cui un pixel è stato rifiutato.

## <a name="syntax"></a>Sintassi


```C++
};
```

## <a name="constants"></a>Costanti

<span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ NONE**  
Valore che indica che il pixel non è stato rifiutato.

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**PKR \_ SHADERKILL**  
Valore che indica che il pixel è stato rifiutato perché lo shader non è stato eseguito.

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**PKR \_ SCISSORTEST**  
Valore che indica che il pixel è stato rifiutato perché il test di scissor non è riuscito.

<span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**PKR \_ ALPHATEST**  
Valore che indica che il pixel è stato rifiutato perché il test alfa non è riuscito.

<span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**PKR \_ STENCILTEST**  
Valore che indica che il pixel è stato rifiutato perché il test dello stencil non è riuscito.

<span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**TEST PROFONDITÀ \_ PKR**  
Valore che indica che il pixel è stato rifiutato perché il test di profondità non è riuscito.

<span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**PKR \_ NOTCOMPUTABLE**  
Valore che indica che non è possibile calcolare la cronologia pixel.

<span id="PKR_ERROR"></span><span id="pkr_error"></span>**ERRORE \_ PKR**  
Valore che indica che il pixel è stato rifiutato a causa di un errore generale.

<span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR \_ NOINTERSECTION**  
Valore che indica che il pixel è stato rifiutato perché la chiamata di disegno non interseca il pixel.

<span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ OCCLUDED**  
Valore che indica che il pixel è stato rifiutato perché il disegno è stato occluded.

<span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**PROFONDITÀ \_ PKRSTENCILTEST**  
Valore che indica che il pixel è stato rifiutato perché il test di profondità e stencil non è riuscito.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



