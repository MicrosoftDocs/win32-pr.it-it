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
ms.openlocfilehash: 8304184f3323feb92a14b523dc629c6ae45f6a85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083179"
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

 

 




