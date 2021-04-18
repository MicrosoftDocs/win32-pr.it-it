---
description: Utilizzato per indicare che si è verificato un errore con il buffer di origine.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: 'Metodo IMFSourceBufferNotify:: OnError'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308478"
---
# <a name="imfsourcebuffernotifyonerror-method"></a>Metodo IMFSourceBufferNotify:: OnError

Utilizzato per indicare che si è verificato un errore con il buffer di origine.

## <a name="syntax"></a>Sintassi


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*risorse umane* \[ in\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFSourceBufferNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




