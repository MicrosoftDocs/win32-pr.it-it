---
title: Metodo IOrpcDebugNotify ClientFillBuffer
description: Invia i dati dal debugger client al debugger del server.
ms.assetid: d575cf34-34a2-4951-a87e-7835b2c5b7a0
keywords:
- Metodo ClientFillBuffer COM
- Metodo ClientFillBuffer COM, interfaccia IOrpcDebugNotify
- Interfaccia IOrpcDebugNotify COM, Metodo ClientFillBuffer
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 633f4f0a8a3e135ca60468d24356a3f6e038d062
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743706"
---
# <a name="iorpcdebugnotifyclientfillbuffer-method"></a>Metodo IOrpcDebugNotify:: ClientFillBuffer

Invia i dati dal debugger client al debugger del server.

> [!Note]  
> Una libreria di importazione contenente la funzione **ClientFillBuffer** non è inclusa in Microsoft Windows Software Development Kit (SDK). Un'applicazione può usare le funzioni [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questa funzione tramite l'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

## <a name="syntax"></a>Sintassi


```C++
void ClientFillBuffer(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpOrpcDebugAll* 
</dt> <dd>

Puntatore a una struttura [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) che contiene informazioni specifiche della notifica che il sistema RPC com passa al debugger.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>N/D</dt> </dl> |
| IDL<br/>                      | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

