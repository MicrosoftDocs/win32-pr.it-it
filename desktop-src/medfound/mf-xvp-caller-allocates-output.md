---
description: Specifica se il chiamante allocherà le trame usate per l'output.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: Attributo MF_XVP_CALLER_ALLOCATES_OUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527396"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a>Il \_ chiamante MF XVP \_ \_ alloca l' \_ attributo output

Specifica se il chiamante allocherà le trame usate per l'output.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Se questo attributo è **true**, il processore video prevede che le trame di output siano allocate dal chiamante, anche quando si opera in modalità DXVA (DirectX Video Acceleration). Se questo attributo è **false**, il processore video alloca le trame di output quando opera in modalità DXVA e avrà esito negativo se vengono fornite le trame di output fornite dal chiamante.

Per impostare l'attributo:

1.  Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sul processore video.
2.  Chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Impostare l'attributo prima dell'inizio del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




