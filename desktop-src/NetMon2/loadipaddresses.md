---
description: La funzione LoadIPAddresses viene chiamata dal monitoraggio per compilare un elenco di indirizzi IP con gli indirizzi ricavati da una variabile di stringa di configurazione HTML.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: Funzione LoadIPAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a5c172117081777b2a89b875401ec0645dd643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319938"
---
# <a name="loadipaddresses-function"></a>LoadIPAddresses (funzione)

La funzione **LoadIPAddresses** viene chiamata dal monitoraggio per compilare un elenco di indirizzi IP con gli indirizzi ricavati da una variabile di stringa di configurazione HTML.

## <a name="syntax"></a>Sintassi


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pConfig* \[ in\]
</dt> <dd>

Puntatore alla stringa di configurazione HTML passata al monitoraggio tramite il metodo [Imonitor::D oconfigure](imonitor-doconfigure.md) .

</dd> <dt>

*pVarName* \[ in\]
</dt> <dd>

Puntatore al nome della variabile nella stringa di configurazione.

</dd> <dt>

*ppAddresses* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una matrice di indirizzi. Se la variabile specificata in *pVarName* viene trovata e ha una lunghezza diversa da zero, la funzione alloca spazio sufficiente e archivia tutti gli indirizzi IP come matrice.

</dd> <dt>

*pNumAddresses* \[ out\]
</dt> <dd>

Puntatore alla variabile **DWORD** impostata sul numero di indirizzi IP ricavati dalla stringa di configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (il nome della variabile è stato trovato e presenta una stringa di lunghezza diversa da zero che rappresenta gli indirizzi IP), il valore restituito è **true**.

Se la funzione ha esito negativo, il valore restituito è **false**.

## <a name="remarks"></a>Commenti

Gli indirizzi IP devono essere nel formato x. x.x. x, ad esempio 127.0.0.1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




