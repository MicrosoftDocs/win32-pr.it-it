---
description: Imposta l'identificatore di sicurezza radice per il Microsoft Media Foundation di byte HTTP.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: MFPKEY_HTTP_ByteStream_Urlmon_Security_Id proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d64b07dc7d419624bfe300b890b58554394a5cd3e8363ddcbc4d5be91d9e4b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118738008"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a>Proprietà MFPKEY \_ HTTP \_ ByteStream \_ Urlmon \_ Security \_ Id

Imposta l'identificatore di sicurezza radice per il Microsoft Media Foundation di byte HTTP.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**CAUB**

VT \_ VECTOR \| VT \_ UI1

**caub**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare il flusso Media Foundation byte HTTP. Per impostare la proprietà, passare un [**puntatore IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

Questa proprietà si applica solo quando la [proprietà MFPKEY \_ HTTP \_ ByteStream Enable \_ \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) è impostata su **VARIANT \_ TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
