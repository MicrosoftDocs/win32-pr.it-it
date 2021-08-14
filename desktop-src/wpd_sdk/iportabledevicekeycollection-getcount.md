---
description: Il metodo GetCount recupera il numero di chiavi in questa raccolta.
ms.assetid: 963f514e-3e0f-4334-ac29-6de7cc8aa336
title: Metodo IPortableDeviceKeyCollection::GetCount (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d5cd44ebcb17df00f8af2dad5d92445346c3c929500a78fce28358c0cf39a2cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194416"
---
# <a name="iportabledevicekeycollectiongetcount-method"></a>Metodo IPortableDeviceKeyCollection::GetCount

Il **metodo GetCount** recupera il numero di chiavi in questa raccolta.

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

Puntatore a **un valore DWORD** che contiene il numero di chiavi nella raccolta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il metodo è riuscito.<br/>                     |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl> | Un argomento del puntatore obbligatorio era **NULL.**<br/> |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [Recupero di eventi del servizio supportati.](retrieving-supported-events.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[Recupero di eventi del servizio supportati](retrieving-supported-events.md)
</dt> <dt>

[Recupero di metodi di servizio supportati](retrieving-supported-methods.md)
</dt> </dl>

 

 




