---
title: Funzione MpManagerVersionQuery (MpClient. h)
description: Restituisce le informazioni sulla versione dei vari componenti di malware Protection Manager.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpManagerVersionQuery
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302068"
---
# <a name="mpmanagerversionquery-function"></a>MpManagerVersionQuery (funzione)

Restituisce le informazioni sulla versione dei vari componenti di malware Protection Manager.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hMpHandle* \[ in\]
</dt> <dd>

Tipo: **MPHANDLE**

Handle per l'interfaccia di malware Protection Manager. Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*pVersionInfo* \[ out\]
</dt> <dd>

Tipo: **PMPVERSION \_ info**

Puntatore a una struttura che contiene informazioni sulla versione dei vari componenti di malware Protection Manager. Vedere [**MPVERSION \_ info**](mpversion-info.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.

Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito. Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**\_informazioni MPVERSION**](mpversion-info.md)
</dt> </dl>

 

 





