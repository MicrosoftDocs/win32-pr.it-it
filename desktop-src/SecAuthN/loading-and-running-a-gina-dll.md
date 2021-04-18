---
description: Windows carica ed esegue la DLL standard di Microsoft GINA (MSGina.dll). Per caricare un'altra GINA, è necessario modificare un valore della chiave del registro di sistema.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Caricamento ed esecuzione di una DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6242ac0124d85d280d951cbc0bfbdbe748fde0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313288"
---
# <a name="loading-and-running-a-gina-dll"></a>Caricamento ed esecuzione di una DLL GINA

Windows carica ed esegue la DLL standard di Microsoft GINA (MSGina.dll). Per caricare un'altra [*Gina*](../secgloss/g-gly.md), è necessario modificare il valore della chiave del registro di sistema seguente:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

Se il valore della chiave GinaDLL è presente, deve contenere il nome di una DLL GINA, che verrà caricata e utilizzata da [*Winlogon*](../secgloss/w-gly.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione e test di una DLL GINA](building-and-testing-a-gina-dll.md)
</dt> <dt>

[Funzioni di esportazione GINA](authentication-functions.md)
</dt> <dt>

[Strutture GINA](authentication-structures.md)
</dt> <dt>

[Funzioni di Servizi terminal GINA](terminal-services-gina-functions.md)
</dt> </dl>

 

 
