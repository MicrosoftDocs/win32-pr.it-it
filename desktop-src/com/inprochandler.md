---
title: InprocHandler
description: Specifica se un'applicazione utilizza un gestore personalizzato.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- InprocHandler chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8c19089ece43496465351b44e9faa8793ba893
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396495"
---
# <a name="inprochandler"></a>InprocHandler

Specifica se un'applicazione utilizza un gestore personalizzato.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** che specifica il gestore personalizzato usato dall'applicazione. Se non viene utilizzato un gestore personalizzato, la voce deve essere impostata su Ole32.dll.

Se un contenitore esegue una ricerca nel registro di sistema per un gestore personalizzato, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 




