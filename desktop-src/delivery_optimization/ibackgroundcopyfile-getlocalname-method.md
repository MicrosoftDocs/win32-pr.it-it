---
title: Metodo GetLocalName IBackgroundCopyFile (Deliveryoptimization. h)
description: Recupera il nome locale del file.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- GetLocalName (metodo)
- Metodo GetLocalName, interfaccia IBackgroundCopyFile
- Interfaccia IBackgroundCopyFile, metodo GetLocalName
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048279"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a>Metodo IBackgroundCopyFile:: GetLocalName

Recupera il nome locale del file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppName* \[ out\]
</dt> <dd>

Stringa con terminazione null che contiene il nome del file nel client. Il nome è completo. Chiamare la funzione [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) per liberare *ppName* al termine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **S_OK** in esito positivo o uno dei valori **HRESULT** com standard in errore.

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

[**IBackgroundCopyFile:: GetRemoteName**](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

