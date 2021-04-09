---
description: Disabilita la conversione della frequenza dei frame nella MFT del processore video.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: Attributo MF_XVP_DISABLE_FRC (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1922705514c51308138f9f301a3681e598ca6278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966894"
---
# <a name="mf_xvp_disable_frc-attribute"></a>MF \_ XVP \_ Disabilita l' \_ attributo FRC

Disabilita la conversione della frequenza dei frame nella [**MFT del processore video**](video-processor-mft.md).

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Se questo attributo è impostato su **true**, il processore video non eseguirà la conversione della frequenza dei frame. Per impostazione predefinita, il processore video convertirà la frequenza dei fotogrammi in modo che corrisponda al tipo di supporto di output.

Per impostare l'attributo:

1.  Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) sul processore video.
2.  Chiamare [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Impostare l'attributo prima dell'inizio del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




