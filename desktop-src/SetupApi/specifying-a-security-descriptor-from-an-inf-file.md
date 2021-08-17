---
description: È possibile controllare la capacità di un processo di accedere a oggetti a protezione diretta o di eseguire attività di amministrazione del sistema.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Specifica di un descrittore di sicurezza da un file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52267f443bf20fe8a9b71a64e2422ac43688d7a54bca2692f1b61ad891fda8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964837"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a>Specifica di un descrittore di sicurezza da un file INF

È possibile controllare la capacità di un processo di accedere a oggetti a protezione diretta o di eseguire attività di amministrazione del sistema. Un oggetto a protezione diretta è un oggetto che può avere un descrittore di sicurezza. Tutti gli oggetti denominati sono a protezione diretta. Alcuni oggetti senza nome, ad esempio gli oggetti processo e thread, possono avere anche descrittori di sicurezza. Per altre informazioni sul controllo dell'accesso agli oggetti a protezione diretta, vedere [Controllo di accesso](/windows/desktop/SecAuthZ/access-control).

[I descrittori di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) contengono le informazioni di sicurezza associate agli oggetti a protezione diretta. Per la maggior parte degli oggetti a protezione diretta, è possibile specificare il descrittore di sicurezza di un oggetto nella chiamata di funzione che crea l'oggetto. È ad esempio possibile specificare un descrittore di sicurezza nelle [**funzioni CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**e CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

Per impostare un descrittore di sicurezza da un file INF, aggiungere una sezione Security (Sicurezza) del writer INF immediatamente successiva alla sezione che installa il file, la chiave del Registro di sistema o il componente. La sezione Sicurezza deve contenere una riga con il descrittore di sicurezza della stringa scritto usando il formato per [Stringhe descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptor-strings). Anche la riga deve essere racchiusa tra virgolette (").

Ad esempio, il frammento di file INF seguente crea una chiave del Registro di sistema a cui solo gli amministratori e il sistema hanno accesso. Si noti che questo esempio richiede privilegi amministrativi.

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

In questo caso, il significato della stringa è che gli amministratori hanno il controllo completo, il sistema ha il controllo completo e l'accesso è ereditabile a tutte le sottochiavi. Per altre informazioni, vedere [Linguaggio di definizione del descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptor-definition-language).

 

 
