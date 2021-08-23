---
description: 'Metodo IPortableDeviceValuesCollection::GetCount: il metodo GetCount recupera il numero di elementi nella raccolta.'
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: Metodo IPortableDeviceValuesCollection::GetCount (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: abf157a8a539d98c5b75826e4568df7c3209a0efc2dab49f6487250dd08ae391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707371"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a>Metodo IPortableDeviceValuesCollection::GetCount

Il **metodo GetCount** recupera il numero di elementi nella raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcElems* \[ Pollici\]
</dt> <dd>

Puntatore a **un valore DWORD** che contiene il **numero di interfacce IPortableDeviceValues** nella raccolta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il metodo è riuscito.<br/>                     |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Un argomento del puntatore obbligatorio era **NULL.**<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




