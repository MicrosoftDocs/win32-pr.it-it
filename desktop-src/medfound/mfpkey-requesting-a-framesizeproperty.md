---
description: Specifica se il codificatore deve usare una dimensione del fotogramma preferita specificata in numero di campioni per fotogramma.
ms.assetid: c9baeff7-53fb-425f-b07b-4066a705ca54
title: MFPKEY_REQUESTING_A_FRAMESIZE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c39d1d9ecdba27e46a1e49949f1607fc60d53501d321e49c4899f9b8928ccf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555431"
---
# <a name="mfpkey_requesting_a_framesize-property"></a>MFPKEY \_ CHE RICHIEDE UNA proprietà \_ \_ FRAMESIZE

Specifica se il codificatore deve usare una dimensione del fotogramma preferita specificata in numero di campioni per fotogramma.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**VT \_ BOOL**

## <a name="remarks"></a>Commenti

Per specificare le dimensioni preferite del frame, impostare le proprietà seguenti.

-   Impostare **MFPKEY \_ REQUESTING \_ A \_ FRAMESIZE** su VARIANT \_ TRUE.
-   Impostare [**MFPKEY \_ PREFERRED \_ FRAMESIZE**](mfpkey-preferred-framesizeproperty.md) sul numero di campioni desiderato in ogni frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
