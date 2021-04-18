---
description: Specifica se il codificatore deve usare una dimensione del frame preferita specificata in numero di campioni per fotogramma.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: Proprietà MFPKEY_REQUESTING_A_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3355e84318ba4ad7995ac5ad0f002f4d70767b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333808"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>MFPKEY che \_ richiede \_ una \_ Proprietà FRAMESIZE

Specifica se il codificatore deve usare una dimensione del frame preferita specificata in numero di campioni per fotogramma.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_bool VT**

## <a name="remarks"></a>Commenti

Per specificare una dimensione del fotogramma preferita, impostare le proprietà seguenti.

-   Impostare **MFPKEY che \_ richiede \_ un \_ FRAMESIZE** a Variant \_ true.
-   Impostare [**MFPKEY \_ preferenziale \_ FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) sul numero di campioni desiderato in ogni frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
