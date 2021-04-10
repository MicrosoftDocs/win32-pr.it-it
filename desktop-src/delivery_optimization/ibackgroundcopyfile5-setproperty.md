---
title: Metodo SetProperty IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Imposta una proprietà generica di un trasferimento di file di ottimizzazione recapito.
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- Metodo SetProperty
- Metodo SetProperty, interfaccia IBackgroundCopyFile5
- Interfaccia IBackgroundCopyFile5, metodo SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964127"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a>Metodo IBackgroundCopyFile5:: SetProperty

Imposta una proprietà generica di un trasferimento di file di ottimizzazione recapito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PropertyId* \[ in\]
</dt> <dd>

Specifica la proprietà da impostare.

</dd> <dt>

*ProertyValue* \[ out\]
</dt> <dd>

Puntatore a un'Unione che specifica il valore da impostare. Viene usato il membro dell'Unione appropriato per l'ID di proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S_OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 viene definito come 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5. GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





