---
title: Estrazione degli esempi di codice
description: Sebbene gli esempi di codice siano divisi in una serie di lezioni di esercitazione, è possibile estrarre facilmente i raggruppamenti di esempio appropriati dalla raccolta.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395718"
---
# <a name="extracting-the-code-samples"></a><span data-ttu-id="100ec-103">Estrazione degli esempi di codice</span><span class="sxs-lookup"><span data-stu-id="100ec-103">Extracting the Code Samples</span></span>

<span data-ttu-id="100ec-104">Sebbene gli esempi di codice siano divisi in una serie di lezioni di esercitazione, è possibile estrarre facilmente i raggruppamenti di esempio appropriati dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="100ec-104">Though the code samples are divided into a series of tutorial lessons, the appropriate sample groupings can easily be extracted from the collection.</span></span> <span data-ttu-id="100ec-105">La maggior parte delle singole directory di esempio è concepita per funzionare insieme ad almeno un'altra directory di esempio.</span><span class="sxs-lookup"><span data-stu-id="100ec-105">Most of the individual sample directories are meant to work in conjunction with at least one other sample directory.</span></span> <span data-ttu-id="100ec-106">Gli esempi correlati ai componenti sono costituiti da una coppia client e server, con il server che richiede l'uso dell'utilità di registrazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="100ec-106">The component-related samples consist of a client and server pair, with the server requiring the use of the REGISTER sample utility.</span></span> <span data-ttu-id="100ec-107">Ecco un riepilogo dei raggruppamenti di esempio e come estrarre ogni gruppo come unità compilabile.</span><span class="sxs-lookup"><span data-stu-id="100ec-107">Here is a summary of the sample groupings and how to extract each group as a buildable unit.</span></span> <span data-ttu-id="100ec-108">Per ogni raggruppamento di esempio, copiare il contenuto delle directory visualizzate.</span><span class="sxs-lookup"><span data-stu-id="100ec-108">For each sample grouping, copy the content of the directories shown.</span></span> <span data-ttu-id="100ec-109">La \[ \] directory di destinazione padre visualizzata non richiede alcun contenuto dal branch degli esempi.</span><span class="sxs-lookup"><span data-stu-id="100ec-109">The parent \[destination\] directory shown requires no content from the samples branch.</span></span> <span data-ttu-id="100ec-110">Tuttavia, i menu della guida negli esempi in esecuzione presuppongono che l'esercitazione appropriata. I file della Guida HTM si trovano in questa \[ directory di destinazione padre \] .</span><span class="sxs-lookup"><span data-stu-id="100ec-110">However, the help menus in the running samples do assume that the appropriate tutorial .HTM help files are located in this parent \[destination\] directory.</span></span>

<span data-ttu-id="100ec-111">Per l'applicazione Win32 READTUT:</span><span class="sxs-lookup"><span data-stu-id="100ec-111">For the Win32 READTUT application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

<span data-ttu-id="100ec-112">Per l'applicazione Win32 EXE Skeleton:</span><span class="sxs-lookup"><span data-stu-id="100ec-112">For the Win32 EXE skeleton application:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

<span data-ttu-id="100ec-113">Per lo scheletro della DLL Win32:</span><span class="sxs-lookup"><span data-stu-id="100ec-113">For the Win32 DLL skeleton:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

<span data-ttu-id="100ec-114">Per gli esempi di oggetti COM di base:</span><span class="sxs-lookup"><span data-stu-id="100ec-114">For the basic COM object samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

<span data-ttu-id="100ec-115">Per gli esempi client/server del componente DLL di base in-process:</span><span class="sxs-lookup"><span data-stu-id="100ec-115">For the basic in-process DLL component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

<span data-ttu-id="100ec-116">Per gli esempi client/server del componente con licenza:</span><span class="sxs-lookup"><span data-stu-id="100ec-116">For the licensed component client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

<span data-ttu-id="100ec-117">Per gli esempi di marshalling standard:</span><span class="sxs-lookup"><span data-stu-id="100ec-117">For the standard marshaling samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

<span data-ttu-id="100ec-118">Per gli esempi client/server locali out-of-process:</span><span class="sxs-lookup"><span data-stu-id="100ec-118">For the out-of-process local client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

<span data-ttu-id="100ec-119">Per gli esempi client/server del modello di Apartment:</span><span class="sxs-lookup"><span data-stu-id="100ec-119">For the apartment model client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

<span data-ttu-id="100ec-120">Per gli esempi client/server DCOM (Distributed COM):</span><span class="sxs-lookup"><span data-stu-id="100ec-120">For the DCOM (Distributed COM) client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

<span data-ttu-id="100ec-121">Per gli esempi client/server di threading gratuiti:</span><span class="sxs-lookup"><span data-stu-id="100ec-121">For the free threading client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

<span data-ttu-id="100ec-122">Per gli esempi client/server di oggetti COM collegabili:</span><span class="sxs-lookup"><span data-stu-id="100ec-122">For the connectable COM object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

<span data-ttu-id="100ec-123">Per gli esempi client/server di archiviazione strutturata:</span><span class="sxs-lookup"><span data-stu-id="100ec-123">For the structured storage client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

<span data-ttu-id="100ec-124">Per gli esempi client/server di oggetti permanenti:</span><span class="sxs-lookup"><span data-stu-id="100ec-124">For the persistent object client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

<span data-ttu-id="100ec-125">Per gli esempi client/server di sicurezza DCOM:</span><span class="sxs-lookup"><span data-stu-id="100ec-125">For the DCOM security client/server samples:</span></span>

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




