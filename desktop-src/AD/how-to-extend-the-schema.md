---
title: Come estendere lo schema
description: Quando le classi e/o gli attributi esistenti non rientrano nel tipo di dati che si desidera archiviare, potrebbe essere necessario estendere lo schema.
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- ANNUNCIO dello schema, come estendere
- Active Directory, utilizzo di, schema
- Active Directory, utilizzo di, schema, estensione dello schema, come estendere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724495"
---
# <a name="how-to-extend-the-schema"></a><span data-ttu-id="3d16c-106">Come estendere lo schema</span><span class="sxs-lookup"><span data-stu-id="3d16c-106">How to Extend the Schema</span></span>

<span data-ttu-id="3d16c-107">Quando le classi e/o gli attributi esistenti non rientrano nel tipo di dati che si desidera archiviare, potrebbe essere necessario estendere lo schema.</span><span class="sxs-lookup"><span data-stu-id="3d16c-107">When the existing classes and/or attributes do not fit with the type of data that you want to store, you might want to extend the schema.</span></span> <span data-ttu-id="3d16c-108">Per ulteriori informazioni su come decidere quando estendere lo schema, vedere [estensione dello schema](extending-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="3d16c-108">For more information on deciding when to extend the schema, see [Extending the Schema](extending-the-schema.md).</span></span> <span data-ttu-id="3d16c-109">Quando si è deciso che è richiesta l'estensione dello schema, utilizzare la procedura seguente per estendere lo schema.</span><span class="sxs-lookup"><span data-stu-id="3d16c-109">When you have decided that schema extension is required, use the following procedure to extend the schema.</span></span>

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a><span data-ttu-id="3d16c-110">Verificare Active Directory funzionalità prima di applicare le estensioni dello schema</span><span class="sxs-lookup"><span data-stu-id="3d16c-110">Verify Active Directory functionality before you apply any schema extensions</span></span>

<span data-ttu-id="3d16c-111">Verificare Active Directory funzionalità prima di aggiornare lo schema per garantire che l'estensione dello schema proceda senza errori.</span><span class="sxs-lookup"><span data-stu-id="3d16c-111">Verify Active Directory functionality before you update the schema to help ensure that the schema extension proceeds without error.</span></span> <span data-ttu-id="3d16c-112">Assicurarsi almeno che tutti i controller di dominio per la foresta siano online ed eseguano la replica in ingresso.</span><span class="sxs-lookup"><span data-stu-id="3d16c-112">At a minimum, ensure that all domain controllers for the forest are online and performing inbound replication.</span></span>

<span data-ttu-id="3d16c-113">**Per verificare Active Directory funzionalità prima di applicare l'estensione dello schema**</span><span class="sxs-lookup"><span data-stu-id="3d16c-113">**To verify Active Directory functionality before you apply the schema extension**</span></span>

1.  <span data-ttu-id="3d16c-114">Accedere a una workstation amministrativa in cui è installato lo strumento di supporto di Windows Repadmin.exe.</span><span class="sxs-lookup"><span data-stu-id="3d16c-114">Log on to an administrative workstation that has the Windows Support Tool Repadmin.exe installed.</span></span>
    > [!Note]  
    > <span data-ttu-id="3d16c-115">Gli strumenti di supporto si trovano nel supporto di installazione del sistema operativo nella \\ cartella strumenti di supporto.</span><span class="sxs-lookup"><span data-stu-id="3d16c-115">The Support Tools are located on the operating system installation media in the Support\\Tools folder.</span></span>

     

2.  <span data-ttu-id="3d16c-116">Aprire un prompt dei comandi, quindi passare alla cartella in cui sono installati gli strumenti di supporto di Windows.</span><span class="sxs-lookup"><span data-stu-id="3d16c-116">Open a command prompt, and then change directories to the folder in which the Windows Support Tools are installed.</span></span>
3.  <span data-ttu-id="3d16c-117">Al prompt dei comandi digitare quanto segue e quindi premere INVIO:</span><span class="sxs-lookup"><span data-stu-id="3d16c-117">At a command prompt, type the following, and then press ENTER:</span></span>

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    <span data-ttu-id="3d16c-118">Tutti i controller di dominio devono visualizzare 0 nella colonna errore e i Delta più grandi, che indicano il numero di modifiche apportate al database Active Directory dall'ultima replica completata, devono essere minori o approssimativamente uguali alla frequenza di replica del collegamento di sito utilizzato dal controller di dominio per la replica.</span><span class="sxs-lookup"><span data-stu-id="3d16c-118">All domain controllers should show 0 in the Fails column, and the largest deltas (which indicate the number of changes that have been made to the Active Directory database since the last successful replication) should be less than or roughly equal to the replication frequency of the site link that is used by the domain controller for replication.</span></span> <span data-ttu-id="3d16c-119">La frequenza di replica predefinita è di 180 minuti.</span><span class="sxs-lookup"><span data-stu-id="3d16c-119">The default replication frequency is 180 minutes.</span></span>

    <span data-ttu-id="3d16c-120">Per ulteriori informazioni sui passaggi aggiuntivi che è possibile eseguire per verificare Active Directory funzionalità prima di applicare l'estensione dello schema, vedere [l'articolo 325379 della Microsoft Knowledge base](https://support.microsoft.com/kb/325379/en-us).</span><span class="sxs-lookup"><span data-stu-id="3d16c-120">For more information about additional steps that you can take to verify Active Directory functionality before you apply the schema extension, see [article 325379 in the Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).</span></span>

<span data-ttu-id="3d16c-121">**Per estendere lo schema**</span><span class="sxs-lookup"><span data-stu-id="3d16c-121">**To Extend the Schema**</span></span>

1.  <span data-ttu-id="3d16c-122">Determinare il metodo di estensione.</span><span class="sxs-lookup"><span data-stu-id="3d16c-122">Determine the method of extension.</span></span> <span data-ttu-id="3d16c-123">Dopo aver progettato con attenzione le modifiche dello schema, il passaggio successivo consiste nel decidere quale metodo utilizzare per estendere lo schema.</span><span class="sxs-lookup"><span data-stu-id="3d16c-123">Once you have carefully designed your schema changes, the next step is to decide which method to use to extend the schema.</span></span> <span data-ttu-id="3d16c-124">È possibile utilizzare uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3d16c-124">You can use one of the following methods:</span></span>
    -   <span data-ttu-id="3d16c-125">Manualmente, usando i file di importazione.</span><span class="sxs-lookup"><span data-stu-id="3d16c-125">Manually, using import files.</span></span> <span data-ttu-id="3d16c-126">Vedere la documentazione [con lo strumento LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span><span class="sxs-lookup"><span data-stu-id="3d16c-126">See the documentation [Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span></span>
        > [!Note]  
        > <span data-ttu-id="3d16c-127">Non usare LDIFDE per importare file Windows SCH \* . ldf.</span><span class="sxs-lookup"><span data-stu-id="3d16c-127">Do not use LDIFDE to import Windows Sch\*.ldf files.</span></span> <span data-ttu-id="3d16c-128">Tali file sono necessari per estendere lo schema di Active Directory per installare controller di dominio che eseguono una versione più recente di Windows Server rispetto alla versione in esecuzione nel master schema corrente.</span><span class="sxs-lookup"><span data-stu-id="3d16c-128">Those files are required to extend the Active Directory schema in order to install domain controllers that run a newer version of Windows Server than the version that is running on the current schema master.</span></span> <span data-ttu-id="3d16c-129">Quando è necessario estendere lo schema per poter installare un nuovo controller di dominio, utilizzare Adprep.exe.</span><span class="sxs-lookup"><span data-stu-id="3d16c-129">When you need to extend the schema in order to install a new domain controller, use Adprep.exe.</span></span>

         

    -   <span data-ttu-id="3d16c-130">A livello di codice, usando un programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="3d16c-130">Programmatically, using an installation program.</span></span> <span data-ttu-id="3d16c-131">Per ulteriori informazioni, vedere [estensione a livello di codice](programmatic-extension.md)</span><span class="sxs-lookup"><span data-stu-id="3d16c-131">For more information, see [Programmatic Extension](programmatic-extension.md)</span></span>
2.  <span data-ttu-id="3d16c-132">Abilitare le modifiche dello schema.</span><span class="sxs-lookup"><span data-stu-id="3d16c-132">Enable Schema Changes.</span></span> <span data-ttu-id="3d16c-133">Per ulteriori informazioni, vedere [prerequisiti per l'installazione di un'estensione dello schema](prerequisites-for-installing-a-schema-extension.md) e [l'abilitazione delle modifiche dello schema nel master schema](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="3d16c-133">For more information, see [Prerequisites for Installing a Schema Extension](prerequisites-for-installing-a-schema-extension.md) and [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
3.  <span data-ttu-id="3d16c-134">Ottenere un identificatore di oggetto (OID) per i nuovi attributi e/o le classi, come descritto in [ottenere un identificatore di oggetto](obtaining-an-object-identifier.md).</span><span class="sxs-lookup"><span data-stu-id="3d16c-134">Obtain an Object Identifier (OID) for your new attributes and/or classes, as described in [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>
4.  <span data-ttu-id="3d16c-135">Creare nuovi attributi e classi.</span><span class="sxs-lookup"><span data-stu-id="3d16c-135">Create new attributes and classes.</span></span>
5.  <span data-ttu-id="3d16c-136">Usare gli identificatori di visualizzazione per integrare nuovi attributi e classi con l'interfaccia utente, se necessario.</span><span class="sxs-lookup"><span data-stu-id="3d16c-136">Use display specifiers to integrate new attributes and classes with the user interface, if necessary.</span></span>
6.  <span data-ttu-id="3d16c-137">Aggiornare la cache dello schema come descritto in [aggiornamento della cache dello schema](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="3d16c-137">Update the schema cache as described in [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>
7.  <span data-ttu-id="3d16c-138">Verificare l'estensione dello schema utilizzando LDP.exe.</span><span class="sxs-lookup"><span data-stu-id="3d16c-138">Verify the schema extension using LDP.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d16c-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d16c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d16c-140">Ottenere un identificatore di oggetto</span><span class="sxs-lookup"><span data-stu-id="3d16c-140">Obtaining an Object Identifier</span></span>](obtaining-an-object-identifier.md)
</dt> <dt>

[<span data-ttu-id="3d16c-141">Nuovi strumenti da riga di comando per Active Directory in Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d16c-141">The new command-line tools for Active Directory in Windows Server 2003</span></span>](https://support.microsoft.com/kb/298882)
</dt> <dt>

<span data-ttu-id="3d16c-142">[Utilizzo dello strumento LDIFDE](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span><span class="sxs-lookup"><span data-stu-id="3d16c-142">[Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span></span>
</dt> <dt>

<span data-ttu-id="3d16c-143">[Estensione dello schema di Active Directory](/previous-versions/ms806972(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3d16c-143">[Extending the Active Directory Schema](/previous-versions/ms806972(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="3d16c-144">Restrizioni sull'estensione dello schema</span><span class="sxs-lookup"><span data-stu-id="3d16c-144">Restrictions on Schema Extension</span></span>](restrictions-on-schema-extension.md)
</dt> </dl>

 

 