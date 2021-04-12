---
description: Rappresenta una richiesta di un campione da un MediaStreamSource.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: Interfaccia IMFMediaStreamSourceSampleRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351511"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a>Interfaccia IMFMediaStreamSourceSampleRequest

Rappresenta una richiesta di un campione da un MediaStreamSource.

## <a name="members"></a>Membri

L'interfaccia **IMFMediaStreamSourceSampleRequest** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMFMediaStreamSourceSampleRequest** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMFMediaStreamSourceSampleRequest** dispone di questi metodi.



| Metodo                                                           | Descrizione                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [**SetSample**](imfmediastreamsourcesamplerequest-setsample.md) | Imposta l'esempio per l'origine del flusso multimediale.<br/> |



 

## <a name="remarks"></a>Commenti

**MFMediaStreamSourceSampleRequest** viene implementato dalla classe di runtime [**Windows. Media. Core. MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                       |
| IDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Media Foundation](media-foundation-interfaces.md)
</dt> </dl>

 

 
