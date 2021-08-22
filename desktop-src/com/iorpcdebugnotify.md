---
title: Interfaccia IOrpcDebugNotify
description: Fornisce funzionalità di debug remoto.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- Interfaccia COM IOrpcDebugNotify
- Interfaccia COM IOrpcDebugNotify , descritta
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
ms.openlocfilehash: e3dd051819b70ae93b7c615d803e12134221d55ffbd464c60d5b9c41d983eb9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678581"
---
# <a name="iorpcdebugnotify-interface"></a>Interfaccia IOrpcDebugNotify

Fornisce funzionalità di debug remoto.

## <a name="when-to-implement"></a>Quando implementare

Implementare questa interfaccia per abilitare il debug remoto su RPC.

## <a name="when-to-use"></a>Utilizzo

Questa interfaccia deve essere usata per il debug remoto in-process quando le eccezioni software non devono essere usate per le notifiche del debugger COM. Consente ai debugger in-process di ricevere notifiche tramite chiamate dirette usando questi metodi.

## <a name="members"></a>Membri

**L'interfaccia IOrpcDebugNotify** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) **IOrpcDebugNotify** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IOrpcDebugNotify** include questi metodi.



| Metodo                                                              | Descrizione                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md)       | Invia i dati dal debugger client al debugger server.<br/>         |
| [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) | Recupera le dimensioni del buffer RPC dal debugger sul lato client.<br/>        |
| [**ClientNotify**](iorpcdebugnotify-clientnotify.md)               | Informa il client di una richiesta del debugger in uscita al server.<br/>   |
| [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)       | Invia i dati dal debugger del server al debugger client.<br/>         |
| [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) | Recupera le dimensioni del buffer RPC dal debugger lato server.<br/>        |
| [**ServerNotify**](iorpcdebugnotify-servernotify.md)               | Informa il server di una richiesta del debugger in ingresso dal client.<br/> |



 

## <a name="remarks"></a>Commenti

Una libreria di importazione contenente **l'interfaccia IOrpcDebugNotify** non è inclusa in Microsoft Windows Software Development Kit (SDK). Un'applicazione può usare le [**funzioni GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questi metodi tramite l'interfaccia **IOrpcDebugNotify.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>N/D</dt> </dl> |
| Idl<br/>                      | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ DBG \_ BUFFER**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> </dl>

 

