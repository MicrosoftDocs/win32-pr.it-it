---
description: L'impostazione del valore di questo criterio di sistema per computer su &\# 0034; 1&\# 0034; consente agli utenti non amministratori di utilizzare una finestra di dialogo Sfoglia per individuare le origini di applicazioni gestite.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881142"
---
# <a name="allowlockdownbrowse"></a><span data-ttu-id="55309-103">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="55309-103">AllowLockdownBrowse</span></span>

<span data-ttu-id="55309-104">L'impostazione del valore di questo criterio di [sistema](system-policy.md) per computer su "1" consente agli utenti non amministratori di utilizzare una [finestra di dialogo Sfoglia](browse-dialog.md) per individuare le origini di [*applicazioni gestite*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="55309-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" enables nonadministrative users to use a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md).</span></span> <span data-ttu-id="55309-105">Le origini possono includere supporti, ad esempio CD-ROM, URL e percorsi di rete.</span><span class="sxs-lookup"><span data-stu-id="55309-105">Sources may include media, such as CD-ROM, URLs, and network locations.</span></span> <span data-ttu-id="55309-106">Per altre informazioni, vedere [resilienza dell'origine](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="55309-106">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="55309-107">Il valore predefinito Windows Installer è che gli utenti non amministratori non possono cercare nuove origini di applicazioni gestite.</span><span class="sxs-lookup"><span data-stu-id="55309-107">The default on Windows Installer is that nonadministrative users cannot browse for new sources of managed applications.</span></span> <span data-ttu-id="55309-108">Le uniche origini disponibili sono quelle già registrate nell'elenco di origine del prodotto.</span><span class="sxs-lookup"><span data-stu-id="55309-108">The only sources available are those that are already registered in the source list of the product.</span></span> <span data-ttu-id="55309-109">Se questo criterio è impostato, un utente non amministratore potrebbe individuare le nuove origini delle applicazioni assegnate o pubblicate o installate per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="55309-109">If this policy is set, a nonadministrative user may browse for new sources of assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="55309-110">L'impostazione di AllowLockdownBrowse consente inoltre agli utenti non amministratori di eseguire programmi con privilegi LocalSystem durante un'installazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="55309-110">Setting AllowLockdownBrowse also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="55309-111">L'impostazione predefinita è consigliata per garantire un ambiente protetto.</span><span class="sxs-lookup"><span data-stu-id="55309-111">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="55309-112">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="55309-112">Registry Key</span></span>

<span data-ttu-id="55309-113">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="55309-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="55309-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="55309-114">Data Type</span></span>

<span data-ttu-id="55309-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="55309-115">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="55309-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="55309-116">Remarks</span></span>

<span data-ttu-id="55309-117">L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi arbitrari con privilegi LocalSystem se dispongono di un pacchetto di Windows Installer per l'installazione o l'avvio di tali programmi.</span><span class="sxs-lookup"><span data-stu-id="55309-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

<span data-ttu-id="55309-118">[DisableBrowse](disablebrowse.md) esegue l'override di AllowLockdownBrowse e impedisce l'esplorazione anche se è impostato AllowLockdownBrowse.</span><span class="sxs-lookup"><span data-stu-id="55309-118">[DisableBrowse](disablebrowse.md) overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

<span data-ttu-id="55309-119">Per informazioni sull'interazione di questi criteri con le origini di installazione, vedere [gestione delle origini di installazione](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="55309-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="55309-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55309-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55309-121">Resilienza di origine</span><span class="sxs-lookup"><span data-stu-id="55309-121">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="55309-122">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="55309-122">AllowLockdownMedia</span></span>](allowlockdownmedia.md)
</dt> </dl>

 

 



