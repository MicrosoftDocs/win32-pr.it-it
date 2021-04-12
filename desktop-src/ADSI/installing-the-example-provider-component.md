---
title: Installazione del componente provider di esempio
description: Dopo l'installazione di ADSI SDK, dalla directory di installazione passare alla \\ sottodirectory Samples NetDs \\ ADSI \\ Samples \\ \\ Setup provider. Eseguire Install.bat come descritto nel file di README.TXT.
ms.assetid: 7bf4bf22-38ac-4b0d-946e-5f60c7693707
ms.tgt_platform: multiple
keywords:
- Installazione del componente provider di esempio ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0df567aa08b03ce9c043d345380f05cd6d1c20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395286"
---
# <a name="installing-the-example-provider-component"></a><span data-ttu-id="94806-105">Installazione del componente provider di esempio</span><span class="sxs-lookup"><span data-stu-id="94806-105">Installing the Example Provider Component</span></span>

<span data-ttu-id="94806-106">Dopo l'installazione di ADSI SDK, dalla directory di installazione passare alla \\ sottodirectory Samples NetDs \\ ADSI \\ Samples \\ \\ Setup provider.</span><span class="sxs-lookup"><span data-stu-id="94806-106">After installing the ADSI SDK, from the installation directory, change directories to the Samples\\NetDs\\ADSI\\Samples\\Provider\\Setup subdirectory.</span></span> <span data-ttu-id="94806-107">Eseguire Install.bat come descritto nel file di README.TXT.</span><span class="sxs-lookup"><span data-stu-id="94806-107">Run Install.bat as described in the README.TXT file.</span></span>

<span data-ttu-id="94806-108">Il provider ADSI di esempio aggiungerà le sottochiavi e i valori seguenti al registro di sistema quando viene eseguito Install.bat file:</span><span class="sxs-lookup"><span data-stu-id="94806-108">The sample ADSI provider will add the following subkeys and values to the registry when Install.bat file is run:</span></span>

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

<span data-ttu-id="94806-109">Sono presenti altre voci del registro di sistema per il componente provider di esempio perché il componente provider di esempio ha implementato la gerarchia di directory nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="94806-109">Other registry entries for the example provider component exist because the example provider component implemented its directory hierarchy in the registry.</span></span> <span data-ttu-id="94806-110">Questo non implica che altri provider vogliano o debbano eseguire la stessa operazione.</span><span class="sxs-lookup"><span data-stu-id="94806-110">This in no way implies other providers would want to or should do the same.</span></span>

 

 




