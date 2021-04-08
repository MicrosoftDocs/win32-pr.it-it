---
description: Contiene un puntatore IMFFieldOfUseMFTUnlock, che può essere usato per sbloccare una trasformazione Media Foundation (MFT). L'interfaccia IMFFieldOfUseMFTUnlock viene utilizzata per sbloccare un MFT con restrizioni di campo per l'utilizzo.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: Attributo MFT_FIELDOFUSE_UNLOCK_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755271"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a>\_Attributo di \_ sblocco dell' \_ attributo FIELDOFUSE di MFT

Contiene un puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , che può essere usato per sbloccare una trasformazione Media Foundation (MFT). L'interfaccia **IMFFieldOfUseMFTUnlock** viene utilizzata per sbloccare un MFT con restrizioni di campo per l'utilizzo.

## <a name="data-type"></a>Tipo di dati

**[](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) IMFFieldOfUseMFTUnlock \** _ archiviato come _*IUnknown \**_

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Per ulteriori informazioni su questo attributo, vedere [restrizioni relative all'utilizzo dei campi](field-of-use-restrictions.md).

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Limitazioni per l'utilizzo dei campi](field-of-use-restrictions.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




