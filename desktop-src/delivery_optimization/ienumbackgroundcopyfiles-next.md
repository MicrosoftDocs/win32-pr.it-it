---
title: Metodo Next IEnumBackgroundCopyFiles (Deliveryoptimization.h)
description: Recupera un determinato numero di elementi nella sequenza di enumerazione. Se nella sequenza rimane un numero di elementi inferiore al numero richiesto, vengono recuperati gli elementi rimanenti.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Metodo Next
- Metodo Next, interfaccia IEnumBackgroundCopyFiles
- Interfaccia IEnumBackgroundCopyFiles, metodo Next
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dcf24c65b7f282b1a1e15d3109ce1af9ccfc0af6436c80c94760f0b4cd18069
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461881"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a>Metodo IEnumBackgroundCopyFiles::Next

Recupera un determinato numero di elementi nella sequenza di enumerazione. Se nella sequenza rimane un numero di elementi inferiore al numero richiesto, vengono recuperati gli elementi rimanenti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*celt* \[ Pollici\]
</dt> <dd>

Numero di elementi richiesti.

</dd> <dt>

*rgelt* \[ Cambio\]
</dt> <dd>

Matrice di [**oggetti IBackgroundCopyFile.**](ibackgroundcopyfile.md) Al termine, è necessario rilasciare ogni oggetto in *rgelt.*

</dd> <dt>

*pceltFetched* \[ Cambio\]
</dt> <dd>

Numero di elementi restituiti in *rgelt.* È possibile impostare *pceltFetched* su **NULL se** *celt* è uno. In caso contrario, inizializzare il valore di *pceltFetched* su 0 prima di chiamare questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                              | Descrizione                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | È stato restituito il numero di elementi richiesti.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Restituito minore del numero di elementi richiesti.<br/>    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles è definito come CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





