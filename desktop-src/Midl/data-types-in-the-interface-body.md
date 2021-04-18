---
title: Tipi di dati nel corpo dell'interfaccia
description: Il corpo dell'interfaccia racchiuso tra parentesi graffe () contiene i tipi di dati che verranno utilizzati nelle chiamate a procedure remote e nei prototipi per le funzioni che verranno eseguite in modalità remota.
ms.assetid: a5130744-6b14-48a4-b439-16f0ecaf08c2
keywords:
- interfacce MIDL, tipi di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5bdbbb90c4cbecd4a6a4e3cc74ba9775772dd0a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297979"
---
# <a name="data-types-in-the-interface-body"></a><span data-ttu-id="844a3-104">Tipi di dati nel corpo dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="844a3-104">Data Types in the Interface Body</span></span>

<span data-ttu-id="844a3-105">Il corpo dell'interfaccia racchiuso tra parentesi graffe ({}) contiene i tipi di dati che verranno utilizzati nelle chiamate a procedure remote e nei prototipi per le funzioni che verranno eseguite in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="844a3-105">The interface body, which is enclosed in braces ({ }), contains the data types that will be used in remote procedure calls and prototypes for the functions that will be executed remotely.</span></span> <span data-ttu-id="844a3-106">Il corpo di un'interfaccia può contenere importazioni, pragma, dichiarazioni di costanti, dichiarazioni di tipo e dichiarazioni di funzione.</span><span class="sxs-lookup"><span data-stu-id="844a3-106">An interface body can contain imports, pragmas, constant declarations, type declarations, and function declarations.</span></span> <span data-ttu-id="844a3-107">Fatta eccezione per la modalità di compatibilità OSF, il compilatore MIDL consente anche dichiarazioni implicite sotto forma di definizioni di variabili.</span><span class="sxs-lookup"><span data-stu-id="844a3-107">Except in OSF-compatibility mode, the MIDL compiler also allows implicit declarations in the form of variable definitions.</span></span>

<span data-ttu-id="844a3-108">Si noti che la specifica OSF-DCE per le interfacce RPC non consente più interfacce in un unico file IDL.</span><span class="sxs-lookup"><span data-stu-id="844a3-108">Note that the OSF-DCE specification for RPC interfaces does not allow multiple interfaces in a single IDL file.</span></span> <span data-ttu-id="844a3-109">Pertanto, se si esegue la compilazione in modalità di compatibilità OSF ( [**/OSF**](-osf.md)) di MIDL, il file IDL può contenere una sola interfaccia.</span><span class="sxs-lookup"><span data-stu-id="844a3-109">Therefore, if you are compiling in MIDL's OSF-compatibility mode ( [**/osf**](-osf.md)), your IDL file can contain only one interface.</span></span>

<span data-ttu-id="844a3-110">Per informazioni dettagliate sull'uso del compilatore MIDL per produrre librerie dei tipi, vedere [generazione di una libreria dei tipi con MIDL](generating-a-type-library-with-midl-2.md).</span><span class="sxs-lookup"><span data-stu-id="844a3-110">For details on using the MIDL compiler to produce type libraries, see [Generating a Type Library with MIDL](generating-a-type-library-with-midl-2.md).</span></span>

<span data-ttu-id="844a3-111">In Microsoft RPC, un file IDL può contenere più interfacce e queste interfacce possono essere dichiarate in modo diretto (all'interno del file IDL che le definisce).</span><span class="sxs-lookup"><span data-stu-id="844a3-111">In Microsoft RPC, an IDL file can contain multiple interfaces and these interfaces can be forward declared (within the IDL file that defines them).</span></span> <span data-ttu-id="844a3-112">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="844a3-112">For example:</span></span>

``` syntax
interface ITwo; //forward declaration
interface IOne 
{
...uses ITwo...
}
interface ITwo 
{
...uses IOne...
}
```

 

 




