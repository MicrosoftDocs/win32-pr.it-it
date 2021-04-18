---
description: La classe CommandLineEventConsumer esegue un programma eseguibile specificato da una riga di comando quando si verifica un evento specificato. Questa classe è un consumer di eventi standard fornito da WMI.
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: Esecuzione di un programma dalla riga di comando in base a un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7f4fb5e679a6b5767635c70e2ffb5eda3ba800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309901"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a><span data-ttu-id="eaec9-104">Esecuzione di un programma dalla riga di comando in base a un evento</span><span class="sxs-lookup"><span data-stu-id="eaec9-104">Running a Program from the Command Line Based on an Event</span></span>

<span data-ttu-id="eaec9-105">La classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) esegue un programma eseguibile specificato da una riga di comando quando si verifica un evento specificato.</span><span class="sxs-lookup"><span data-stu-id="eaec9-105">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class runs a specified executable program from a command line when a specified event occurs.</span></span> <span data-ttu-id="eaec9-106">Questa classe è un consumer di eventi standard fornito da WMI.</span><span class="sxs-lookup"><span data-stu-id="eaec9-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="eaec9-107">Quando si usa [**CommandLineEventConsumer**](commandlineeventconsumer.md), è necessario proteggere il file eseguibile che si vuole avviare.</span><span class="sxs-lookup"><span data-stu-id="eaec9-107">When you use [**CommandLineEventConsumer**](commandlineeventconsumer.md), you should secure the executable that you want to start.</span></span> <span data-ttu-id="eaec9-108">Se il file eseguibile non si trova in una posizione sicura o non è protetto con un elenco di controllo di accesso (ACL) sicuro, un utente senza privilegi di accesso può sostituire l'eseguibile con un file eseguibile diverso.</span><span class="sxs-lookup"><span data-stu-id="eaec9-108">If the executable is not in a secure location or not secured with a strong access control list (ACL), a user without access privileges can replace your executable with a different executable.</span></span> <span data-ttu-id="eaec9-109">È possibile utilizzare le classi [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) o [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) per modificare a livello di codice la sicurezza di un file o di una condivisione.</span><span class="sxs-lookup"><span data-stu-id="eaec9-109">You can use the [**Win32\_LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) or [**Win32\_LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) classes to change programmatically the security of a file or share.</span></span> <span data-ttu-id="eaec9-110">Per ulteriori informazioni, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="eaec9-110">For more information, see [Creating a Security Descriptor for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

<span data-ttu-id="eaec9-111">La procedura di base per l'uso di consumer standard è sempre la stessa e si trova nel [monitoraggio e nella risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="eaec9-111">The basic procedure to use standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="eaec9-112">La procedura seguente aggiunge alla procedura di base, è specifica della classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) e descrive come creare un consumer di eventi che esegue un programma.</span><span class="sxs-lookup"><span data-stu-id="eaec9-112">The following procedure adds to the basic procedure, is specific to the [**CommandLineEventConsumer**](commandlineeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

> [!Caution]
>
> <span data-ttu-id="eaec9-113">La classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) presenta vincoli di sicurezza speciali.</span><span class="sxs-lookup"><span data-stu-id="eaec9-113">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="eaec9-114">Questo consumer standard deve essere configurato da un membro locale del gruppo Administrators nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="eaec9-114">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="eaec9-115">Se si utilizza un account di dominio per creare la sottoscrizione, è necessario che l'account LocalSystem disponga delle autorizzazioni necessarie per il dominio per verificare che il creatore sia un membro del gruppo Administrators locale.</span><span class="sxs-lookup"><span data-stu-id="eaec9-115">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>
>
> <span data-ttu-id="eaec9-116">Non è possibile usare [**CommandLineEventConsumer**](commandlineeventconsumer.md) per avviare un processo che viene eseguito in modo interattivo.</span><span class="sxs-lookup"><span data-stu-id="eaec9-116">[**CommandLineEventConsumer**](commandlineeventconsumer.md) cannot be used to start a process that runs interactively.</span></span>

 

<span data-ttu-id="eaec9-117">Nella procedura seguente viene descritto come creare un consumer di eventi che esegue un processo da una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="eaec9-117">The following procedure describes how to create an event consumer that runs a process from a command line.</span></span>

<span data-ttu-id="eaec9-118">**Per creare un consumer di eventi che esegue un processo da una riga di comando**</span><span class="sxs-lookup"><span data-stu-id="eaec9-118">**To create an event consumer that runs a process from a command line**</span></span>

1.  <span data-ttu-id="eaec9-119">Nel file Managed Object Format (MOF) creare un'istanza di [**CommandLineEventConsumer**](commandlineeventconsumer.md) per ricevere gli eventi richiesti nella query.</span><span class="sxs-lookup"><span data-stu-id="eaec9-119">In the Managed Object Format (MOF) file, create an instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="eaec9-120">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="eaec9-120">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="eaec9-121">Creare un'istanza di [**\_ \_ EventFilter**](--eventfilter.md) e assegnarle un nome.</span><span class="sxs-lookup"><span data-stu-id="eaec9-121">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and give it a name.</span></span>
3.  <span data-ttu-id="eaec9-122">Creare una query per specificare il tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="eaec9-122">Create a query to specify the type of event.</span></span> <span data-ttu-id="eaec9-123">Per ulteriori informazioni, vedere [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="eaec9-123">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>
4.  <span data-ttu-id="eaec9-124">Creare un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) per associare il filtro all'istanza di [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="eaec9-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span></span>
5.  <span data-ttu-id="eaec9-125">Compilare il file MOF usando [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="eaec9-125">Compile your MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="eaec9-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="eaec9-126">Example</span></span>

<span data-ttu-id="eaec9-127">Nell'esempio di codice seguente viene creata una nuova classe denominata "MyCmdLineConsumer" per generare eventi quando viene creata un'istanza della nuova classe alla fine di un file MOF.</span><span class="sxs-lookup"><span data-stu-id="eaec9-127">The following code example creates a new class called "MyCmdLineConsumer" to generate events when an instance of the new class is created at the end of a MOF.</span></span> <span data-ttu-id="eaec9-128">L'esempio è nel codice MOF, ma è possibile creare le istanze a livello di programmazione usando l' [API di scripting per WMI](scripting-api-for-wmi.md) o l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="eaec9-128">The example is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="eaec9-129">Nella procedura seguente viene descritto come creare una nuova classe denominata MyCmdLineConsumer.</span><span class="sxs-lookup"><span data-stu-id="eaec9-129">The following procedure describes how to create a new class called MyCmdLineConsumer.</span></span>

<span data-ttu-id="eaec9-130">**Per creare una nuova classe denominata MyCmdLineConsumer**</span><span class="sxs-lookup"><span data-stu-id="eaec9-130">**To create a new class called MyCmdLineConsumer**</span></span>

1.  <span data-ttu-id="eaec9-131">Creare il \\ \_ file ditest.bat c: cmdline con un comando che esegue un programma visibile, ad esempio "calc.exe".</span><span class="sxs-lookup"><span data-stu-id="eaec9-131">Create the c:\\cmdline\_test.bat file with a command that executes a visible program, such as "calc.exe" .</span></span>
2.  <span data-ttu-id="eaec9-132">Copiare il file MOF in un file di testo e salvarlo con un'estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="eaec9-132">Copy the MOF to a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="eaec9-133">In una finestra di comando compilare il file MOF usando il comando seguente: **mofcomp nomefile. mof**.</span><span class="sxs-lookup"><span data-stu-id="eaec9-133">In a Command window, compile the MOF file by using the following command: **Mofcomp filename.mof**.</span></span>

> [!Note]  
> <span data-ttu-id="eaec9-134">Il programma specificato in cmdline \_test.bat deve essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="eaec9-134">The program specified in cmdline\_test.bat should execute.</span></span>

 

``` syntax
// Set the namespace as root\subscription.
// The CommandLineEventConsumer is already compiled
// in the root\subscription namespace. 
#pragma namespace ("\\\\.\\Root\\subscription")

class MyCmdLineConsumer
{
 [key]string Name;
};

// Create an instance of the command line consumer
// and give it the alias $CMDLINECONSUMER

instance of CommandLineEventConsumer as $CMDLINECONSUMER
{
 Name = "CmdLineConsumer_Example";
 CommandLineTemplate = "c:\\cmdline_test.bat";
 RunInteractively = True;
 WorkingDirectory = "c:\\";
};    

// Create an instance of the event filter
// and give it the alias $CMDLINEFILTER
// The filter queries for instance creation event
// for instances of the MyCmdLineConsumer class

instance of __EventFilter as $CMDLINEFILTER
{
    Name = "CmdLineFilter";
    Query = "SELECT * FROM __InstanceCreationEvent"
        " WHERE TargetInstance.__class = \"MyCmdLineConsumer\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
     Consumer = $CMDLINECONSUMER;
     Filter = $CMDLINEFILTER;
};

// Create an instance of this class right now. 
// The commands in c:\\cmdline_test.bat execute
// as the result of creating the instance
// of MyCmdLineConsumer.
 
instance of MyCmdLineConsumer
{
     Name = "CmdLineEventConsumer test";
};
```

## <a name="related-topics"></a><span data-ttu-id="eaec9-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eaec9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaec9-136">Monitoraggio e risposta agli eventi con consumer standard</span><span class="sxs-lookup"><span data-stu-id="eaec9-136">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
