---
description: Tutte le impostazioni di autenticazione vengono eseguite tramite il Gestione servizi Internet.
ms.assetid: 9b118120-f0cb-4973-b537-dd3d12a7a6d5
ms.tgt_platform: multiple
title: Configurazione di IIS 5,0 e versioni successive per lo scripting ASP WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4b5ddde139b3eef32fd7c80f4cca4e10fd816a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310414"
---
# <a name="configuring-iis-50-and-later-for-wmi-asp-scripting"></a><span data-ttu-id="ad8f4-103">Configurazione di IIS 5,0 e versioni successive per lo scripting ASP WMI</span><span class="sxs-lookup"><span data-stu-id="ad8f4-103">Configuring IIS 5.0 and Later for WMI ASP Scripting</span></span>

<span data-ttu-id="ad8f4-104">Tutte le impostazioni di autenticazione vengono eseguite tramite il Gestione servizi Internet.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-104">All authentication settings are made through the Internet Services Manager.</span></span>

<span data-ttu-id="ad8f4-105">Quando si configurano Internet Information Server (IIS) 5,0 e IIS 6,0 Security per gli script ASP WMI, tenere presenti i seguenti problemi:</span><span class="sxs-lookup"><span data-stu-id="ad8f4-105">When configuring Internet Information Server (IIS) 5.0 and IIS 6.0 security for WMI ASP scripts, consider the following issues:</span></span>

-   [<span data-ttu-id="ad8f4-106">Livello di autenticazione</span><span class="sxs-lookup"><span data-stu-id="ad8f4-106">Authentication level</span></span>](#authentication-level)

    <span data-ttu-id="ad8f4-107">È possibile configurare a livello di server, di directory o di file.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-107">You can configure at the server, directory, or file level.</span></span>

-   [<span data-ttu-id="ad8f4-108">Impostazione di autenticazione</span><span class="sxs-lookup"><span data-stu-id="ad8f4-108">Authentication setting</span></span>](#authentication-setting)

    <span data-ttu-id="ad8f4-109">È possibile impostare l'autenticazione su finestre anonime, integrate o entrambe.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-109">You can set authentication to Anonymous, Integrated Windows, or both.</span></span>

-   [<span data-ttu-id="ad8f4-110">Protezione</span><span class="sxs-lookup"><span data-stu-id="ad8f4-110">Protection</span></span>](#protection)

    <span data-ttu-id="ad8f4-111">È possibile impostare l'ASP per l'esecuzione in-process (protezione ridotta) o out-of-process usando Dllhost.exe (media o High Protection).</span><span class="sxs-lookup"><span data-stu-id="ad8f4-111">You can set the ASP to run in-process (low protection), or out-of-process by using Dllhost.exe (medium or high protection).</span></span>

## <a name="authentication-level"></a><span data-ttu-id="ad8f4-112">Livello di autenticazione</span><span class="sxs-lookup"><span data-stu-id="ad8f4-112">Authentication Level</span></span>

<span data-ttu-id="ad8f4-113">Per una maggiore sicurezza, è possibile configurare l'autenticazione a livello di directory o di file.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-113">For added security, you can configure the authentication at the directory or file level.</span></span>

<span data-ttu-id="ad8f4-114">Se l'autenticazione viene impostata a livello di server, tutte le directory e i file successivi rispettano l'autenticazione del server, a meno che non vengano modificati in modo esplicito a livello di directory o di file.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-114">If authentication is set at the server level, all subsequent directories and files adhere to the server authentication unless explicitly altered at the directory or file level.</span></span> <span data-ttu-id="ad8f4-115">È possibile creare una struttura di directory che contenga tutti gli script ASP WMI in cui le pagine HTML e gli ASP specifici di WMI possono essere configurati in modo indipendente dal resto del server.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-115">You can create a directory structure to contain all WMI ASP scripts where HTML pages and ASPs specific to WMI can be configured independently from the rest of the server.</span></span> <span data-ttu-id="ad8f4-116">Eseguire la procedura seguente per modificare il livello di autenticazione di un server, di una directory o di un file.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-116">Perform the following procedure to change the authentication level of a server, directory, or file.</span></span>

<span data-ttu-id="ad8f4-117">**Per impostare l'autenticazione a qualsiasi livello**</span><span class="sxs-lookup"><span data-stu-id="ad8f4-117">**To set the authentication at any level**</span></span>

1.  <span data-ttu-id="ad8f4-118">Nel pannello di controllo fare doppio clic su **strumenti di amministrazione**, quindi fare doppio clic sullo snap-in IIS.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-118">In Control Panel, double-click **Administrative Tools**, and then double-click the IIS snap-in.</span></span>

2.  <span data-ttu-id="ad8f4-119">Individuare l'icona pagina ASP, quindi aprire le proprietà del livello da impostare, che può essere server, directory o file.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-119">Locate the ASP page icon, and then open the properties for the level to set, which can be server, directory, or file.</span></span>

    > [!Note]  
    > <span data-ttu-id="ad8f4-120">Le impostazioni di autenticazione si trovano nella scheda **sicurezza directory** o **sicurezza file** della finestra delle **proprietà**.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-120">Authentication settings are located on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

     

## <a name="authentication-setting"></a><span data-ttu-id="ad8f4-121">Impostazione di autenticazione</span><span class="sxs-lookup"><span data-stu-id="ad8f4-121">Authentication Setting</span></span>

<span data-ttu-id="ad8f4-122">Per gli script ASP WMI, la combinazione di autenticazione anonima disattivata (deselezionata) e l'autenticazione integrata di Windows attivata (selezionata) offre maggiore opportunità di impostare la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-122">For WMI ASP scripts, the combination of Anonymous authentication turned off (unchecked), and Integrated Windows authentication turned on (checked) provides greater opportunity to set security.</span></span> <span data-ttu-id="ad8f4-123">Per utilizzare le impostazioni di autenticazione IIS NT (NTLM), Passport o digest, è necessario attivare i privilegi di abilitazione remota, perché l'utente viene considerato come un'identità di rete e registrato in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-123">To use NT LAN Manager (NTLM), Passport, or Digest IIS authentication settings, you must turn on the remote enable privileges, because the user is treated as a network identity and logged remotely.</span></span> <span data-ttu-id="ad8f4-124">L'impostazione Abilita remoto non è necessaria per l'autenticazione anonima e di base.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-124">The remote enable setting is not required for Anonymous and Basic authentication.</span></span> <span data-ttu-id="ad8f4-125">Tuttavia, il sistema è molto meno sicuro quando si usa l'autenticazione anonima e di base.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-125">However, the system is much less secure when you are using Anonymous and Basic authentication.</span></span>

<span data-ttu-id="ad8f4-126">Se l'autenticazione anonima viene utilizzata con o senza l'autenticazione integrata di Windows, l'approccio più sicuro consiste nell'utilizzare un accesso che richiede all'utente di immettere un nome utente e una password.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-126">If Anonymous authentication is used with or without Integrated Windows authentication, the most secure approach is to use a logon that requires a user to enter a username and password.</span></span> <span data-ttu-id="ad8f4-127">L'account di accesso predefinito è l'identità IIS, ma è possibile creare un accesso utilizzando autorizzazioni specifiche appropriate per gli script ASP WMI che possono essere utilizzati come account per le connessioni anonime o Guest.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-127">The default logon is the IIS identity, but a logon can be created by using specific permissions suited for the WMI ASP Scripts that can be used as the account for the anonymous or guest connections.</span></span>

<span data-ttu-id="ad8f4-128">Se si sceglie un identificatore di accesso che non è un'identità IIS, deselezionare la casella **di controllo Consenti a IIS di controllare la password** e immettere la password corretta.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-128">If you choose a logon identifier that is not an IIS identity, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="ad8f4-129">Questa operazione impone a tutte le connessioni anonime o Guest di utilizzare l'identificatore di accesso.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-129">This forces all anonymous or guest connections to use the logon identifier.</span></span> <span data-ttu-id="ad8f4-130">Creando un accesso separato dall'identità IIS, è possibile controllare i privilegi di un account che accede a WMI senza influire sulle altre directory o sui file nel server IIS, a meno che l'autenticazione non sia impostata a livello di server.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-130">By creating a logon separate from the IIS identity, the privileges of an account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="ad8f4-131">Eseguire la procedura seguente per impostare i requisiti di autenticazione per la pagina ASP tramite lo snap-in IIS nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-131">Perform the following procedure to set the authentication requirements for the ASP page using the IIS snap-in in the Control Panel.</span></span>

<span data-ttu-id="ad8f4-132">**Per ottenere l'impostazione dell'account**</span><span class="sxs-lookup"><span data-stu-id="ad8f4-132">**To get to the account setting**</span></span>

1.  <span data-ttu-id="ad8f4-133">Nel pannello di controllo fare doppio clic sull'icona **strumenti di amministrazione** , aprire lo snap-in IIS, individuare la pagina ASP e aprire le proprietà del livello da impostare, che può essere server, directory o file.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-133">In Control Panel, double-click the **Administrative Tools** icon, open the IIS snap-in, locate your ASP page, and open the properties of the level to set, which can be server, directory, or file.</span></span>

    <span data-ttu-id="ad8f4-134">È possibile trovare le impostazioni di autenticazione nella scheda **sicurezza directory** o **sicurezza file** della finestra delle **proprietà** .</span><span class="sxs-lookup"><span data-stu-id="ad8f4-134">Authentication settings can be found on either the **Directory Security** or **File Security** tab of the **Properties** sheet.</span></span>

2.  <span data-ttu-id="ad8f4-135">Nell'area autenticazione anonima fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-135">In the Anonymous authentication area, click **Edit**.</span></span>

3.  <span data-ttu-id="ad8f4-136">Se è selezionato un identificatore di accesso diverso dall'identità IIS, deselezionare la casella **di controllo Consenti a IIS di controllare la password** e immettere la password corretta.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-136">If a logon identifier other than the IIS identity is selected, then clear the **Allow IIS to control password** check box, and enter the correct password.</span></span> <span data-ttu-id="ad8f4-137">Questa operazione impone a tutte le connessioni anonime o Guest di utilizzare l'identificatore di accesso.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-137">This forces all anonymous or guest connections to use the logon identifier.</span></span>

<span data-ttu-id="ad8f4-138">Utilizzando un accesso diverso dall'identità IIS, i privilegi dell'account che accede a WMI possono essere controllati senza influire sulle altre directory o sui file nel server IIS, a meno che l'autenticazione non sia impostata a livello di server.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-138">By using a logon different from the IIS identity, the privileges of the account accessing WMI can be controlled without affecting the other directories or files on the IIS server—unless the authentication is set at the server level.</span></span>

<span data-ttu-id="ad8f4-139">La configurazione precedente consente al server IIS di usare l'autenticazione anonima in alcune aree, oltre a Windows integrata o all'autenticazione mista in altri.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-139">The previous configuration allows the IIS server to use Anonymous authentication in some areas, and Integrated Windows or mixed authentication in others.</span></span>

## <a name="protection"></a><span data-ttu-id="ad8f4-140">Protezione</span><span class="sxs-lookup"><span data-stu-id="ad8f4-140">Protection</span></span>

<span data-ttu-id="ad8f4-141">L'ultima considerazione per la configurazione del server IIS è la protezione da utilizzare durante l'esecuzione di un'applicazione ASP.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-141">The last consideration when configuring the IIS server is which protection to use when executing an ASP.</span></span>

<span data-ttu-id="ad8f4-142">È possibile impostare un ASP per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ad8f4-142">You can set an ASP to run the following:</span></span>

-   <span data-ttu-id="ad8f4-143">In-process per IIS (bassa protezione).</span><span class="sxs-lookup"><span data-stu-id="ad8f4-143">In-process to IIS (low protection).</span></span>

-   <span data-ttu-id="ad8f4-144">Da esterno a IIS con Dllhost.exe in pool o out-of-process (protezione da pool).</span><span class="sxs-lookup"><span data-stu-id="ad8f4-144">External to IIS with Dllhost.exe as pooled or out-of-process (pooled medium protection).</span></span>

-   <span data-ttu-id="ad8f4-145">Self-of-process-host (protezione elevata).</span><span class="sxs-lookup"><span data-stu-id="ad8f4-145">Out-of-process self-host (high protection).</span></span>

> [!Note]  
> <span data-ttu-id="ad8f4-146">Per il migliore equilibrio tra sicurezza e prestazioni, utilizzare l'host in pool.</span><span class="sxs-lookup"><span data-stu-id="ad8f4-146">For the best balance of security and performance, use pooled host.</span></span>

 

 

 



