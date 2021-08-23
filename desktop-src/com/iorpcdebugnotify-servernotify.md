---
title: Metodo IOrpcDebugNotify ServerNotify
description: Informa il server di una richiesta del debugger in ingresso dal client.
ms.assetid: 6c868b9e-f25b-4d27-80ff-697d0c005b8d
keywords:
- Metodo ServerNotify COM
- Metodo ServerNotify COM , interfaccia IOrpcDebugNotify
- Interfaccia IOrpcDebugNotify COM , metodo ServerNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff0faac4ee4e5fa691088afa9de8871a8bf9382ce3da629b3fc14dd9d932ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048099"
---
# <a name="iorpcdebugnotifyservernotify-method"></a>Metodo IOrpcDebugNotify::ServerNotify

Informa il server di una richiesta del debugger in ingresso dal client.

> [!Note]  
> Una libreria di importazione contenente **la funzione ServerNotify** non è inclusa in Microsoft Windows Software Development Kit (SDK). Un'applicazione può usare le funzioni [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questa funzione tramite l'interfaccia [**IOrpcDebugNotify.**](iorpcdebugnotify.md)

 

## <a name="syntax"></a>Sintassi


```C++
void ServerNotify(
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

[**ARGOMENTI \_ ORPC INIT \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

