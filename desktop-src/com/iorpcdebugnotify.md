---
title: Interfaccia IOrpcDebugNotify
description: Fornisce funzionalità di debug remoto.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- Interfaccia COM IOrpcDebugNotify
- Interfaccia IOrpcDebugNotify COM, descritta
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519054"
---
# <a name="iorpcdebugnotify-interface"></a>Interfaccia IOrpcDebugNotify

Fornisce funzionalità di debug remoto.

## <a name="when-to-implement"></a>Quando implementare

Implementare questa interfaccia per abilitare il debug remoto tramite RPC.

## <a name="when-to-use"></a>Utilizzo

Questa interfaccia deve essere utilizzata per il debug remoto in-process quando le eccezioni software non devono essere utilizzate per le notifiche del debugger COM. Consente ai debugger in-process di ricevere notifiche tramite chiamate dirette usando questi metodi.

## <a name="members"></a>Membri

L'interfaccia **IOrpcDebugNotify** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . **IOrpcDebugNotify** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IOrpcDebugNotify** dispone di questi metodi.



| Metodo                                                              | Descrizione                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)       | Invia i dati dal debugger client al debugger del server.<br/>         |
| [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) | Recupera la dimensione del buffer RPC dal debugger sul lato client.<br/>        |
| [**ClientNotify**](iorpcdebugnotify-clientnotify.md)               | Informa il client di una richiesta del debugger in uscita al server.<br/>   |
| [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)       | Invia i dati dal debugger del server al debugger client.<br/>         |
| [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) | Recupera la dimensione del buffer RPC dal debugger lato server.<br/>        |
| [**ServerNotify**](iorpcdebugnotify-servernotify.md)               | Informa il server di una richiesta del debugger in ingresso dal client.<br/> |



 

## <a name="remarks"></a>Commenti

Una libreria di importazione contenente l'interfaccia **IOrpcDebugNotify** non è inclusa nel Software Development Kit (SDK) di Microsoft Windows. Un'applicazione può usare le funzioni [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questi metodi tramite l'interfaccia **IOrpcDebugNotify** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>N/D</dt> </dl> |
| IDL<br/>                      | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**ORPC \_ dbg \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**\_buffer dbg \_ ORPC**](orpc-dbg-buffer.md)
</dt> <dt>

[**\_argomenti init \_ ORPC**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> </dl>

 

