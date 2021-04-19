---
description: Specifica il numero preferito di campioni per fotogramma.
ms.assetid: ad629dbd-49d8-43d0-95a8-03f2043e397e
title: Proprietà MFPKEY_PREFERRED_FRAMESIZE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe04ad37c6cd684e3179cbd16328346fd6f11dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333090"
---
# <a name="mfpkey_preferred_framesize-property"></a>\_ \_ Proprietà FRAMESIZE preferita MFPKEY

Specifica il numero preferito di campioni per fotogramma.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

**\_UI4 VT**

## <a name="remarks"></a>Commenti

Per specificare una dimensione del fotogramma preferita, impostare le proprietà seguenti.

-   Impostare [**MFPKEY che \_ richiede \_ un \_ FRAMESIZE**](mfpkey-requesting-a-framesizeproperty.md) a **Variant \_ true**.
-   Impostare **MFPKEY \_ preferenziale \_ FRAMESIZE** sul numero di campioni desiderato in ogni frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows Vista o Windows 7<br/>                                                   |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
