---
description: Consente al flusso Microsoft Media Foundation di byte HTTP di usare moniker URL (detti anche Urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: MFPKEY_HTTP_ByteStream_Enable_Urlmon proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ede2b9109a7345f3a0d764f6a8fa68952686c5ca05207d01bb0a2e54cea4d32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344381"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a>MFPKEY \_ HTTP \_ ByteStream Enable \_ \_ Urlmon - proprietà

Consente al flusso Microsoft Media Foundation di byte HTTP di usare moniker URL ( detto *anche Urlmon*).



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare il flusso Media Foundation byte HTTP. Per impostare la proprietà, passare un [**puntatore IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale.](configuring-a-media-source.md)

Se il valore è **VARIANT \_ TRUE,** il flusso di byte HTTP usa Urlmon per il trasporto HTTP. In caso contrario, se il valore **è VARIANT \_ FALSE,** il flusso di byte usa WinHTTP.

Il valore predefinito è **VARIANT TRUE per \_ le** Windows Store e **VARIANT \_ FALSE** per Windows app desktop.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
