---
title: MachineAccessRestriction
description: Imposta i criteri di restrizione a livello di computer per l'accesso al componente.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- Valore MachineAccessRestriction del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298633"
---
# <a name="machineaccessrestriction"></a><span data-ttu-id="08fc3-104">MachineAccessRestriction</span><span class="sxs-lookup"><span data-stu-id="08fc3-104">MachineAccessRestriction</span></span>

<span data-ttu-id="08fc3-105">Imposta i criteri di restrizione a livello di computer per l'accesso al componente.</span><span class="sxs-lookup"><span data-stu-id="08fc3-105">Sets the computer-wide restriction policy for component access.</span></span>

> [!Caution]  
> <span data-ttu-id="08fc3-106">La modifica di questo valore influirà su tutte le applicazioni server COM e potrebbe impedire il corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="08fc3-106">Changing this value will affect all COM server applications, and might prevent them from working properly.</span></span> <span data-ttu-id="08fc3-107">Se sono presenti applicazioni server COM con restrizioni meno restrittive rispetto a quelle a livello di computer, la riduzione delle restrizioni a livello di computer può esporre tali applicazioni a accessi non desiderati.</span><span class="sxs-lookup"><span data-stu-id="08fc3-107">If there are COM server applications that have restrictions that are less stringent than the computer-wide restrictions, reducing the computer-wide restrictions may expose these applications to unwanted access.</span></span> <span data-ttu-id="08fc3-108">Viceversa, se si aumentano le restrizioni a livello di computer, alcune applicazioni server COM potrebbero non essere più accessibili chiamando le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="08fc3-108">Conversely, if you increase the computer-wide restrictions, some COM server applications might no longer be accessible by calling applications.</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="08fc3-109">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="08fc3-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a><span data-ttu-id="08fc3-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="08fc3-110">Remarks</span></span>

<span data-ttu-id="08fc3-111">Si tratta di un valore **\_ binario REG** .</span><span class="sxs-lookup"><span data-stu-id="08fc3-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="08fc3-112">Le entità non concesse in questo caso non possono ottenerle anche se le autorizzazioni vengono concesse dal valore del registro di sistema [DefaultAccessPermission](defaultaccesspermission.md) o dalla funzione [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="08fc3-112">Principals not given permissions here cannot obtain them even if the permissions are granted by the [DefaultAccessPermission](defaultaccesspermission.md) registry value or by the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function.</span></span>

<span data-ttu-id="08fc3-113">Per impostazione predefinita, i membri del gruppo Everyone possono ottenere le autorizzazioni di accesso locale e remoto, mentre gli utenti anonimi possono ottenere le autorizzazioni di accesso locale.</span><span class="sxs-lookup"><span data-stu-id="08fc3-113">By default, members of the Everyone group can obtain local and remote access permissions, and anonymous users can obtain local access permissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08fc3-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08fc3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08fc3-115">Impostazione della sicurezza per le applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="08fc3-115">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




