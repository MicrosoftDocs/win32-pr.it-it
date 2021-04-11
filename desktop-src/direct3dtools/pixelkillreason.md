---
description: Enumerazione utilizzata per indicare il motivo per cui un pixel è stato rifiutato.
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
ms.openlocfilehash: f87b072eec1ac98ca68171593765567f5e77e70e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341821"
---
# <a name="span-idvspixenginepixelkillreasonspanpixelkillreason-enumeration"></a><span id="vspixengine.pixelkillreason"></span>Enumerazione PIXELKILLREASON

Enumerazione utilizzata per indicare il motivo per cui un pixel è stato rifiutato.

## <a name="syntax"></a>Sintassi


```C++
};
```

## <a name="constants"></a>Costanti

<span id="PKR_NONE"></span><span id="pkr_none"></span>**PKR \_ None**  
Valore che indica che il pixel non è stato rifiutato.

<span id="PKR_SHADERKILL"></span><span id="pkr_shaderkill"></span>**\_SHADERKILL PKR**  
Valore che indica che il pixel è stato rifiutato perché lo shader non è stato eseguito.

<span id="PKR_SCISSORTEST"></span><span id="pkr_scissortest"></span>**\_SCISSORTEST PKR**  
Valore che indica che il pixel è stato rifiutato perché il test della forbice ha avuto esito negativo.

<span id="PKR_ALPHATEST"></span><span id="pkr_alphatest"></span>**\_ALPHATEST PKR**  
Valore che indica che il pixel è stato rifiutato perché il test alfa ha avuto esito negativo.

<span id="PKR_STENCILTEST"></span><span id="pkr_stenciltest"></span>**\_STENCILTEST PKR**  
Valore che indica che il pixel è stato rifiutato perché il test dello stencil ha avuto esito negativo.

<span id="PKR_DEPTHTEST"></span><span id="pkr_depthtest"></span>**\_DEPTHTEST PKR**  
Valore che indica che il pixel è stato rifiutato perché il test di profondità non è riuscito.

<span id="PKR_NOTCOMPUTABLE"></span><span id="pkr_notcomputable"></span>**\_NOTCOMPUTABLE PKR**  
Valore che indica che non è possibile calcolare la cronologia dei pixel.

<span id="PKR_ERROR"></span><span id="pkr_error"></span>**\_errore PKR**  
Valore che indica che il pixel è stato rifiutato a causa di un errore generale.

<span id="PKR_NOINTERSECTION"></span><span id="pkr_nointersection"></span>**PKR \_ NOintersection**  
Valore che indica che il pixel è stato rifiutato perché la chiamata di progetto non interseca il pixel.

<span id="PKR_OCCLUDED"></span><span id="pkr_occluded"></span>**PKR \_ nascosto**  
Valore che indica che il pixel è stato rifiutato perché il progetto è nascosto.

<span id="PKR_DEPTHSTENCILTEST"></span><span id="pkr_depthstenciltest"></span>**\_DEPTHSTENCILTEST PKR**  
Valore che indica che il pixel è stato rifiutato perché il test di profondità e stencil ha avuto esito negativo.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



