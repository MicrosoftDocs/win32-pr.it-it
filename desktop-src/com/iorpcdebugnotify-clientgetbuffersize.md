---
title: Metodo IOrpcDebugNotify ClientGetBufferSize
description: Recupera la dimensione del buffer RPC dal debugger sul lato client.
ms.assetid: 05475156-1508-4eb2-82a6-bb1701839fbd
keywords:
- Metodo ClientGetBufferSize COM
- Metodo ClientGetBufferSize COM, interfaccia IOrpcDebugNotify
- Interfaccia IOrpcDebugNotify COM, metodo ClientGetBufferSize
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bd925b9c518c78ca37aa8219a00965f398c415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302662"
---
# <a name="iorpcdebugnotifyclientgetbuffersize-method"></a>Metodo IOrpcDebugNotify:: ClientGetBufferSize

Recupera la dimensione del buffer RPC dal debugger sul lato client.

> [!Note]  
> Una libreria di importazione contenente la funzione **ClientGetBufferSize** non è inclusa in Microsoft Windows Software Development Kit (SDK). Un'applicazione può usare le funzioni [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questa funzione tramite l'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

## <a name="syntax"></a>Sintassi


```C++
void ClientGetBufferSize(
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

 

