---
description: Consente all'Microsoft Media Foundation flusso di byte HTTP di utilizzare i moniker URL (detti anche Urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: Proprietà MFPKEY_HTTP_ByteStream_Enable_Urlmon (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325421"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a>MFPKEY \_ http \_ ByteStream \_ Abilita \_ Proprietà Urlmon

Consente all'Microsoft Media Foundation flusso di byte HTTP di utilizzare i moniker URL (detti anche *Urlmon*).



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**\_bool Variant**

\_bool VT

**boolVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare il flusso di byte HTTP Media Foundation. Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Se il valore è **Variant \_ true**, il flusso di byte http USA Urlmon per il trasporto HTTP. In caso contrario, se il valore è **Variant \_ false**, il flusso di byte utilizza WinHTTP.

Il valore predefinito è **Variant \_ true** per le applicazioni Windows Store e **Variant \_ false** per applicazioni desktop di Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
