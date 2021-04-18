---
title: Metodo GetFile IBackgroundCopyError (Deliveryoptimization. h)
description: Recupera un puntatore di interfaccia all'oggetto file associato all'errore.
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
ms.openlocfilehash: b84396797378c77a6f774b4c63a3966b0d601b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301486"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a>Metodo IBackgroundCopyError:: GetFile

Recupera un puntatore di interfaccia all'oggetto file associato all'errore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppFile* \[ out\]
</dt> <dd>

Puntatore all'interfaccia [**IBackgroundCopyFile**](ibackgroundcopyfile.md) i cui metodi vengono utilizzati per determinare i nomi file locali e remoti associati all'errore. Il parametro *ppFile* è impostato su **null** se l'errore non è associato al file locale o remoto. Al termine, rilasciare *ppFile*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti.



| Codice restituito                                                                                                | Descrizione                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>                   | Il puntatore di interfaccia all'oggetto file è stato recuperato.<br/>                                     |
| <dl> <dt>**DO_E_FILE_NOT_AVAILABLE**</dt> </dl> | L'errore non è associato a un file locale o remoto. Il parametro *ppFile* è impostato su **null**.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError viene definito come 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError:: GetError**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





