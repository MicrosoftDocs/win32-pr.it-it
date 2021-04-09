---
title: InprocServer
description: Specifica il percorso della DLL del server in-process.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- InprocServer chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5682693d711f734bbc60def8a711f11e2bad0ef9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955457"
---
# <a name="inprocserver"></a>InprocServer

Specifica il percorso della DLL del server in-process.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      InprocServer
         (Default) = path
```

## <a name="remarks"></a>Commenti

La voce **InprocServer** è relativamente rara per le classi inseribili.

I server in-process sono attualmente registrati usando la voce del registro di sistema **InprocServer** . I server in-process a 32 e 64 bit devono usare la voce [**InprocServer32**](inprocserver32.md) . Se un contenitore esegue una ricerca nel registro di sistema per un server in-process, la versione a 16 bit ha la priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**InprocServer32**](inprocserver32.md)
</dt> </dl>

 

 




