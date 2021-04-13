---
description: Specifica la velocità in bit massima del video per il sink multimediale Digital Living Network Alliance (DLNA).
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: Attributo MF_MP2DLNA_VIDEO_BIT_RATE (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226642"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a>\_ \_ \_ Attributo velocità in bit del video MF MP2DLNA \_

Specifica la velocità in bit massima del video per il sink multimediale Digital Living Network Alliance (DLNA).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Il valore è la velocità in bit massima di destinazione per il flusso video codificato, in bit al secondo. Il valore massimo è 9,8 milioni (9,8 Mbps), che è anche il valore predefinito.

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Per impostare questo attributo sul sink multimediale DLNA, eseguire una query sul sink multimediale per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Impostare l'attributo prima dell'inizio del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




