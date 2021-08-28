---
description: Specifica che il codificatore MFT supporta la ricezione di eventi MEEncodingParameter durante lo streaming.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: MFT_ENCODER_SUPPORTS_CONFIG_EVENT attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a528da44d59077c8445616f8fe344cba5497ced8b33be75e33be71bf9b5d76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113041"
---
# <a name="mft_encoder_supports_config_event-attribute"></a>IL CODIFICATORE MFT \_ \_ SUPPORTA \_ l'attributo \_ CONFIG EVENT

Specifica che il codificatore MFT supporta la ricezione di [eventi MEEncodingParameter durante](meencodingparameters.md) lo streaming.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Inviato dal codificatore MFT tramite [**IMFTransform::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| app UWP\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mftransform.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFTransform::P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




