---
description: Richiede che l'operazione di sospensione dell'app venga posticipata.
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: 'Metodo ISuspendingOperation:: getrinvio (Windows. ApplicationModel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.GetDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 6874eb31e73fa1c20399f68850fc69204d0e0f6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879254"
---
# <a name="isuspendingoperationgetdeferral-method"></a>Metodo ISuspendingOperation:: getrinvio

Richiede che l'operazione di sospensione dell'app venga posticipata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDeferral(
  [out, retval] ISuspendingDeferral **deferral
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rinvio* \[ out, retval\]
</dt> <dd>

Sospensione di rinvio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Intestazione<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 




