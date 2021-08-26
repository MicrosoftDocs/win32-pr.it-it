---
description: Disabilita la conversione della frequenza dei fotogrammi nel processore video MFT.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: MF_XVP_DISABLE_FRC attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e82c60438a91111ffce6cc80c71fa76231b8e00d85644f4f56f1b496202d62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940331"
---
# <a name="mf_xvp_disable_frc-attribute"></a>Attributo \_ MF XVP \_ DISABLE \_ FRC

Disabilita la conversione della frequenza fotogrammi nel [**processore video MFT**](video-processor-mft.md).

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Se questo attributo è **TRUE,** il processore video non eseguirà la conversione della frequenza fotogrammi. Per impostazione predefinita, il processore video converte la frequenza dei fotogrammi in modo che corrisponda al tipo di supporto di output.

Per impostare questo attributo:

1.  Chiamare [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) nel processore video.
2.  Chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Impostare l'attributo prima dell'inizio del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




