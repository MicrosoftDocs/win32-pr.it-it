---
description: Specifica se il chiamante alloca le trame usate per l'output.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: MF_XVP_CALLER_ALLOCATES_OUTPUT attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31da89bec9c9573d9d968077e51d413e1861bca28cb606667d402fab5a408f96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599971"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a>Attributo MF \_ XVP \_ CALLER \_ ALLOCATES \_ OUTPUT

Specifica se il chiamante alloca le trame usate per l'output.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Se questo attributo è **TRUE,** il processore video prevede l'allocazione delle trame di output da parte del chiamante, anche quando si opera in modalità Accelerazione video DirectX (DXVA). Se questo attributo è **FALSE,** il processore video alloca le trame di output quando opera in modalità DXVA e avrà esito negativo se vengono fornite trame di output fornite dal chiamante.

Per impostare questo attributo:

1.  Chiamare [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) nel processore video.
2.  Chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Impostare l'attributo prima dell'inizio del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




