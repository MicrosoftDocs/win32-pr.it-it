---
description: Imposta i flag di associazione del moniker per il flusso di byte HTTP Microsoft Media Foundation.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: Proprietà MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325417"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a>MFPKEY \_ http \_ ByteStream \_ Urlmon \_ binding \_ Flags proprietà

Imposta i flag di associazione del moniker per il flusso di byte HTTP Microsoft Media Foundation.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**ULONG**

\_UI4 VT

**ulVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare il flusso di byte HTTP Media Foundation. Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Il valore di questa proprietà è un operatore OR bit per bit di **flag dell'enumerazione** **BINDF** . Questa proprietà si applica solo quando la proprietà [MFPKEY \_ http \_ ByteStream \_ enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) è impostata su **Variant \_ true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
