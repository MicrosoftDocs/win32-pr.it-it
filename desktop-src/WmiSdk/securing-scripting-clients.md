---
description: Per gli script e le applicazioni Visual Basic è necessario impostare la sicurezza DCOM, in particolare per l'accesso remoto, e potrebbe inoltre essere necessario abilitare i privilegi.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Protezione dei client di scripting
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226822"
---
# <a name="securing-scripting-clients"></a><span data-ttu-id="90adf-103">Protezione dei client di scripting</span><span class="sxs-lookup"><span data-stu-id="90adf-103">Securing Scripting Clients</span></span>

<span data-ttu-id="90adf-104">Per gli script e le applicazioni Visual Basic è necessario impostare la sicurezza DCOM, in particolare per l'accesso remoto, e potrebbe inoltre essere necessario abilitare i privilegi.</span><span class="sxs-lookup"><span data-stu-id="90adf-104">Scripts and Visual Basic applications must set DCOM security, especially for remote access, and may also need to enable privileges.</span></span>

## <a name="default-access-permissions"></a><span data-ttu-id="90adf-105">Autorizzazioni di accesso predefinite</span><span class="sxs-lookup"><span data-stu-id="90adf-105">Default Access Permissions</span></span>

<span data-ttu-id="90adf-106">L'accesso WMI è diverso tra computer locali e remoti.</span><span class="sxs-lookup"><span data-stu-id="90adf-106">WMI access differs between local and remote computers.</span></span> <span data-ttu-id="90adf-107">Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="90adf-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="90adf-108">Di seguito sono riportate le autorizzazioni di accesso predefinite per account:</span><span class="sxs-lookup"><span data-stu-id="90adf-108">The following are the default access permissions by account:</span></span>

-   <span data-ttu-id="90adf-109">Tutti, LocalService, NetworkService</span><span class="sxs-lookup"><span data-stu-id="90adf-109">Everyone, LocalService, NetworkService</span></span>

    <span data-ttu-id="90adf-110">Autorizzazione per la lettura o la scrittura di dati e per l'esecuzione di [*metodi del provider*](gloss-p.md) nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="90adf-110">Permission to read or write data and to run [*provider methods*](gloss-p.md) on the local computer.</span></span> <span data-ttu-id="90adf-111">Questi account non possono creare nuove classi o installare nuovi provider.</span><span class="sxs-lookup"><span data-stu-id="90adf-111">These accounts cannot create new classes or install new providers.</span></span>

-   <span data-ttu-id="90adf-112">Account amministratore</span><span class="sxs-lookup"><span data-stu-id="90adf-112">Administrator accounts</span></span>

    <span data-ttu-id="90adf-113">Controllo completo sul computer locale.</span><span class="sxs-lookup"><span data-stu-id="90adf-113">Full control on local computer.</span></span> <span data-ttu-id="90adf-114">Quando ci si connette a un computer remoto, l'account deve essere anche un amministratore locale nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="90adf-114">When connecting to a remote computer, the account must be a local administrator on the remote computer also.</span></span>

## <a name="securing-a-scripting-client"></a><span data-ttu-id="90adf-115">Protezione di un client di scripting</span><span class="sxs-lookup"><span data-stu-id="90adf-115">Securing a Scripting Client</span></span>

<span data-ttu-id="90adf-116">Gli script WMI e le applicazioni Visual Basic devono impostare i livelli di sicurezza DCOM in modo appropriato per i sistemi operativi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="90adf-116">WMI scripting and Visual Basic applications must set DCOM security levels appropriately for the operating systems they are targeting.</span></span> <span data-ttu-id="90adf-117">Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="90adf-117">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="90adf-118">Quando ci si connette a un computer remoto, potrebbe essere necessario modificare il servizio (NTLM o Kerberos) che gestisce l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="90adf-118">When connecting to a remote computer, you may need to change the service (NTLM or Kerberos) that handles authentication.</span></span> <span data-ttu-id="90adf-119">Per ulteriori informazioni, vedere [impostazione del servizio di autenticazione tramite VBScript](setting-the-authentication-service-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="90adf-119">For more information, see [Setting the Authentication Service Using VBScript](setting-the-authentication-service-using-vbscript.md).</span></span>

<span data-ttu-id="90adf-120">L'accesso ad alcune classi o dati WMI potrebbe richiedere un privilegio non abilitato.</span><span class="sxs-lookup"><span data-stu-id="90adf-120">Access to some WMI classes or data may require a privilege that is not enabled.</span></span> <span data-ttu-id="90adf-121">Ad esempio, è necessario includere il privilegio di sicurezza quando ci si connette alla classe [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="90adf-121">For example, you must include the Security privilege when connecting to the [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) class.</span></span> <span data-ttu-id="90adf-122">Per ulteriori informazioni, vedere [esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="90adf-122">For more information, see [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="90adf-123">Se si accede a WMI da una pagina di Active Server (ASP), è necessaria una configurazione di IIS.</span><span class="sxs-lookup"><span data-stu-id="90adf-123">If you are accessing WMI from an Active Server Page (ASP), then some IIS configuration is required.</span></span> <span data-ttu-id="90adf-124">Per ulteriori informazioni, vedere [la pagina relativa alla configurazione di IIS 5,0 e versioni successive per lo scripting ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="90adf-124">For more information, see [Configuring IIS 5.0 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>

<span data-ttu-id="90adf-125">È possibile che si stia tentando di connettersi a uno spazio dei nomi che richiede una connessione crittografata, ovvero una connessione che richiede un livello di autenticazione su PktPrivacy.</span><span class="sxs-lookup"><span data-stu-id="90adf-125">You may be trying to connect to a namespace which requires an encrypted connection, in other words, one that requires an authentication level of pktPrivacy.</span></span> <span data-ttu-id="90adf-126">Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="90adf-126">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

 

 
