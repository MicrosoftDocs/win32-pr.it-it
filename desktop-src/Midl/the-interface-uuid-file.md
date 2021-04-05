---
title: File UUID dell'interfaccia
description: Il file UUID dell'interfaccia raccoglie le definizioni degli identificatori di interfaccia da tutte le interfacce del file IDL elaborato.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL e COM MIDL, interfacce, file UUID proxy
- file UUID dell'interfaccia MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713456"
---
# <a name="the-interface-uuid-file"></a><span data-ttu-id="744bf-105">File UUID dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="744bf-105">The Interface UUID File</span></span>

<span data-ttu-id="744bf-106">Il file UUID dell'interfaccia raccoglie le definizioni degli identificatori di interfaccia da tutte le interfacce del file IDL elaborato.</span><span class="sxs-lookup"><span data-stu-id="744bf-106">The interface UUID file collects the definitions of the interface identifiers from all interfaces in the processed IDL file.</span></span> <span data-ttu-id="744bf-107">Analogamente al file stub e al file di intestazione, la chiusura del flusso di input è definita dal file IDL corrente e dai file inclusi.</span><span class="sxs-lookup"><span data-stu-id="744bf-107">Similar to the stub file and the header file, the input stream closure is defined by the current IDL file and the included files.</span></span> <span data-ttu-id="744bf-108">Ad esempio, per l'interfaccia IFace, il compilatore genera un IID costante \_ IFace e lo inizializza sull'UUID dell'interfaccia specificato nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="744bf-108">For example, for Interface IFace, the compiler generates a constant IID\_IFace and initializes it to the interface's UUID specified in the IDL file.</span></span> <span data-ttu-id="744bf-109">Le applicazioni client e la DLL proxy utilizzano questa costante per identificare l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="744bf-109">Client applications and the proxy DLL use this constant to identify the interface.</span></span>

<span data-ttu-id="744bf-110">Il nome predefinito per un file IID di interfaccia generato da un file. idl è il file \_ i.c.</span><span class="sxs-lookup"><span data-stu-id="744bf-110">The default name for an interface IID file generated from a file.idl is File\_i.c.</span></span> <span data-ttu-id="744bf-111">L'opzione del compilatore MIDL [**/IID**](-iid.md) sostituisce il nome predefinito del file UUID dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="744bf-111">The [**/iid**](-iid.md) MIDL compiler switch overrides the default name of the interface UUID file.</span></span>

 

 




