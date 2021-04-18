---
title: DefaultLaunchPermission
description: Definisce l'elenco di controllo di accesso (ACL) delle entità che possono avviare classi che non specificano il proprio ACL tramite il valore del registro di sistema LaunchPermission.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- Valore DefaultLaunchPermission del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298985"
---
# <a name="defaultlaunchpermission"></a><span data-ttu-id="1fdbd-104">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="1fdbd-104">DefaultLaunchPermission</span></span>

<span data-ttu-id="1fdbd-105">Definisce l'elenco di controllo di accesso (ACL) delle entità che possono avviare classi che non specificano il proprio ACL tramite il valore del registro di sistema [**LaunchPermission**](launchpermission.md) .</span><span class="sxs-lookup"><span data-stu-id="1fdbd-105">Defines the Access Control List (ACL) of the principals that can launch classes that do not specify their own ACL through the [**LaunchPermission**](launchpermission.md) registry value.</span></span>

> [!Caution]  
> <span data-ttu-id="1fdbd-106">Non è consigliabile modificare questo valore, perché questo influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo e potrebbe impedire il corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="1fdbd-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="1fdbd-107">Se si modifica questo valore in modo da influire sulle impostazioni di sicurezza di una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM.</span><span class="sxs-lookup"><span data-stu-id="1fdbd-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="1fdbd-108">Per altre informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione della sicurezza a livello di processo](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="1fdbd-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="1fdbd-109">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="1fdbd-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="1fdbd-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fdbd-110">Remarks</span></span>

<span data-ttu-id="1fdbd-111">Si tratta di un valore **\_ binario REG** .</span><span class="sxs-lookup"><span data-stu-id="1fdbd-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="1fdbd-112">Di seguito sono riportate le autorizzazioni di accesso predefinite:</span><span class="sxs-lookup"><span data-stu-id="1fdbd-112">The default access permissions are as follows:</span></span>

-   <span data-ttu-id="1fdbd-113">Amministratori: Consenti avvio</span><span class="sxs-lookup"><span data-stu-id="1fdbd-113">Administrators: allow launch</span></span>
-   <span data-ttu-id="1fdbd-114">SISTEMA: Consenti avvio</span><span class="sxs-lookup"><span data-stu-id="1fdbd-114">SYSTEM: allow launch</span></span>
-   <span data-ttu-id="1fdbd-115">INTERATTIVO: Consenti avvio</span><span class="sxs-lookup"><span data-stu-id="1fdbd-115">INTERACTIVE: allow launch</span></span>

<span data-ttu-id="1fdbd-116">Se il valore [**LaunchPermission**](launchpermission.md) è impostato per un server, avrà la precedenza sul valore di **DefaultLaunchPermission** .</span><span class="sxs-lookup"><span data-stu-id="1fdbd-116">If the [**LaunchPermission**](launchpermission.md) value is set for a server, it takes precedence over the **DefaultLaunchPermission** value.</span></span> <span data-ttu-id="1fdbd-117">Quando riceve una richiesta locale o remota per l'avvio di un server la cui chiave [**AppID**](appid-key.md) non ha un valore **LAUNCHPERMISSION** , l'ACL descritto da questo valore viene verificato durante la rappresentazione del client e il relativo esito positivo consente o impedisce l'avvio del codice della classe.</span><span class="sxs-lookup"><span data-stu-id="1fdbd-117">Upon receiving a local or remote request to launch a server whose [**AppID**](appid-key.md) key has no **LaunchPermission** value of its own, the ACL described by this value is checked while impersonating the client and its success either allows or disallows the launching of the class code.</span></span>

<span data-ttu-id="1fdbd-118">Questo valore fornisce un semplice livello di amministrazione centralizzata dell'accesso di avvio predefinito a classi altrimenti non amministrate in un computer.</span><span class="sxs-lookup"><span data-stu-id="1fdbd-118">This value provides a simple level of centralized administration of the default launching access to otherwise unadministered classes on a computer.</span></span> <span data-ttu-id="1fdbd-119">Ad esempio, un amministratore può utilizzare lo strumento DCOMCNFG per configurare il sistema in modo da consentire l'accesso in sola lettura per gli utenti esperti.</span><span class="sxs-lookup"><span data-stu-id="1fdbd-119">For example, an administrator might use the DCOMCNFG tool to configure the system to allow read-only access for Power Users.</span></span> <span data-ttu-id="1fdbd-120">OLE limita quindi le richieste di avvio del codice della classe ai membri del gruppo Power Users.</span><span class="sxs-lookup"><span data-stu-id="1fdbd-120">OLE would therefore restrict requests to launch class code to members of the Power Users group.</span></span> <span data-ttu-id="1fdbd-121">Un amministratore potrebbe successivamente configurare le autorizzazioni di avvio per le singole classi per concedere la possibilità di avviare il codice della classe ad altri gruppi o singoli utenti in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="1fdbd-121">An administrator could subsequently configure launch permissions for individual classes to grant the ability to launch class code to other groups or individual users as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fdbd-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1fdbd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fdbd-123">**LaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="1fdbd-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="1fdbd-124">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="1fdbd-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="1fdbd-125">Impostazione della sicurezza a livello di processo</span><span class="sxs-lookup"><span data-stu-id="1fdbd-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




