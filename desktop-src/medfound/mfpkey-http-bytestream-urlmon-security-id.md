---
description: Imposta l'identificatore di sicurezza radice per il flusso di byte HTTP Microsoft Media Foundation.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: Proprietà MFPKEY_HTTP_ByteStream_Urlmon_Security_Id (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332665"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a>MFPKEY \_ http \_ ByteStream \_ Urlmon \_ sicurezza \_ ID proprietà

Imposta l'identificatore di sicurezza radice per il flusso di byte HTTP Microsoft Media Foundation.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**Campo CAUB**

VT \_ vettore \| VT \_ UI1

**Campo CAUB**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare il flusso di byte HTTP Media Foundation. Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Questa proprietà si applica solo quando la proprietà [MFPKEY \_ http \_ ByteStream \_ enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) è impostata su **Variant \_ true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
