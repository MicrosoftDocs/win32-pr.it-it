---
description: Specifica se il codec deve usare il filtro mediano durante la codifica.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: Proprietà MFPKEY_FORCEMEDIANSETTING (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886005"
---
# <a name="mfpkey_forcemediansetting-property"></a>\_Proprietà FORCEMEDIANSETTING di MFPKEY

Specifica se il codec deve usare il filtro mediano durante la codifica.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCForceMedianSetting

## <a name="data-type"></a>Tipo di dati

\_bool VT

## <a name="default-value"></a>Valore predefinito

FALSE

## <a name="remarks"></a>Commenti

Il filtro mediano indica al codec di ignorare il rumore e la granularità durante il calcolo del movimento tra frame. Questo può migliorare la qualità dei video molto rumorosi, ma può condurre a percorsi di movimento (noti anche come artefatti finali) quando applicati a video di origine puliti.

Per impostazione predefinita, il codec usa la logica interna per determinare se usare il filtro mediano. Se si imposta questa proprietà, la logica verrà sottoposta a override.

> [!Note]  
> Questo filtro non corrisponde ai filtri di sfocatura mediani disponibili in molte applicazioni di modifica e post-elaborazione video.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




