---
title: Installazione del componente provider di esempio
description: Dopo aver installato ADSI SDK, dalla directory di installazione passare alla sottodirectory Samples \\ NetDs \\ ADSI \\ Samples Provider \\ \\ Setup. Eseguire Install.bat come descritto nel file README.TXT.
ms.assetid: 7bf4bf22-38ac-4b0d-946e-5f60c7693707
ms.tgt_platform: multiple
keywords:
- Installazione del componente del provider di esempio ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e58fb471385b862982904e69a432bec1a94e3b9aff0248fdacd9f5e9c7a3e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333241"
---
# <a name="installing-the-example-provider-component"></a>Installazione del componente provider di esempio

Dopo aver installato ADSI SDK, dalla directory di installazione passare alla sottodirectory Samples \\ NetDs \\ ADSI \\ Samples Provider \\ \\ Setup. Eseguire Install.bat come descritto nel file README.TXT.

Il provider ADSI di esempio aggiungerà le sottochiavi e i valori seguenti al Registro di sistema Install.bat viene eseguito il file :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               Sample = SampleNamespace
```

```
HKEY_CLASSES_ROOT
   SampleNamespace
      Clsid = {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   Sample
      Clsid = {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Namespace Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = SampleNamespace
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Provider Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = Sample
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

Esistono altre voci del Registro di sistema per il componente provider di esempio perché il componente provider di esempio ha implementato la gerarchia di directory nel Registro di sistema. Ciò non implica in alcun modo che altri provider vogliano o debbano eseguire la stessa operazione.

 

 




