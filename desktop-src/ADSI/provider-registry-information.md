---
title: Informazioni sul Registro di sistema del provider
description: Questo argomento illustra le chiavi e i valori da impostare quando si aggiunge un provider ADSI.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813ad37d77d532e3c9bec91bcc3eda1f0aaf703f09dd3cf1b61ac059d7d7493b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838867"
---
# <a name="provider-registry-information"></a>Informazioni sul Registro di sistema del provider

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

Nei paragrafi precedenti, il *provider* è l'identificatore dell'oggetto di primo livello del provider. Lo *spazio dei nomi* del provider è l'identificatore dell'oggetto che implementa lo spazio dei nomi del provider.

Per un esempio specifico, vedere [Installazione del componente provider di esempio](installing-the-example-provider-component.md).

 

 




