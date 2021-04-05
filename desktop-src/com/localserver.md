---
title: LocalServer
description: Specifica il percorso completo di un'applicazione server locale a 16 bit.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- LocalServer chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045058"
---
# <a name="localserver"></a><span data-ttu-id="d6ade-104">LocalServer</span><span class="sxs-lookup"><span data-stu-id="d6ade-104">LocalServer</span></span>

<span data-ttu-id="d6ade-105">Specifica il percorso completo di un'applicazione server locale a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="d6ade-105">Specifies the full path to a 16-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d6ade-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="d6ade-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a><span data-ttu-id="d6ade-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6ade-107">Remarks</span></span>

<span data-ttu-id="d6ade-108">Si tratta di un valore **reg \_ SZ** che specifica il percorso completo e può includere qualsiasi argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d6ade-108">This is a **REG\_SZ** value that specifies the full path and can include any command-line arguments.</span></span>

<span data-ttu-id="d6ade-109">COM aggiunge il flag "-Embedding" alla stringa, quindi l'applicazione che usa i flag deve analizzare l'intera stringa e verificare la presenza del flag-Embedding.</span><span class="sxs-lookup"><span data-stu-id="d6ade-109">COM appends the "-Embedding" flag to the string, so the application that uses flags must parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="d6ade-110">Per eseguire un server oggetto COM in uno spazio di memoria separato, modificare il valore di **LocalServer** come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="d6ade-110">To run a COM object server in a separate memory space, change the value of **LocalServer** as follows:</span></span>

<span data-ttu-id="d6ade-111">**cmd/c avviare/separate** *percorso \* \* *. exe**</span><span class="sxs-lookup"><span data-stu-id="d6ade-111">**cmd /c start /separate** *path\*\*\*.exe*\*</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6ade-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d6ade-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6ade-113">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="d6ade-113">**LocalServer32**</span></span>](localserver32.md)
</dt> </dl>

 

 




