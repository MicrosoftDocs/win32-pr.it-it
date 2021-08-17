---
title: Metodo IBackgroundCopyFile GetRemoteName (Deliveryoptimization.h)
description: Recupera il nome remoto del file.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- Metodo GetRemoteName
- Metodo GetRemoteName, interfaccia IBackgroundCopyFile
- Interfaccia IBackgroundCopyFile, metodo GetRemoteName
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
ms.openlocfilehash: e84827f4c1144c4242f382aff822984b24dd83610c1ebd5d2540ba7c4ca65d2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118810334"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a>Metodo IBackgroundCopyFile::GetRemoteName

Recupera il nome remoto del file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppName* \[ Cambio\]
</dt> <dd>

Stringa con terminazione Null contenente il nome remoto del file da trasferire. Il nome è completo. Al [**termine, chiamare la funzione CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per *liberare ppName.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo **restituisce** S_OK in caso di esito positivo o uno dei valori **HRESULT** COM standard in caso di errore.

## <a name="remarks"></a>Commenti

Per modificare il nome del file remoto, chiamare il [**metodo IBackgroundCopyFile2::SetRemoteName.**](ibackgroundcopyfile2-setremotename-method.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile è definito come 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile::GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

