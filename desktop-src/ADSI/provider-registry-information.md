---
title: Informazioni del registro di sistema del provider
description: In questo argomento vengono illustrate le chiavi e i valori che è necessario impostare quando si aggiunge un provider ADSI.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790a80964bdcc6111a4c167056a0b85bda23e147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395278"
---
# <a name="provider-registry-information"></a>Informazioni del registro di sistema del provider

Il provider viene registrato con ADSI con le chiavi e i valori seguenti:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

Il provider viene registrato con Windows con le chiavi e i valori seguenti:

```
HKEY_CLASSES_ROOT
   provider
      Clsid
         (Default) = <provider CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider DLL filename>
            ThreadingModel = Both
         ProgID = <provider object name>
         TypeLib = <provider TypeLib CLSID>
         Version = <provider version number>
```

Lo spazio dei nomi del provider viene registrato con Windows con le chiavi e i valori seguenti:

```
HKEY_CLASSES_ROOT
   provider namespace
      Clsid
         (Default) = <provider namespace CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider namespace CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider namespace DLL filename>
            ThreadingModel = Both
         ProgID = <provider namespace object name>
         TypeLib = <provider namespace TypeLib CLSID>
         Version = <provider namespace version number>
```

Nei paragrafi precedenti, il *provider* è l'identificatore dell'oggetto di primo livello del provider. Lo *spazio dei nomi del provider* è l'identificatore dell'oggetto che implementa lo spazio dei nomi del provider.

Per un esempio specifico, vedere [installazione del componente provider di esempio](installing-the-example-provider-component.md).

 

 




