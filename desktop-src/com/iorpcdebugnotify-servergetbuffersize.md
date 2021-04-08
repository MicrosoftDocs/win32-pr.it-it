---
title: Metodo IOrpcDebugNotify ServerGetBufferSize
description: Recupera la dimensione del buffer RPC dal debugger lato server.
ms.assetid: 1e9ef194-c85b-4f6d-8b89-1f7ee6941189
keywords:
- Metodo ServerGetBufferSize COM
- Metodo ServerGetBufferSize COM, interfaccia IOrpcDebugNotify
- Interfaccia IOrpcDebugNotify COM, metodo ServerGetBufferSize
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d461670cc65f5cfcb433a52529e724a1c54bede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964951"
---
# <a name="iorpcdebugnotifyservergetbuffersize-method"></a>Metodo IOrpcDebugNotify:: ServerGetBufferSize

Recupera la dimensione del buffer RPC dal debugger lato server.

> [!Note]  
> Una libreria di importazione contenente la funzione **ServerGetBufferSize** non è inclusa in Microsoft Windows Software Development Kit (SDK). Un'applicazione può usare le funzioni [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questa funzione tramite l'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

## <a name="syntax"></a>Sintassi


```C++
void ServerGetBufferSize(
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

[**\_argomenti init \_ ORPC**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

