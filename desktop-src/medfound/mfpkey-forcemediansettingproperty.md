---
description: Specifica se il codec deve usare il filtro mediano durante la codifica.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: MFPKEY_FORCEMEDIANSETTING proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722fca2f73f2114cf17664f228e00a12f46e5a399f54b8dc6990940f5c18d979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953951"
---
# <a name="mfpkey_forcemediansetting-property"></a>Proprietà MFPKEY \_ FORCEMEDIANSETTING

Specifica se il codec deve usare il filtro mediano durante la codifica.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCForceMedianSetting

## <a name="data-type"></a>Tipo di dati

VT \_ BOOL

## <a name="default-value"></a>Valore predefinito

FALSE

## <a name="remarks"></a>Commenti

Il filtro mediano indica al codec di ignorare il disturbo e la granulosità durante il calcolo del movimento tra fotogrammi. Ciò può migliorare la qualità dei video molto rumorosi, ma può causare tracce di movimento (note anche come artefatti finali) se applicate al video di origine pulita.

Per impostazione predefinita, il codec usa la logica interna per determinare se usare il filtro mediano. Se si imposta questa proprietà, tale logica verrà sottoposta a override.

> [!Note]  
> Questo filtro non corrisponde ai filtri di sfocatura mediana presenti in molte applicazioni di modifica e post-elaborazione video.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 




