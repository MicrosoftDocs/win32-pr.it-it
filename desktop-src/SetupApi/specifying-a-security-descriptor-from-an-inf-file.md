---
description: È possibile controllare la capacità di un processo di accedere agli oggetti a protezione diretta o di eseguire attività di amministrazione del sistema.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Specifica di un descrittore di sicurezza da un file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968500"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a>Specifica di un descrittore di sicurezza da un file INF

È possibile controllare la capacità di un processo di accedere agli oggetti a protezione diretta o di eseguire attività di amministrazione del sistema. Un oggetto a protezione diretta è un oggetto che può disporre di un descrittore di sicurezza. Tutti gli oggetti denominati sono entità a protezione diretta. Alcuni oggetti senza nome, ad esempio gli oggetti processo e thread, possono avere anche descrittori di sicurezza. Per ulteriori informazioni sul controllo dell'accesso agli oggetti a protezione diretta, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control).

I [descrittori di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) contengono le informazioni di sicurezza associate agli oggetti a protezione diretta. Per la maggior parte degli oggetti a protezione diretta, è possibile specificare un descrittore di sicurezza di un oggetto nella chiamata di funzione che crea l'oggetto. È ad esempio possibile specificare un descrittore di sicurezza nelle funzioni [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

Per impostare un descrittore di sicurezza da un file INF, aggiungere una sezione sicurezza creata dal writer INF immediatamente dopo la sezione che consente di installare il file, la chiave del registro di sistema o il componente. La sezione Security deve contenere una riga con il descrittore di sicurezza della stringa scritta usando il formato per le [stringhe del descrittore di sicurezza](/windows/desktop/SecAuthZ/security-descriptor-strings). La riga deve anche essere racchiusa tra virgolette (").

Il frammento di file INF seguente, ad esempio, creerà una chiave del registro di sistema a cui possono accedere solo gli amministratori e il sistema. Si noti che questo esempio richiede privilegi amministrativi.

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

In questo caso, il significato della stringa è che gli amministratori hanno il controllo completo, il sistema dispone di controllo completo e l'accesso è ereditabile a tutte le sottochiavi. Per ulteriori informazioni, vedere [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).

 

 
