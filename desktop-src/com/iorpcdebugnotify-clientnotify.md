---
title: Metodo IOrpcDebugNotify ClientNotify
description: Informa il client di una richiesta del debugger in uscita al server.
ms.assetid: a41e3eaa-6d1f-46bf-9103-f83e45b2cd90
keywords:
- Metodo ClientNotify COM
- Metodo ClientNotify COM, interfaccia IOrpcDebugNotify
- Interfaccia IOrpcDebugNotify COM, metodo ClientNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e788a51e278df09715aaf9d4993ac5724ed65b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479192"
---
# <a name="iorpcdebugnotifyclientnotify-method"></a>Metodo IOrpcDebugNotify:: ClientNotify

Informa il client di una richiesta del debugger in uscita al server.

> [!Note]  
> Una libreria di importazione contenente la funzione **ClientNotify** non è inclusa in Microsoft Windows Software Development Kit (SDK). Un'applicazione può usare le funzioni [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questa funzione tramite l'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

## <a name="syntax"></a>Sintassi


```C++
void ClientNotify(
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

 

