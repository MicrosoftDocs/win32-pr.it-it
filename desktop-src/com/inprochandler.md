---
title: InprocHandler
description: InprocHandler specifica se un'applicazione usa un gestore personalizzato nella HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID del Registro di sistema.
ms.assetid: b371b331-148b-46f2-a21e-b88b285bcfc9
keywords:
- Com della chiave del Registro di sistema InprocHandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1159ad4fd1f41edda75509d5bea5491f89b83ac80aa21ff969dfa1fa9aff6d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919108"
---
# <a name="inprochandler"></a>InprocHandler

Specifica se un'applicazione usa un gestore personalizzato.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocHandler = handler.dll
```

## <a name="remarks"></a>Commenti

Si tratta di **un \_ valore REG SZ** che specifica il gestore personalizzato usato dall'applicazione. Se non viene usato un gestore personalizzato, la voce deve essere impostata su Ole32.dll.

Se un contenitore cerca nel Registro di sistema un gestore personalizzato, la versione a 16 bit ha priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**InprocHandler32**](inprochandler32.md)
</dt> </dl>

 

 




