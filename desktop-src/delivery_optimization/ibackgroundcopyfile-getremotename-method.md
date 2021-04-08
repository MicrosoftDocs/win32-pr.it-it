---
title: Metodo GetRemoteName IBackgroundCopyFile (Deliveryoptimization. h)
description: Recupera il nome remoto del file.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- GetRemoteName (metodo)
- Metodo GetRemoteName, interfaccia IBackgroundCopyFile
- Interfaccia IBackgroundCopyFile, Metodo GetRemoteName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9984ed9971fdfb91279dabc5810490b62804b7e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048277"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a>Metodo IBackgroundCopyFile:: GetRemoteName

Recupera il nome remoto del file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppName* \[ out\]
</dt> <dd>

Stringa con terminazione null che contiene il nome remoto del file da trasferire. Il nome è completo. Chiamare la funzione [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare *ppName* al termine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **S_OK** in esito positivo o uno dei valori **HRESULT** com standard in errore.

## <a name="remarks"></a>Commenti

Per modificare il nome del file remoto, chiamare il metodo [**IBackgroundCopyFile2:: Seremotename**](ibackgroundcopyfile2-setremotename-method.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile viene definito come 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile:: GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

