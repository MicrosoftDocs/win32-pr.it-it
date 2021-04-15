---
title: EnableDCOM
description: Controlla i criteri di attivazione e chiamata globali del computer. Solo gli amministratori e il sistema hanno accesso completo a questa parte del registro di sistema. Tutti gli altri utenti hanno accesso in sola lettura.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Valore EnableDCOM del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395671"
---
# <a name="enabledcom"></a><span data-ttu-id="875da-106">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="875da-106">EnableDCOM</span></span>

<span data-ttu-id="875da-107">Controlla i criteri di attivazione e chiamata globali del computer.</span><span class="sxs-lookup"><span data-stu-id="875da-107">Controls the global activation and call policies of the machine.</span></span> <span data-ttu-id="875da-108">Solo gli amministratori e il sistema hanno accesso completo a questa parte del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="875da-108">Only administrators and the system have full access to this portion of the registry.</span></span> <span data-ttu-id="875da-109">Tutti gli altri utenti hanno accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="875da-109">All other users have read-only access.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="875da-110">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="875da-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a><span data-ttu-id="875da-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="875da-111">Remarks</span></span>

<span data-ttu-id="875da-112">Si tratta di un valore **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="875da-112">This is a **REG\_SZ** value.</span></span>



| <span data-ttu-id="875da-113">Valore</span><span class="sxs-lookup"><span data-stu-id="875da-113">Value</span></span>    | <span data-ttu-id="875da-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="875da-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="875da-115">N (o n)</span><span class="sxs-lookup"><span data-stu-id="875da-115">N (or n)</span></span> | <span data-ttu-id="875da-116">Nessun client remoto può avviare Server o connettersi a oggetti nel computer.</span><span class="sxs-lookup"><span data-stu-id="875da-116">No remote clients may launch servers or connect to objects on this computer.</span></span> <span data-ttu-id="875da-117">I client locali non possono accedere ai server DCOM remoti; tutto il traffico DCOM è bloccato.</span><span class="sxs-lookup"><span data-stu-id="875da-117">Local clients cannot access remote DCOM servers; all DCOM traffic is blocked.</span></span> <span data-ttu-id="875da-118">L'avvio locale del codice della classe e la connessione a oggetti sono consentiti per ogni classe in base al valore e alle autorizzazioni di accesso del valore del registro di sistema [**LaunchPermission**](launchpermission.md) della classe e al valore del registro di sistema [**DefaultLaunchPermission**](defaultlaunchpermission.md) globale.</span><span class="sxs-lookup"><span data-stu-id="875da-118">Local launching of class code and connecting to objects are allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span> |
| <span data-ttu-id="875da-119">Y (o y)</span><span class="sxs-lookup"><span data-stu-id="875da-119">Y (or y)</span></span> | <span data-ttu-id="875da-120">L'avvio di server e la connessione a oggetti da parte di client remoti sono consentiti in base alle singole classi in base al valore e alle autorizzazioni di accesso del valore del registro di sistema [**LaunchPermission**](launchpermission.md) della classe e al valore del registro di sistema [**DefaultLaunchPermission**](defaultlaunchpermission.md) globale.</span><span class="sxs-lookup"><span data-stu-id="875da-120">Launching of servers and connecting to objects by remote clients is allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span>                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="875da-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="875da-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="875da-122">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="875da-122">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="875da-123">**LaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="875da-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="875da-124">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="875da-124">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




