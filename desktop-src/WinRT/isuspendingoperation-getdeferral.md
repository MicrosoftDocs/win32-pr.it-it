---
description: Richiede che l'operazione di sospensione dell'app sia posticipata.
ms.assetid: 5AB84652-165D-4173-A047-541B05848871
title: Metodo ISuspendingOperation::GetDeferral (Windows. ApplicationModel.h)
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
ms.openlocfilehash: 4a64ed4449c2e11ebeec9194adb7fd69ecc7227efa9df36a6900f4139e44ec4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794991"
---
# <a name="isuspendingoperationgetdeferral-method"></a>Metodo ISuspendingOperation::GetDeferral

Richiede che l'operazione di sospensione dell'app sia posticipata.

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

Sospensione posticipata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Intestazione<br/>                   | <dl> <dt>Windows. ApplicationModel.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 




