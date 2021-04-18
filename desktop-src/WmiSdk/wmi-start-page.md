---
description: Strumentazione gestione Windows (WMI) è l'infrastruttura per i dati e le operazioni di gestione nei sistemi operativi basati su Windows.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Strumentazione gestione Windows (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec2313ca7ee744ebe6f14be42a33e2e5878960b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310332"
---
# <a name="windows-management-instrumentation"></a><span data-ttu-id="102c9-103">Strumentazione gestione Windows (WMI)</span><span class="sxs-lookup"><span data-stu-id="102c9-103">Windows Management Instrumentation</span></span>

## <a name="purpose"></a><span data-ttu-id="102c9-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="102c9-104">Purpose</span></span>

<span data-ttu-id="102c9-105">Strumentazione gestione Windows (WMI) è l'infrastruttura per i dati e le operazioni di gestione nei sistemi operativi basati su Windows.</span><span class="sxs-lookup"><span data-stu-id="102c9-105">Windows Management Instrumentation (WMI) is the infrastructure for management data and operations on Windows-based operating systems.</span></span> <span data-ttu-id="102c9-106">È possibile scrivere script o applicazioni WMI per automatizzare le attività amministrative sui computer remoti, ma WMI fornisce anche i dati di gestione ad altre parti del sistema operativo e dei prodotti, ad esempio System Center Operations Manager, in precedenza Microsoft Operations Manager (MOM) o Gestione remota Windows ([WinRM](/windows/desktop/WinRM/portal)).</span><span class="sxs-lookup"><span data-stu-id="102c9-106">You can write WMI scripts or applications to automate administrative tasks on remote computers but WMI also supplies management data to other parts of the operating system and products, for example System Center Operations Manager, formerly Microsoft Operations Manager (MOM), or Windows Remote Management ([WinRM](/windows/desktop/WinRM/portal)).</span></span>

> [!Note]  
> <span data-ttu-id="102c9-107">La seguente documentazione è destinata agli sviluppatori e agli amministratori IT.</span><span class="sxs-lookup"><span data-stu-id="102c9-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="102c9-108">Se si è un utente finale che ha riscontrato un messaggio di errore relativo a WMI, è necessario passare a [supporto tecnico Microsoft](https://support.microsoft.com/) e cercare il codice di errore visualizzato nel messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="102c9-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="102c9-109">Per ulteriori informazioni sulla risoluzione dei problemi relativi agli script WMI e al servizio WMI, vedere la pagina relativa al [funzionamento di WMI.](/previous-versions/tn-archive/ff406382(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="102c9-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))</span></span>

 

> [!Note]  
> <span data-ttu-id="102c9-110">WMI è completamente supportato da Microsoft; Tuttavia, la versione più recente del controllo e dello scripting amministrativo è disponibile tramite l'infrastruttura di gestione Windows (MI).</span><span class="sxs-lookup"><span data-stu-id="102c9-110">WMI is fully supported by Microsoft; however, the latest version of administrative scripting and control is available through the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="102c9-111">MI è completamente compatibile con le versioni precedenti di WMI e offre una serie di funzionalità e vantaggi che semplificano la progettazione e lo sviluppo di provider e client.</span><span class="sxs-lookup"><span data-stu-id="102c9-111">MI is fully compatible with previous versions of WMI, and provides a host of features and benefits that make designing and developing providers and clients easier than ever.</span></span> <span data-ttu-id="102c9-112">Per ulteriori informazioni, vedere [Windows Management Infrastructure (mi)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span><span class="sxs-lookup"><span data-stu-id="102c9-112">For more information, see [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="102c9-113">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="102c9-113">Where applicable</span></span>

<span data-ttu-id="102c9-114">WMI può essere utilizzato in tutte le applicazioni basate su Windows ed è particolarmente utile nelle applicazioni aziendali e negli script amministrativi.</span><span class="sxs-lookup"><span data-stu-id="102c9-114">WMI can be used in all Windows-based applications, and is most useful in enterprise applications and administrative scripts.</span></span>

<span data-ttu-id="102c9-115">Gli amministratori di sistema possono trovare informazioni sull'utilizzo di WMI presso TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)e in diversi libri su WMI.</span><span class="sxs-lookup"><span data-stu-id="102c9-115">System administrators can find information about using WMI at the TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx), and in various books about WMI.</span></span> <span data-ttu-id="102c9-116">Per ulteriori informazioni, vedere [ulteriori informazioni](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="102c9-116">For more information, see [Further Information](further-information.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="102c9-117">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="102c9-117">Developer audience</span></span>

<span data-ttu-id="102c9-118">WMI è progettato per i programmatori che utilizzano C/C++, l'applicazione Microsoft Visual Basic o un linguaggio di scripting che dispone di un motore di Windows e gestisce gli oggetti ActiveX Microsoft.</span><span class="sxs-lookup"><span data-stu-id="102c9-118">WMI is designed for programmers who use C/C++, the Microsoft Visual Basic application, or a scripting language that has an engine on Windows and handles Microsoft ActiveX objects.</span></span> <span data-ttu-id="102c9-119">Sebbene sia utile una certa familiarità con la programmazione COM, gli sviluppatori C++ che scrivono applicazioni possono trovare ottimi esempi per iniziare a [creare un'applicazione WMI con C++](creating-a-wmi-application-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="102c9-119">While some familiarity with COM programming is helpful, C++ developers who are writing applications can find good examples for getting started at [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

<span data-ttu-id="102c9-120">Per sviluppare applicazioni o provider di codice gestito in C# o Visual Basic .NET usando il .NET Framework, vedere [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="102c9-120">To develop managed code providers or applications in C# or Visual Basic .NET using the .NET Framework, see [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span></span>

<span data-ttu-id="102c9-121">Molti amministratori e professionisti IT accedono a WMI tramite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="102c9-121">Many administrators and IT professionals access WMI through PowerShell.</span></span> <span data-ttu-id="102c9-122">Il cmdlet Get-WMI per PowerShell consente di recuperare informazioni per un repository WMI locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="102c9-122">The Get-WMI cmdlet for PowerShell enables you to retrieve information for a local or remote WMI repository.</span></span> <span data-ttu-id="102c9-123">Di conseguenza, una serie di argomenti e classi, soprattutto nella sezione [creazione di client WMI](creating-wmi-clients.md) , contiene esempi di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="102c9-123">As such, a number of topics and classes, especially in the [Creating WMI Clients](creating-wmi-clients.md) section, contain PowerShell examples.</span></span> <span data-ttu-id="102c9-124">Per altre informazioni sull'uso di PowerShell, vedere [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) e creazione di [script con Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="102c9-124">For additional information on using PowerShell, see [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) and [Scripting with Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="102c9-125">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="102c9-125">Run-time requirements</span></span>

<span data-ttu-id="102c9-126">Per ulteriori informazioni sul sistema operativo richiesto per l'utilizzo di un elemento API specifico o di una classe WMI, vedere la sezione requisiti di ogni argomento nella documentazione di WMI.</span><span class="sxs-lookup"><span data-stu-id="102c9-126">For more information about which operating system is required to use a specific API element or WMI class, see the Requirements section of each topic in the WMI documentation.</span></span>

<span data-ttu-id="102c9-127">Se un componente previsto risulta mancante, vedere [disponibilità del sistema operativo dei componenti WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="102c9-127">If an expected component appears to be missing, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

<span data-ttu-id="102c9-128">Non è necessario scaricare o installare uno specifico SDK (Software Development) per creare script o applicazioni per WMI.</span><span class="sxs-lookup"><span data-stu-id="102c9-128">You do not need to download or install a specific software development (SDK) in order to create scripts or applications for WMI.</span></span> <span data-ttu-id="102c9-129">Tuttavia, sono disponibili alcuni strumenti di amministrazione WMI utili per gli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="102c9-129">However, there are some WMI administrative tools that developers find useful.</span></span> <span data-ttu-id="102c9-130">Per ulteriori informazioni, vedere la sezione Download in [ulteriori informazioni](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="102c9-130">For more information, see the Downloads section in [Further Information](further-information.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="102c9-131">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="102c9-131">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="102c9-132">Informazioni su WMI</span><span class="sxs-lookup"><span data-stu-id="102c9-132">About WMI</span></span>](about-wmi.md)
</dt> <dd>

<span data-ttu-id="102c9-133">Informazioni generali su WMI.</span><span class="sxs-lookup"><span data-stu-id="102c9-133">General information about WMI.</span></span>

</dd> <dt>

[<span data-ttu-id="102c9-134">Utilizzo di WMI</span><span class="sxs-lookup"><span data-stu-id="102c9-134">Using WMI</span></span>](using-wmi.md)
</dt> <dd>

<span data-ttu-id="102c9-135">Informazioni sullo sviluppo di applicazioni per l'utilizzo di WMI, incluse informazioni sugli strumenti di.</span><span class="sxs-lookup"><span data-stu-id="102c9-135">Information about how to develop applications to use WMI, which includes information about tools.</span></span>

</dd> <dt>

[<span data-ttu-id="102c9-136">Informazioni di riferimento su WMI</span><span class="sxs-lookup"><span data-stu-id="102c9-136">WMI Reference</span></span>](wmi-reference.md)
</dt> <dd>

<span data-ttu-id="102c9-137">Documentazione sulle classi WMI, le classi C++ WMI, l'API COM WMI, l'API di scripting e altro materiale di riferimento WMI.</span><span class="sxs-lookup"><span data-stu-id="102c9-137">Documentation about the WMI classes, WMI C++ classes, WMI COM API, Scripting API, and other WMI reference material.</span></span>

</dd> </dl>

 

 
