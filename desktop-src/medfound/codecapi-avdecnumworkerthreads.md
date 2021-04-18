---
description: Imposta il numero di thread di lavoro utilizzati da un decodificatore video.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: Proprietà CODECAPI_AVDecNumWorkerThreads (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305503"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a>Proprietà AVDecNumWorkerThreads di codecapi \_

Imposta il numero di thread di lavoro utilizzati da un decodificatore video.

## <a name="data-type"></a>Tipo di dati

**Long** (**VT \_ I4**)

## <a name="property-guid"></a>GUID proprietà

Codecapis \_ AVDecNumWorkerThreads

## <a name="remarks"></a>Commenti

Se il valore è 1, il decodificatore seleziona il numero di thread.

Per l'interfaccia [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) , impostare questa proprietà come valore **Long** (**VT \_ I4**). Per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , impostare questa proprietà come **UInt32**, anche se il valore è firmato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

