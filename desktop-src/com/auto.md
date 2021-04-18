---
title: Auto
description: Determina se il debugger viene avviato automaticamente quando viene inviata una notifica RPC COM.
ms.assetid: e05ae7cb-79d1-4543-aef3-9397548c2030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c7730c3c6e0fe9dc01b43a7c4f9621897f9f16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298959"
---
# <a name="auto"></a>Auto

Determina se il debugger viene avviato automaticamente quando viene inviata una notifica RPC COM.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\DebugObjectRPCEnabled\AeDebug
   Auto = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ Word** .



| Valore | Descrizione                    |
|-------|--------------------------------|
| 1     | Avvia automaticamente il debugger. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> <dt>

[**ORPC \_ dbg \_ All**](orpc-dbg-all.md)
</dt> </dl>

 

 




