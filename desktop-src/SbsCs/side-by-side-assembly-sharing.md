---
description: Nella figura seguente viene illustrato il modo in cui due applicazioni possono condividere un assembly utilizzando il metodo tradizionale di condivisione degli assembly.
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: Condivisione di assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a94295baf2c29733c0ec366f9476a4dbf5cc3f40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968303"
---
# <a name="side-by-side-assembly-sharing"></a><span data-ttu-id="577ec-103">Condivisione di assembly affiancati</span><span class="sxs-lookup"><span data-stu-id="577ec-103">Side-by-side Assembly Sharing</span></span>

<span data-ttu-id="577ec-104">Nella figura seguente viene illustrato il modo in cui due applicazioni possono condividere un assembly utilizzando il metodo tradizionale di condivisione degli assembly.</span><span class="sxs-lookup"><span data-stu-id="577ec-104">The following figure illustrates how two applications might share an assembly using the traditional method of assembly sharing.</span></span> <span data-ttu-id="577ec-105">Un problema con la condivisione di assembly tradizionale si verifica quando un'applicazione installa una versione di un assembly, in genere una DLL, che non è compatibile con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="577ec-105">A problem with traditional assembly sharing occurs when an application installs a version of an assembly—commonly a DLL—that is not backward compatible.</span></span> <span data-ttu-id="577ec-106">L'applicazione appena installata funziona, ma le applicazioni che dipendono dalla versione precedente della DLL potrebbero non funzionare più.</span><span class="sxs-lookup"><span data-stu-id="577ec-106">The application just installed works, but applications that depended on the previous DLL version may no longer work.</span></span>

![rappresentazione di due applicazioni che condividono un assembly](images/sxs1.png)

<span data-ttu-id="577ec-108">L'applicazione isolata e la soluzione assembly side-by-side consentono l'esecuzione contemporanea di versioni diverse dello stesso assembly Win32 nello stesso sistema senza conflitti.</span><span class="sxs-lookup"><span data-stu-id="577ec-108">The isolated application and side-by-side assembly solution enables different versions of the same Win32 assembly to run at the same time on the same system without conflict.</span></span> <span data-ttu-id="577ec-109">Specificando la versione dell'assembly affiancata che l'applicazione deve utilizzare, gli sviluppatori possono garantire che la configurazione testata venga sempre duplicata nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="577ec-109">By specifying which side-by-side assembly version the application should use, developers can guarantee that the configuration they test will always be duplicated on the user's computer.</span></span> <span data-ttu-id="577ec-110">La condivisione affiancata è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="577ec-110">Side-by-side sharing is illustrated in the following figure.</span></span>

![implementazione della condivisione di assembly side-by-side](images/sxs2.png)

<span data-ttu-id="577ec-112">Per ulteriori informazioni, vedere [informazioni sulle applicazioni isolate e gli assembly affiancati](about-isolated-applications-and-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="577ec-112">For more information, see [About Isolated Applications and Side-by-side Assemblies](about-isolated-applications-and-side-by-side-assemblies.md).</span></span>

 

 



