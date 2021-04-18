---
description: L'impostazione del valore di questo criterio di sistema per computer su &\# 0034; 1&\# 0034; impedisce agli utenti non amministratori di utilizzare una finestra di dialogo Sfoglia per individuare le origini di applicazioni gestite archiviate su supporti, ad esempio CD-ROM.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: DisableBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305968"
---
# <a name="disablebrowse"></a><span data-ttu-id="58be8-103">DisableBrowse</span><span class="sxs-lookup"><span data-stu-id="58be8-103">DisableBrowse</span></span>

<span data-ttu-id="58be8-104">Impostando il valore di questo criterio di [sistema](system-policy.md) per computer su "1" si impedisce agli utenti non amministratori di utilizzare una [finestra di dialogo Sfoglia](browse-dialog.md) per individuare le origini di [*applicazioni gestite*](m-gly.md) archiviate su supporti, ad esempio CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="58be8-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" prevents nonadministrative users from using a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md) stored on media, such as CD-ROM.</span></span> <span data-ttu-id="58be8-105">La casella combinata "utilizza funzionalità da:" per l'input diretto è bloccata e il "Sfoglia". il pulsante è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="58be8-105">The "Use feature from:" combo box for direct input is locked and the "Browse..." button is disabled.</span></span> <span data-ttu-id="58be8-106">Per altri dettagli sull'esplorazione dell'origine, vedere [resilienza dell'origine](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="58be8-106">For more details on source browsing, see [source resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="58be8-107">DisableBrowse esegue l'override di AllowLockdownBrowse e impedisce l'esplorazione anche se è impostato AllowLockdownBrowse.</span><span class="sxs-lookup"><span data-stu-id="58be8-107">DisableBrowse overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="58be8-108">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="58be8-108">Registry Key</span></span>

<span data-ttu-id="58be8-109">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="58be8-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="58be8-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="58be8-110">Data Type</span></span>

<span data-ttu-id="58be8-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="58be8-111">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="58be8-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="58be8-112">Remarks</span></span>

<span data-ttu-id="58be8-113">In alcuni casi con DisableBrowse impostato, un utente non amministratore potrebbe ancora essere in grado di installare le applicazioni gestite dalle origini nei supporti con etichetta corretta.</span><span class="sxs-lookup"><span data-stu-id="58be8-113">In some cases with DisableBrowse set, a nonadministrative user may still be capable of installing managed applications from sources on correctly labeled media.</span></span> <span data-ttu-id="58be8-114">L'impostazione del criterio DisableBrowse Disabilita solo la possibilità di passare alle origini.</span><span class="sxs-lookup"><span data-stu-id="58be8-114">Setting the DisableBrowse policy only disables the capability to browse to sources.</span></span> <span data-ttu-id="58be8-115">Può essere usato per impedire a un utente non amministratore di passare a una nuova origine durante un'installazione, una reinstallazione o una riparazione su richiesta di installazione.</span><span class="sxs-lookup"><span data-stu-id="58be8-115">It can be used to prevent a nonadministrative user from browsing to a new source during an install-on-demand installation, reinstallation, or repair.</span></span> <span data-ttu-id="58be8-116">Se [AllowLockdownMedia](allowlockdownmedia.md) è impostato, l'utente non amministratore potrebbe comunque installare un'applicazione gestita dal supporto con etichetta corretta.</span><span class="sxs-lookup"><span data-stu-id="58be8-116">If [AllowLockdownMedia](allowlockdownmedia.md) is set, the nonadministrative user could still install a managed application from correctly labeled media.</span></span>

<span data-ttu-id="58be8-117">DisableBrowse impedisce l'esplorazione da parte dell'utente non amministratore di un nuovo percorso multimediale o di qualsiasi altro percorso di origine.</span><span class="sxs-lookup"><span data-stu-id="58be8-117">DisableBrowse prevents the nonadministrative user from browsing to a new media location or any other source location.</span></span> <span data-ttu-id="58be8-118">Per informazioni dettagliate su come proteggere le origini multimediali delle applicazioni gestite, vedere [resilienza dell'origine](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="58be8-118">For details of how to secure media sources of managed applications see [Source Resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="58be8-119">Per informazioni sull'interazione di questi criteri con le origini di installazione, vedere [gestione delle origini di installazione](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="58be8-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

 

 



