---
description: Abilita o Disabilita il read-ahead in un'origine multimediale.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: Proprietà MFPKEY_MediaSource_DisableReadAhead (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328190"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a>\_ \_ Proprietà DISABLEREADAHEAD di MFPKEY MediaSource

Abilita o Disabilita il read-ahead in un'origine multimediale.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**\_bool Variant**

\_bool VT

**boolVal**



## <a name="remarks"></a>Commenti

Le applicazioni possono usare questa proprietà per configurare alcune origini multimediali. Per impostare la proprietà, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

Se il valore è **Variant \_ true**, l'origine multimediale non verrà letta in anticipo nel flusso di byte. Questa impostazione può ottimizzare le prestazioni se si prevede di leggere una quantità limitata di dati dall'origine multimediale, ad esempio per ottenere un'immagine di anteprima da un file video.

Per la riproduzione audio/video tipica, questa proprietà deve essere impostata su **Variant \_ false**. Il valore predefinito è **Variant \_ false**.

Non ogni origine supporto supporta questa proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Client<br/> | Windows 7<br/>                                                               |
| Intestazione<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




