---
description: La funzione LoadIPAddresses viene chiamata dal monitoraggio per compilare un elenco di indirizzi IP con indirizzi provenienti da una variabile di stringa di configurazione HTML.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: Funzione LoadIPAddresses (Netmon.h)
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
ms.openlocfilehash: 2f56517fd0caf4762be2848ac9a6f3094ed5e3194b2eb84123bf2fcc2bf67bcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742671"
---
# <a name="loadipaddresses-function"></a>Funzione LoadIPAddresses

La **funzione LoadIPAddresses** viene chiamata dal monitoraggio per compilare un elenco di indirizzi IP con indirizzi provenienti da una variabile di stringa di configurazione HTML.

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

*pConfig* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa di configurazione HTML passata al monitoraggio dal [metodo IMonitor::D oConfigure.](imonitor-doconfigure.md)

</dd> <dt>

*pVarName* \[ Pollici\]
</dt> <dd>

Puntatore al nome della variabile nella stringa di configurazione.

</dd> <dt>

*ppAddresses* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a una matrice di indirizzi. Se la variabile specificata in *pVarName* viene trovata e ha una lunghezza non zero, la funzione alloca spazio sufficiente e archivia tutti gli indirizzi IP come matrice.

</dd> <dt>

*pNumAddresses* \[ Cambio\]
</dt> <dd>

Puntatore alla **variabile DWORD** impostata sul numero di indirizzi IP prelevati dalla stringa di configurazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo (il nome della variabile è stato trovato ed è presente una stringa di lunghezza non zero che rappresenta gli indirizzi IP), il valore restituito è **TRUE.**

Se la funzione ha esito negativo, il valore restituito è **FALSE.**

## <a name="remarks"></a>Commenti

Gli indirizzi IP devono essere in formato x.x.x.x (ad esempio, 127.0.0.1).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




