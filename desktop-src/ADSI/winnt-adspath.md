---
title: ADsPath WinNT
description: Questo argomento contiene esempi di stringhe da usare per la ADsPath WinNT.
ms.assetid: 0fad4b34-5287-43a0-a172-a08955b8b132
ms.tgt_platform: multiple
keywords:
- Provider di servizi WinNT ADSI, WinNT ADsPath
- ADsPath ADSI, WinNT, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 906ea2c3db1b5234fb07045d921858766a105c4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955072"
---
# <a name="winnt-adspath"></a><span data-ttu-id="0793c-105">ADsPath WinNT</span><span class="sxs-lookup"><span data-stu-id="0793c-105">WinNT ADsPath</span></span>

<span data-ttu-id="0793c-106">La stringa ADsPath per il provider ADSI WinNT può essere una delle seguenti forme:</span><span class="sxs-lookup"><span data-stu-id="0793c-106">The ADsPath string for the ADSI WinNT provider can be one of the following forms:</span></span>


```C++
WinNT:
WinNT://<domain name>
WinNT://<domain name>/<server>
WinNT://<domain name>/<path>
WinNT://<domain name>/<object name>
WinNT://<domain name>/<object name>,<object class>
WinNT://<server>
WinNT://<server>/<object name>
WinNT://<server>/<object name>,<object class>
```



<span data-ttu-id="0793c-107">Il nome di dominio può essere un nome NETBIOS o un nome DNS.</span><span class="sxs-lookup"><span data-stu-id="0793c-107">The domain name can be either a NETBIOS name or a DNS name.</span></span>

<span data-ttu-id="0793c-108">Il server è il nome di un server specifico all'interno del dominio.</span><span class="sxs-lookup"><span data-stu-id="0793c-108">The server is the name of a specific server within the domain.</span></span>

<span data-ttu-id="0793c-109">Il percorso è il percorso dell'oggetto, ad esempio "printserver1/Printer2".</span><span class="sxs-lookup"><span data-stu-id="0793c-109">The path is the path of on object, such as "printserver1/printer2".</span></span>

<span data-ttu-id="0793c-110">Il nome dell'oggetto è il nome di un oggetto specifico.</span><span class="sxs-lookup"><span data-stu-id="0793c-110">The object name is the name of a specific object.</span></span>

<span data-ttu-id="0793c-111">La classe Object è il nome della classe dell'oggetto denominato.</span><span class="sxs-lookup"><span data-stu-id="0793c-111">The object class is the class name of the named object.</span></span> <span data-ttu-id="0793c-112">Un esempio di questo utilizzo è "WinNT://MyServer/JeffSmith,user".</span><span class="sxs-lookup"><span data-stu-id="0793c-112">One example of this usage would be "WinNT://MyServer/JeffSmith,user".</span></span> <span data-ttu-id="0793c-113">La specifica di un nome di classe può migliorare le prestazioni dell'operazione di associazione.</span><span class="sxs-lookup"><span data-stu-id="0793c-113">Specifying a class name can improve the performance of the bind operation.</span></span>

 

 




