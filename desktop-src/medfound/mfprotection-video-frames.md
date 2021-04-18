---
description: Specifica se a un'applicazione è consentito l'accesso ai frame video non compressi.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: Attributo MFPROTECTION_VIDEO_FRAMES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310248"
---
# <a name="mfprotection_video_frames-attribute"></a>MFPROTECTION \_ \_ attributo video frames

Specifica se a un'applicazione è consentito l'accesso ai frame video non compressi.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il valore 0 indica che l'applicazione è autorizzata ad accedere ai frame. Questo potrebbe essere determinato in seguito a un contratto privato tra l'applicazione e il particolare sistema di protezione del contenuto in uso.

Il valore 1 indica che l'applicazione è autorizzata ad accedere ai frame se l'applicazione fornisce un certificato dell'applicazione valido (vedere [**IMFMediaEngineProtectedContent:: SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).

Il valore 0xFFFFFFFF, che corrisponde al valore predefinito, indica che non è consentito l'accesso alle applicazioni ai frame non compressi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app UWP Windows 8\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app UWP Windows Server 2012\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




