---
description: Elimina definitivamente un oggetto Surface Microsoft DirectDraw in modalità kernel allocato in precedenza.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: Funzione NtGdiDdDestroySurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 54799aa90007370439b2be8c8cf8c1f584360a5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049183"
---
# <a name="ntgdidddestroysurface-function"></a>NtGdiDdDestroySurface (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Elimina definitivamente un oggetto Surface Microsoft DirectDraw in modalità kernel allocato in precedenza.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hSurface* \[ in\]
</dt> <dd>

Handle per l'oggetto Surface precedentemente allocato in modalità kernel.

</dd> <dt>

*bRealDestroy* \[ in\]
</dt> <dd>

Specifica la modalità di eliminazione della superficie. Può essere uno dei valori seguenti.

<dt>



 TRUE


</dt> <dd>

Elimina la superficie e la memoria video disponibile.

</dd> <dt>



 FALSE


</dt> <dd>

Liberare la memoria del video, ma lasciare la superficie in uno stato non inizializzato.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdDestroySurface** restituisce uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_driver DDHAL \_ gestito**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione. Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione. In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**\_NOTHANDLED driver \_ DDHAL**</dt> </dl> | Il driver non ha commenti sull'operazione richiesta. Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.<br/> |



 

## <a name="remarks"></a>Commenti

È consigliabile che le applicazioni usino le API DirectDraw e Direct3D per creare ed eliminare definitivamente le superfici anziché questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto client di livello inferiore grafica](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




