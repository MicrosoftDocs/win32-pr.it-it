---
title: InprocServer
description: Specifica il percorso della DLL del server in-process.
ms.assetid: f14cc8f7-e93e-4db8-8b0d-ea77a6301f33
keywords:
- InprocServer chiave del Registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b6cd1c7ab32733687292f01ddb48167c68243c62345fb17af3b6533a5cb454d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029891"
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

La **voce InprocServer** è relativamente rara per le classi inseribili.

I server in-process sono attualmente registrati usando la **voce del Registro di sistema InprocServer.** I server in-process a 32 bit e a 64 bit devono usare la [**voce InprocServer32.**](inprocserver32.md) Se un contenitore cerca un server in-process nel Registro di sistema, la versione a 16 bit ha priorità con un contenitore a 16 bit e la versione a 32 bit ha la priorità con un contenitore a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**InprocServer32**](inprocserver32.md)
</dt> </dl>

 

 




