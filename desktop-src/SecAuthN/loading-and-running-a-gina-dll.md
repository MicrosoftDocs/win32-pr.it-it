---
description: Windows carica ed esegue la DLL STANDARD MICROSOFT GINA (MSGina.dll). Per caricare un file GINA diverso, è necessario modificare un valore di chiave del Registro di sistema.
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: Caricamento ed esecuzione di una DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a4e8d68a1e1846a28e1db9402d730834768a132a7c502021fd101f20926f54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140954"
---
# <a name="loading-and-running-a-gina-dll"></a>Caricamento ed esecuzione di una DLL GINA

Windows carica ed esegue la DLL STANDARD MICROSOFT GINA (MSGina.dll). Per caricare un file [*GINA diverso,*](../secgloss/g-gly.md)è necessario modificare il valore della chiave del Registro di sistema seguente:

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

Se il valore della chiave GinaDLL è presente, deve contenere il nome di una DLL GINA, che Verrà caricata e utilizzata da [*Winlogon.*](../secgloss/w-gly.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione e test di una DLL GINA](building-and-testing-a-gina-dll.md)
</dt> <dt>

[Funzioni di esportazione DI GINA](authentication-functions.md)
</dt> <dt>

[Strutture DI GINA](authentication-structures.md)
</dt> <dt>

[Funzioni GINA di Servizi terminal](terminal-services-gina-functions.md)
</dt> </dl>

 

 
