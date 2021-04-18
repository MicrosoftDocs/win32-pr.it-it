---
description: Specifica se una trasformazione Media Foundation (MFT) supporta video stereoscopici 3D.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: Attributo MFT_SUPPORT_3DVIDEO (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbc7208f9bbcf2c638ae83e988c6e541a4be2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309074"
---
# <a name="mft_support_3dvideo-attribute"></a>\_Attributo 3DVIDEO del supporto MFT \_

Specifica se una trasformazione Media Foundation (MFT) supporta video stereoscopici 3D.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Per eseguire una query su questo attributo, chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi globale di MFT. Se **GetAttributes** ha esito positivo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Il valore predefinito di questo attributo è **false**. Considerare questo attributo come di sola lettura. Non modificare il valore. il MFT ignorerà tutte le modifiche apportate al valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




