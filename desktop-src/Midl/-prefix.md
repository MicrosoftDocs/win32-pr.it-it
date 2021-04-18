---
title: opzione/prefix
description: L'opzione/prefix indica al compilatore MIDL di aggiungere stringhe di prefisso ai nomi di routine dello stub client e/o server.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- /prefix switch MIDL
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516354"
---
# <a name="prefix-switch"></a><span data-ttu-id="421d4-104">opzione/prefix</span><span class="sxs-lookup"><span data-stu-id="421d4-104">/prefix switch</span></span>

<span data-ttu-id="421d4-105">L'opzione **/Prefix** indica al compilatore MIDL di aggiungere stringhe di prefisso ai nomi di routine dello stub client e/o server.</span><span class="sxs-lookup"><span data-stu-id="421d4-105">The **/prefix** switch directs the MIDL compiler to add prefix strings to the client and/or server stub routine names.</span></span> <span data-ttu-id="421d4-106">Questo può essere usato per consentire a un singolo programma di essere sia un client che un server della stessa interfaccia, senza che i nomi di routine lato client e lato server siano in conflitto tra loro.</span><span class="sxs-lookup"><span data-stu-id="421d4-106">This can be used to allow a single program to be both a client and server of the same interface, without having the client- and server-side routine names conflict with each other.</span></span>

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a><span data-ttu-id="421d4-107">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="421d4-107">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span data-ttu-id="421d4-108"><span id="client"></span><span id="CLIENT"></span>client \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="421d4-108"><span id="client"></span><span id="CLIENT"></span>\*\*\*\*client\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="421d4-109">Influiscono solo sui nomi delle routine stub del client.</span><span class="sxs-lookup"><span data-stu-id="421d4-109">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span data-ttu-id="421d4-110"><span id="cstub"></span><span id="CSTUB"></span>cstub\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="421d4-110"><span id="cstub"></span><span id="CSTUB"></span>\*\*\*\*cstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="421d4-111">Uguale a *client*.</span><span class="sxs-lookup"><span data-stu-id="421d4-111">Same as *client*.</span></span> <span data-ttu-id="421d4-112">Influiscono solo sui nomi delle routine stub del client.</span><span class="sxs-lookup"><span data-stu-id="421d4-112">Affects only the client stub routine names.</span></span>

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="421d4-113"><span id="server"></span><span id="SERVER"></span>Server \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="421d4-113"><span id="server"></span><span id="SERVER"></span>\*\*\*\*server\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="421d4-114">Influiscono solo sui nomi di routine chiamati dalla routine stub del server.</span><span class="sxs-lookup"><span data-stu-id="421d4-114">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span data-ttu-id="421d4-115"><span id="sstub"></span><span id="SSTUB"></span>sstub \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="421d4-115"><span id="sstub"></span><span id="SSTUB"></span>\*\*\*\*sstub\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="421d4-116">Uguale a *Server*.</span><span class="sxs-lookup"><span data-stu-id="421d4-116">Same as *server*.</span></span> <span data-ttu-id="421d4-117">Influiscono solo sui nomi di routine chiamati dalla routine stub del server.</span><span class="sxs-lookup"><span data-stu-id="421d4-117">Affects only the routine names called by the server stub routine.</span></span>

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="421d4-118"><span id="switch"></span><span id="SWITCH"></span>Switch \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="421d4-118"><span id="switch"></span><span id="SWITCH"></span>\*\*\*\*switch\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="421d4-119">Influiscono su un prototipo aggiuntivo aggiunto al file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="421d4-119">Affects an extra prototype added to the header file.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="421d4-120"><span id="all"></span><span id="ALL"></span>tutti i \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="421d4-120"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="421d4-121">Influiscono sui nomi delle routine stub client e server.</span><span class="sxs-lookup"><span data-stu-id="421d4-121">Affects both the client and server stub routine names.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="421d4-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="421d4-122">Remarks</span></span>

<span data-ttu-id="421d4-123">Se il prefisso per le routine sul lato client è diverso dal prefisso per le routine lato server, il file di intestazione generato avrà sia i prototipi di routine lato client che i prototipi di routine lato server.</span><span class="sxs-lookup"><span data-stu-id="421d4-123">If the prefix for the client-side routines is different from the prefix for the server-side routines, the generated header file will have both client-side routine prototypes and server-side routine prototypes.</span></span>

<span data-ttu-id="421d4-124">L'opzione **/Prefix** è utile quando si usa un singolo file di intestazione con stub di più esecuzioni del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="421d4-124">The **/prefix** switch is useful when a single header file will be used with stubs from multiple runs of the MIDL compiler.</span></span> <span data-ttu-id="421d4-125">In questo modo vengono forzati i prototipi di routine aggiuntivi nel file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="421d4-125">This forces additional routine prototypes in the header file.</span></span>

<span data-ttu-id="421d4-126">In tutti i casi, i prefissi client, server e switch eseguiranno l'override di un prefisso all.</span><span class="sxs-lookup"><span data-stu-id="421d4-126">In all cases, the client, server, and switch prefixes will override an all prefix.</span></span>

## <a name="examples"></a><span data-ttu-id="421d4-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="421d4-127">Examples</span></span>

<span data-ttu-id="421d4-128">**"c \_ " Server "s \_ " del client MIDL/prefix**</span><span class="sxs-lookup"><span data-stu-id="421d4-128">**midl /prefix client "c\_" server "s\_"**</span></span>

<span data-ttu-id="421d4-129">**MIDL/Prefix All "Moo \_ "**</span><span class="sxs-lookup"><span data-stu-id="421d4-129">**midl /prefix all "moo\_"**</span></span>

<span data-ttu-id="421d4-130">**client MIDL/prefix "Bark \_ "**</span><span class="sxs-lookup"><span data-stu-id="421d4-130">**midl /prefix client "bark\_"**</span></span>

## <a name="see-also"></a><span data-ttu-id="421d4-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="421d4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="421d4-132">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="421d4-132">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




