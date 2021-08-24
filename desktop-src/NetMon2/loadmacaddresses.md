---
description: La funzione LoadMACAddresses viene chiamata dal monitoraggio per compilare un elenco di indirizzi MAC con indirizzi presi da una variabile di stringa di configurazione HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Funzione LoadMACAddresses (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2de609ef0a1e820785ee7d62cbbe1e6af32c633aa29b133974f6f5f6f2a649b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742721"
---
# <a name="loadmacaddresses-function"></a>Funzione LoadMACAddresses

La **funzione LoadMACAddresses** viene chiamata dal monitoraggio per compilare un elenco di indirizzi MAC con indirizzi presi da una variabile di stringa di configurazione HTML.

## <a name="syntax"></a>Sintassi


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pConfig* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa di configurazione HTML passata al monitoraggio dal metodo [IMonitor::D oConfigure.](imonitor-doconfigure.md)

</dd> <dt>

*pVarName* \[ Pollici\]
</dt> <dd>

Puntatore al nome della variabile nella stringa di configurazione.

</dd> <dt>

*ppAddresses* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a una matrice di indirizzi. Se la variabile specificata in *pVarName* viene trovata e ha una lunghezza non zero, la funzione alloca spazio sufficiente (usando **HeapAllocMemory**) e archivia tutti gli indirizzi MAC come matrice.

</dd> <dt>

*pNumAddresses* \[ Cambio\]
</dt> <dd>

Puntatore alla **variabile DWORD** impostata sul numero di indirizzi MAC presi dalla stringa di configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo( il nome della variabile è stato trovato e ha una stringa di lunghezza non zero che rappresenta gli indirizzi MAC), il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




