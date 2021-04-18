---
description: L'interfaccia IVssComponent consente a un writer di ottimizzare esattamente il modo in cui i file vengono ripristinati in base al componente.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Impostazione delle destinazioni di ripristino VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310666"
---
# <a name="setting-vss-restore-targets"></a><span data-ttu-id="dc3f0-103">Impostazione delle destinazioni di ripristino VSS</span><span class="sxs-lookup"><span data-stu-id="dc3f0-103">Setting VSS Restore Targets</span></span>

<span data-ttu-id="dc3f0-104">L'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) consente a un writer di ottimizzare esattamente il modo in cui i file vengono ripristinati in base al componente.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-104">The [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface enables a writer to fine-tune exactly how files are restored on a component-by-component basis.</span></span>

<span data-ttu-id="dc3f0-105">Poiché è possibile che la configurazione di sistema durante l'operazione di ripristino sia diversa da quella prevista durante il backup, viene fornito il meccanismo di destinazione del ripristino.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-105">Because it is possible that the system configuration during restore is something other than that anticipated during backup, the restore target mechanism is provided.</span></span>

<span data-ttu-id="dc3f0-106">Consente ai writer di chiamare [**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) per modificare il modo in cui vengono ripristinati i componenti [*inclusi in modo esplicito*](vssgloss-e.md) nel documento dei componenti di backup.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-106">It allows writers to call [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) to change how those components that are [*explicitly included*](vssgloss-e.md) in the Backup Components Document are restored.</span></span> <span data-ttu-id="dc3f0-107">Questa operazione modifica anche il meccanismo di ripristino utilizzato in questi componenti [*inclusi in modo implicito*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="dc3f0-107">This also changes the restoration mechanism used on those components that are [*implicitly included*](vssgloss-i.md).</span></span>

<span data-ttu-id="dc3f0-108">Ripristino del file che si verifica durante un riavvio del sistema (nei valori di enumerazione VSS [**\_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) VSS \_ RME \_ Restore \_ al \_ riavvio e VSS \_ RME \_ Restore \_ al \_ riavvio \_ se \_ non è possibile \_ sostituire) non può essere influenzato dalle destinazioni di ripristino perché non sono in esecuzione servizi VSS quando **MoveFileEx** copia i file nel percorso finale.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-108">File restoration that takes place during a system reboot (under the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration values VSS\_RME\_RESTORE\_AT\_REBOOT and VSS\_RME\_RESTORE\_AT\_REBOOT\_IF\_CANNOT\_REPLACE) cannot be affected by restore targets because there are no running VSS services when **MoveFileEx** copies files to their final location.</span></span>

<span data-ttu-id="dc3f0-109">Analogamente, \_ i \_ ripristini personalizzati di VSS RME possono o meno essere interessati, perché ogni ripristino personalizzato è specifico di un determinato writer e può scegliere di rispettare o ignorare le destinazioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-109">Similarly, VSS\_RME\_CUSTOM restores may or may not be affected, because each custom restore is specific to a given writer and can choose to respect or ignore restore targets.</span></span>

<span data-ttu-id="dc3f0-110">I richiedenti e i writer possono utilizzare [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) per verificare la destinazione di ripristino di un set di componenti.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-110">Requesters and writers can use [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) to check the restore target of a component set.</span></span>

<span data-ttu-id="dc3f0-111">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) supporta le seguenti destinazioni di ripristino, che possono essere impostate su un componente impostato in base al set di componenti:</span><span class="sxs-lookup"><span data-stu-id="dc3f0-111">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) supports the following restore targets, which can be set on a component set by component set basis:</span></span>

-   <span data-ttu-id="dc3f0-112">\_originale VSS RT \_ .</span><span class="sxs-lookup"><span data-stu-id="dc3f0-112">VSS\_RT\_ORIGINAL.</span></span> <span data-ttu-id="dc3f0-113">Verrà rispettato il metodo di ripristino specificato dall'enumerazione [**\_ RESTOREMETHOD \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) dell'enumerazione VSS.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-113">The restore method specified by the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration will be respected.</span></span>
-   <span data-ttu-id="dc3f0-114">\_alternativa VSS RT \_ .</span><span class="sxs-lookup"><span data-stu-id="dc3f0-114">VSS\_RT\_ALTERNATE.</span></span> <span data-ttu-id="dc3f0-115">I file vengono ripristinati in un percorso determinato da un mapping del percorso alternativo esistente.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-115">The files are restored to a location determined from an existing alternate location mapping.</span></span> <span data-ttu-id="dc3f0-116">Se esiste un mapping del percorso alternativo corrispondente a un percorso in un sottocomponente del set di componenti, eseguire il ripristino nel percorso alternativo, se possibile; in caso contrario, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="dc3f0-116">If an alternate location mapping matching a path in a component set subcomponent exists, restore to the alternate location if possible; otherwise, return an error.</span></span>

 

 



