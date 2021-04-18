---
title: Creazione del plug-in per un negozio online di tipo 1
description: Creazione del plug-in per un negozio online di tipo 1
ms.assetid: 5d38a41f-9859-452b-953f-3449c2b0ce06
keywords:
- Windows Media Player Online Stores, plug-in
- archivi online, plug-in
- digitare 1 negozi online, plug-in
- Windows Media Player Online Stores, creazione di plug-in
- negozi online, compilazione di plug-in
- digitare 1 negozi online, compilazione di plug-in
- Windows Media Player Online Stores, interfaccia IWMPContentPartner
- negozi online, interfaccia IWMPContentPartner
- tipo 1 Store online, interfaccia IWMPContentPartner
- plug-in, archivi Windows Media Player online
- plug-in, archivi online
- plug-in, digitare 1 negozi online
- plug-in, interfaccia IWMPContentPartner
- plug-in, compilazione
- Plug-in di Windows Media Player, digitare 1 negozi online
- Plug-in di Windows Media Player, archivi online
- Plug-in di Windows Media Player, archivi Windows Media Player online
- Plug-in di Windows Media Player, interfaccia IWMPContentPartner
- Plug-in di Windows Media Player, compilazione
- IWMPContentPartner
- creazione di plug-in, digitare 1 Store online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36272e3497eebc7b5362d793a0ee265d2c3166fc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299439"
---
# <a name="building-the-plug-in-for-a-type-1-online-store"></a><span data-ttu-id="eaa23-124">Creazione del plug-in per un negozio online di tipo 1</span><span class="sxs-lookup"><span data-stu-id="eaa23-124">Building the Plug-in for a Type 1 Online Store</span></span>

<span data-ttu-id="eaa23-125">Un archivio online di tipo 1 deve fornire un plug-in che implementi l'interfaccia [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="eaa23-125">A type 1 online store must provide a plug-in that implements the [**IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="eaa23-126">Il plug-in viene eseguito in un processo separato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eaa23-126">The plug-in runs in a separate process from Windows Media Player.</span></span>

<span data-ttu-id="eaa23-127">La procedura per la creazione di un plug-in che esegue out-of-process è la seguente:</span><span class="sxs-lookup"><span data-stu-id="eaa23-127">The steps for creating a plug-in that runs out-of-process are as follows:</span></span>

1.  <span data-ttu-id="eaa23-128">Scrivere il plug-in come se fosse un server COM in-process.</span><span class="sxs-lookup"><span data-stu-id="eaa23-128">Write your plug-in as if it were an in-process COM server.</span></span>
2.  <span data-ttu-id="eaa23-129">Creare una voce del registro di sistema **DllSurrogate** nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="eaa23-129">Create a **DllSurrogate** registry entry on the user's computer.</span></span> <span data-ttu-id="eaa23-130">La voce **DllSurrogate** informa il runtime COM che il plug-in deve essere creato in un'istanza del surrogato predefinito della DLL, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="eaa23-130">The **DllSurrogate** entry informs the COM runtime that your plug-in should be created in an instance of the default DLL surrogate, dllhost.exe.</span></span>

<span data-ttu-id="eaa23-131">Per informazioni dettagliate sulla registrazione del plug-in, vedere [chiavi e voci del registro di sistema per un archivio online di tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="eaa23-131">For detailed information about registering your plug-in, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="eaa23-132">Non è necessario creare codice proxy o stub per il plug-in.</span><span class="sxs-lookup"><span data-stu-id="eaa23-132">You do not need to create any proxy or stub code for your plug-in.</span></span> <span data-ttu-id="eaa23-133">Tutto il supporto del marshalling viene fornito da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eaa23-133">All of the marshaling support is provided by Windows Media Player.</span></span>

<span data-ttu-id="eaa23-134">È possibile utilizzare la procedura guidata plug-in di Store online per creare rapidamente un plug-in che funge da punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="eaa23-134">You can use the online store plug-in wizard to quickly create a plug-in that serves as a starting point.</span></span> <span data-ttu-id="eaa23-135">Per ulteriori informazioni, vedere [Installing the Online Store plug-in Wizard](installing-the-online-store-plug-in-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="eaa23-135">For more information, see [Installing the Online Store Plug-in Wizard](installing-the-online-store-plug-in-wizard.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaa23-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eaa23-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaa23-137">**Guida per programmatori per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="eaa23-137">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




