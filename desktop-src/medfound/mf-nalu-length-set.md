---
description: Indica che le informazioni sulla lunghezza di NALU verranno inviate come BLOB con ciascun esempio H. 264 compresso.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: Attributo MF_NALU_LENGTH_SET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318717"
---
# <a name="mf_nalu_length_set-attribute"></a>\_ \_ Attributo set di lunghezza MF Nalu \_

Indica che le informazioni sulla lunghezza di NALU verranno inviate come **BLOB** con ciascun esempio H. 264 compresso.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Impostare questo attributo sul tipo di supporto di input di MEDIASUBTYPE \_ H264.

Impostare \_ \_ la lunghezza MF Nalu \_ impostata sul tipo di supporto di input del decodificatore H. 264, che indica che ogni esempio di input avrà una lunghezza di Nalu disponibile e ogni esempio di input conterrà un'immagine primaria completa.

Il **BLOB** contenente le informazioni sulla lunghezza di Nalu può essere recuperato dall'attributo [MF \_ Nalu \_ length \_ Information](mf-nalu-length-information.md) nell'esempio di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




