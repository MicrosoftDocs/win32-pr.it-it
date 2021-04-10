---
title: Metodo Next di IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Recupera un determinato numero di elementi nella sequenza di enumerazione. Se il numero di elementi rimasti nella sequenza è inferiore a quello richiesto, vengono recuperati gli elementi rimanenti.
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
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964697"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a>IEnumBackgroundCopyFiles:: Next (metodo)

Recupera un determinato numero di elementi nella sequenza di enumerazione. Se il numero di elementi rimasti nella sequenza è inferiore a quello richiesto, vengono recuperati gli elementi rimanenti.

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

*celt* \[ in\]
</dt> <dd>

Numero di elementi richiesti.

</dd> <dt>

*rgelt* \[ out\]
</dt> <dd>

Matrice di oggetti [**IBackgroundCopyFile**](ibackgroundcopyfile.md) . Al termine, è necessario rilasciare ogni oggetto in *rgelt* .

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Numero di elementi restituiti in *rgelt*. Se *celt* è uno, è possibile impostare *pceltFetched* su **null** . In caso contrario, inizializzare il valore di *pceltFetched* su 0 prima di chiamare questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                              | Descrizione                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Il numero di elementi richiesti è stato restituito correttamente.<br/> |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Restituito minore del numero di elementi richiesti.<br/>    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles viene definito come CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





