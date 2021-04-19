---
description: Imposta una finestra per il flusso di byte HTTP Microsoft Media Foundation.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: Proprietà MFPKEY_HTTP_ByteStream_Urlmon_Window (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332664"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a>MFPKEY \_ http \_ ByteStream \_ \_ proprietà finestra Urlmon

Imposta una finestra per il flusso di byte HTTP Microsoft Media Foundation. La finestra viene utilizzata per presentare informazioni nell'interfaccia utente durante un'operazione di associazione.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**IUnknown\***

VT \_ sconosciuto

**punkVal**



## <a name="remarks"></a>Commenti

Usare questa proprietà per configurare il flusso di byte HTTP Media Foundation. Per impostare la proprietà, passare un puntatore [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Il valore di questa proprietà è un puntatore all'interfaccia **IWindowForBindingUI** . Questa proprietà si applica solo quando la proprietà [MFPKEY \_ http \_ ByteStream \_ enable \_ Urlmon](mfpkey-http-bytestream-enable-urlmon.md) è impostata su **Variant \_ true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
