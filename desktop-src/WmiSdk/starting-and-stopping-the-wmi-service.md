---
description: WMI viene eseguito come servizio con il nome visualizzato &\# 0034; Strumentazione gestione Windows&\# 0034; e il nome del servizio &\# 0034; winmgmt&\# 0034;.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Avvio e arresto del servizio WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54b820283aac089ad6191ee587e6beadea6dc030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226819"
---
# <a name="starting-and-stopping-the-wmi-service"></a><span data-ttu-id="ebef3-103">Avvio e arresto del servizio WMI</span><span class="sxs-lookup"><span data-stu-id="ebef3-103">Starting and Stopping the WMI Service</span></span>

<span data-ttu-id="ebef3-104">WMI viene eseguito come servizio con il nome visualizzato "Strumentazione gestione Windows" e il nome del servizio "WinMgmt".</span><span class="sxs-lookup"><span data-stu-id="ebef3-104">WMI runs as a service with the display name "Windows Management Instrumentation" and the service name "winmgmt".</span></span> <span data-ttu-id="ebef3-105">WMI viene eseguito automaticamente all'avvio del sistema con l'account LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="ebef3-105">WMI runs automatically at system startup under the LocalSystem account.</span></span> <span data-ttu-id="ebef3-106">Se WMI non è in esecuzione, viene avviato automaticamente quando il primo script o un'applicazione di gestione richiede la connessione a uno spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="ebef3-106">If WMI is not running, it automatically starts when the first management application or script requests connection to a WMI namespace.</span></span>

<span data-ttu-id="ebef3-107">Molti altri servizi dipendono dal servizio WMI, a seconda della versione del sistema operativo in esecuzione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ebef3-107">Several other services are dependent upon the WMI service, depending on the operating system version that the system is running.</span></span>

## <a name="starting-winmgmt-service"></a><span data-ttu-id="ebef3-108">Avvio del servizio WinMgmt</span><span class="sxs-lookup"><span data-stu-id="ebef3-108">Starting Winmgmt Service</span></span>

<span data-ttu-id="ebef3-109">Nella procedura riportata di seguito viene descritto come avviare il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="ebef3-109">The following procedure describes how to start the WMI service.</span></span>

<span data-ttu-id="ebef3-110">**Per avviare il servizio WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="ebef3-110">**To start Winmgmt Service**</span></span>

1.  <span data-ttu-id="ebef3-111">Al prompt dei comandi immettere **net** **Start** **WinMgmt** \[ */<switch>* \] .</span><span class="sxs-lookup"><span data-stu-id="ebef3-111">At a command prompt, enter **net** **start** **winmgmt** \[*/<switch>*\].</span></span>

    <span data-ttu-id="ebef3-112">Per ulteriori informazioni sulle opzioni disponibili, vedere [WinMgmt](winmgmt.md).</span><span class="sxs-lookup"><span data-stu-id="ebef3-112">For more information about the switches that are available, see [winmgmt](winmgmt.md).</span></span> <span data-ttu-id="ebef3-113">Utilizzare l'account Administrator predefinito o un account del gruppo Administrators che esegue con diritti elevati per avviare il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="ebef3-113">You use the built-in Administrator account or an account in the Administrators group running with elevated rights to start the WMI service.</span></span> <span data-ttu-id="ebef3-114">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ebef3-114">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

2.  <span data-ttu-id="ebef3-115">Altri servizi che dipendono dal servizio WMI, ad esempio host agenti di SMS o Windows Firewall, non verranno riavviati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ebef3-115">Other services that are dependent on the WMI service, such as SMS Agent Host or Windows Firewall, will not automatically be restarted.</span></span>

## <a name="stopping-winmgmt-service"></a><span data-ttu-id="ebef3-116">Arresto del servizio WinMgmt</span><span class="sxs-lookup"><span data-stu-id="ebef3-116">Stopping Winmgmt Service</span></span>

<span data-ttu-id="ebef3-117">Nella procedura riportata di seguito viene descritto come arrestare il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="ebef3-117">The following procedure describes how to stop the WMI Service.</span></span>

<span data-ttu-id="ebef3-118">**Per arrestare il servizio WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="ebef3-118">**To stop Winmgmt Service**</span></span>

1.  <span data-ttu-id="ebef3-119">Al prompt dei comandi, immettere **net stop winmgmt**.</span><span class="sxs-lookup"><span data-stu-id="ebef3-119">At a command prompt, enter **net stop winmgmt**.</span></span>

2.  <span data-ttu-id="ebef3-120">Anche altri servizi che dipendono dal servizio WMI si interrompono, ad esempio host agenti di SMS o Windows Firewall.</span><span class="sxs-lookup"><span data-stu-id="ebef3-120">Other services that are dependent on the WMI service also halt, such as SMS Agent Host or Windows Firewall.</span></span>

## <a name="examples"></a><span data-ttu-id="ebef3-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="ebef3-121">Examples</span></span>

<span data-ttu-id="ebef3-122">La raccolta TechNet contiene lo [script del watchdog del servizio WMI](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), che descrive come arrestare e riavviare il servizio WinMgmt a livello di codice con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ebef3-122">The TechNet Gallery contains the [WMI service watchdog script](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), which describes how to programmatically shut down and restart the winmgmt service with PowerShell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebef3-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ebef3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebef3-124">Utilizzo degli strumenti di Command-Line WMI</span><span class="sxs-lookup"><span data-stu-id="ebef3-124">Using the WMI Command-Line Tools</span></span>](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



