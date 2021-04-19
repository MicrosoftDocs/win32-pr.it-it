---
description: In Windows XP a versioni successive viene fornito un nuovo strumento da riga di comando per la configurazione e la gestione di IPv4. Questo strumento usa il \# comando &0034; netsh interface ip&\# 0034; per la configurazione e la gestione di IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Utilizzo di IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317608"
---
# <a name="using-ipv6"></a><span data-ttu-id="0ea4a-104">Utilizzo di IPv6</span><span class="sxs-lookup"><span data-stu-id="0ea4a-104">Using IPv6</span></span>

<span data-ttu-id="0ea4a-105">In Windows XP a versioni successive viene fornito un nuovo strumento da riga di comando per la configurazione e la gestione di IPv4.</span><span class="sxs-lookup"><span data-stu-id="0ea4a-105">On Windows XP a later, a new command-line tool is provided for configuring and managing IPv4.</span></span> <span data-ttu-id="0ea4a-106">Questo strumento usa il comando "netsh interface IP" per la configurazione e la gestione di IPv4.</span><span class="sxs-lookup"><span data-stu-id="0ea4a-106">This tool uses the "netsh interface ip" command for configuring and managing IPv4.</span></span>

<span data-ttu-id="0ea4a-107">In Windows XP con Service Pack 1 (SP1) e versioni successive, questo nuovo strumento da riga di comando è stato migliorato per supportare la configurazione e la gestione di IPv6.</span><span class="sxs-lookup"><span data-stu-id="0ea4a-107">On Windows XP with Service Pack 1 (SP1) and later, this new command-line tool was enhanced to support the configuration and management of IPv6.</span></span> <span data-ttu-id="0ea4a-108">Questo strumento avanzato è il comando "netsh interface IPv6".</span><span class="sxs-lookup"><span data-stu-id="0ea4a-108">This enhanced tool is the "netsh interface ipv6" command.</span></span> <span data-ttu-id="0ea4a-109">Le modifiche di configurazione apportate utilizzando i comandi Netsh.exe sono permanenti e non vengono perse quando il computer o il protocollo IPv6 viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="0ea4a-109">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="0ea4a-110">Il seguente comando è disponibile in Windows XP con SP1 e versioni successive per eseguire query e configurare IPv6 in un computer locale:</span><span class="sxs-lookup"><span data-stu-id="0ea4a-110">The following command is available on Windows XP with SP1 and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="0ea4a-111">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="0ea4a-111">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="0ea4a-112">Prima di Windows XP con Service Pack 1 (SP1), la configurazione e la gestione di IPv6 usavano diversi strumenti della riga di comando precedenti per la configurazione e la gestione di IPv6.</span><span class="sxs-lookup"><span data-stu-id="0ea4a-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools to configure and manage IPv6.</span></span> <span data-ttu-id="0ea4a-113">Utilizzando questi strumenti obsoleti, le modifiche IPv6 non sono permanenti e vengono perse quando il computer o il protocollo IPv6 è stato riavviato.</span><span class="sxs-lookup"><span data-stu-id="0ea4a-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span>

<span data-ttu-id="0ea4a-114">I comandi precedenti seguenti sono disponibili in Windows XP</span><span class="sxs-lookup"><span data-stu-id="0ea4a-114">The following older commands are available on Windows XP</span></span>

-   [<span data-ttu-id="0ea4a-115">Net.exe</span><span class="sxs-lookup"><span data-stu-id="0ea4a-115">Net.exe</span></span>](net-exe-2.md)
-   [<span data-ttu-id="0ea4a-116">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="0ea4a-116">Ipv6.exe</span></span>](ipv6-exe-2.md)
-   [<span data-ttu-id="0ea4a-117">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="0ea4a-117">Ipsec6.exe</span></span>](ipsec6-exe-2.md)

<span data-ttu-id="0ea4a-118">Questi strumenti meno recenti erano disponibili anche nella versione di anteprima della tecnologia IPv6 per Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0ea4a-118">These older tools were also provided in the IPv6 Technology Preview for Windows 2000</span></span>

<span data-ttu-id="0ea4a-119">Le modifiche di configurazione che utilizzano questi strumenti meno recenti possono essere gestite inserendole come righe di comando in un file script di comando (con estensione cmd) che viene eseguito dopo il riavvio del computer o del protocollo IPv6.</span><span class="sxs-lookup"><span data-stu-id="0ea4a-119">Configuration changes using these older tools could be maintained by placing them as command lines in a command script file (.cmd) that is run after restarting the computer or the IPv6 protocol.</span></span> <span data-ttu-id="0ea4a-120">Per ripristinare automaticamente le modifiche alla configurazione dopo il riavvio, è possibile utilizzare le attività pianificate di Windows per eseguire il file con estensione cmd all'avvio del computer.</span><span class="sxs-lookup"><span data-stu-id="0ea4a-120">To reinstate configuration changes automatically after restarting, is was possible to use the Windows Scheduled Tasks to run the .cmd file when the computer starts.</span></span>

<span data-ttu-id="0ea4a-121">Questi strumenti meno recenti non sono disponibili in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0ea4a-121">These older tools are not provided on Windows Server 2003 and later.</span></span> <span data-ttu-id="0ea4a-122">Lo strumento "netsh interface IPv6" viene fornito per la configurazione e la gestione di IPv6 dalla riga di comando in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0ea4a-122">The "netsh interface ipv6" tool is provided for configuring and managing IPv6 from the command-line on Windows Server 2003 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ea4a-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ea4a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ea4a-124">Protocollo IP versione 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="0ea4a-124">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="0ea4a-125">Guida a IPv6 per le applicazioni Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="0ea4a-125">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="0ea4a-126">Anteprima della tecnologia IPv6 per Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0ea4a-126">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



