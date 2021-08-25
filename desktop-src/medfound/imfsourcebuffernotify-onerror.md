---
description: Utilizzato per indicare che si è verificato un errore con il buffer di origine.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: Metodo IMFSourceBufferNotify::OnError
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
ms.openlocfilehash: 0602340011bae5af974a3441b42d62d392394b79854015acc68da0b1c2fcf538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957801"
---
# <a name="imfsourcebuffernotifyonerror-method"></a>Metodo IMFSourceBufferNotify::OnError

Utilizzato per indicare che si è verificato un errore con il buffer di origine.

## <a name="syntax"></a>Sintassi


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hr* \[ Pollici\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                 |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMFSourceBufferNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




