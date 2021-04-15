---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Determina se RPCSS aggiunge automaticamente \_ \_ per impostazione predefinita un SID di tutti i pacchetti dell'applicazione a restrizioni com.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395435"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>DoNotAddAllApplicationPackagesToRestrictions

Determina se RPCSS aggiunge automaticamente \_ \_ per impostazione predefinita un SID di tutti i pacchetti dell'applicazione a restrizioni com.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore | Descrizione                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | Disabilita le app di Windows Store durante la migrazione da Windows 7 a Windows 8.                   |
| 1     | Non aggiunge il SID tutti \_ i \_ pacchetti dell'applicazione alle restrizioni com. Questo è il valore predefinito. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




