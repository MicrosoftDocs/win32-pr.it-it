---
title: Metodo GetFile IBackgroundCopyError (Deliveryoptimization.h)
description: Recupera un puntatore a interfaccia all'oggetto file associato all'errore.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- Metodo GetFile
- Metodo GetFile, interfaccia IBackgroundCopyError
- Interfaccia IBackgroundCopyError, metodo GetFile
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbed5497bcebb3518c7f6a56646976cc01fbfebc501af4a08e861139311f4bc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096711"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a>Metodo IBackgroundCopyError::GetFile

Recupera un puntatore a interfaccia all'oggetto file associato all'errore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppFile* \[ Cambio\]
</dt> <dd>

Puntatore [**a interfaccia IBackgroundCopyFile**](ibackgroundcopyfile.md) i cui metodi vengono utilizzati per determinare i nomi di file locali e remoti associati all'errore. Il *parametro ppFile* è impostato su **NULL se** l'errore non è associato al file locale o remoto. Al termine, *rilasciare ppFile*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti.



| Codice restituito                                                                                                | Descrizione                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>                   | È stato recuperato un puntatore a interfaccia all'oggetto file.<br/>                                     |
| <dl> <dt>**DO_E_FILE_NOT_AVAILABLE**</dt> </dl> | L'errore non è associato a un file locale o remoto. Il *parametro ppFile* è impostato su **NULL.**<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError è definito come 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError::GetError**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





