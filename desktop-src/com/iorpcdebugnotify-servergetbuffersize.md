---
title: Metodo IOrpcDebugNotify ServerGetBufferSize
description: Recupera le dimensioni del buffer RPC dal debugger lato server.
ms.assetid: 1e9ef194-c85b-4f6d-8b89-1f7ee6941189
keywords:
- Metodo ServerGetBufferSize COM
- Metodo ServerGetBufferSize COM , interfaccia IOrpcDebugNotify
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
ms.openlocfilehash: 570c7371b1aa19bf5a7b3932a9560103ba0b7f25072ad7cb69d5bd53e82bb90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500731"
---
# <a name="iorpcdebugnotifyservergetbuffersize-method"></a>Metodo IOrpcDebugNotify::ServerGetBufferSize

Recupera le dimensioni del buffer RPC dal debugger lato server.

> [!Note]  
> Una libreria di importazione contenente la **funzione ServerGetBufferSize** non è inclusa in Microsoft Windows Software Development Kit (SDK). Un'applicazione può usare le [**funzioni GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questa funzione tramite l'interfaccia [**IOrpcDebugNotify.**](iorpcdebugnotify.md)

 

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

Puntatore a una [**struttura ORPC \_ DBG \_ ALL**](orpc-dbg-all.md) che contiene informazioni specifiche della notifica passate dal sistema RPC COM al debugger.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>N/D</dt> </dl> |
| Idl<br/>                      | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

