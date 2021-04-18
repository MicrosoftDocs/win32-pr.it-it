---
description: Notifica al driver quando un'applicazione Microsoft DirectDraw passa alla modalità esclusiva o viceversa.
ms.assetid: f2b63d90-7ede-479f-a2fd-ae9870c4d7b9
title: Funzione NtGdiDdSetExclusiveMode (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetExclusiveMode
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1d2420f4ae093b4bfc3f68871daefd5c20da308e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304460"
---
# <a name="ntgdiddsetexclusivemode-function"></a>NtGdiDdSetExclusiveMode (funzione)

\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo. Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]

Notifica al driver quando un'applicazione Microsoft DirectDraw passa alla modalità esclusiva o viceversa.

## <a name="syntax"></a>Sintassi


```C++
DWORD APIENTRY NtGdiDdSetExclusiveMode(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_SETEXCLUSIVEMODEDATA puSetExclusiveModeData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDirectDraw* \[ in\]
</dt> <dd>

Handle per l'oggetto DirectDraw in modalità kernel creato in precedenza.

</dd> <dt>

*puSetExclusiveModeData* \[ in uscita\]
</dt> <dd>

Puntatore a una struttura [**DD \_ SETEXCLUSIVEMODEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setexclusivemodedata) che contiene le informazioni di notifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**NtGdiDdSetExclusiveMode** restituisce uno dei codici di callback seguenti.



| Codice restituito                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_driver DDHAL \_ gestito**</dt> </dl>    | Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione. Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione. In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.<br/>                                                                                 |
| <dl> <dt>**\_NOTHANDLED driver \_ DDHAL**</dt> </dl> | Il driver non ha commenti sull'operazione richiesta. Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore. In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.<br/> |



 

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

 

 
