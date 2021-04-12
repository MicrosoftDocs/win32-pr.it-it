---
description: Installare un pacchetto di Windows Installer con privilegi elevati (di sistema).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528878"
---
# <a name="alwaysinstallelevated"></a><span data-ttu-id="f633c-103">AlwaysInstallElevated</span><span class="sxs-lookup"><span data-stu-id="f633c-103">AlwaysInstallElevated</span></span>

<span data-ttu-id="f633c-104">È possibile usare il criterio AlwaysInstallElevated per installare un pacchetto di Windows Installer con privilegi elevati (di sistema).</span><span class="sxs-lookup"><span data-stu-id="f633c-104">You can use the AlwaysInstallElevated policy to install a Windows Installer package with elevated (system) privileges.</span></span>

<span data-ttu-id="f633c-105">\* \* Avviso: \* \*</span><span class="sxs-lookup"><span data-stu-id="f633c-105">\*\*Warning:  \*\*</span></span>

<span data-ttu-id="f633c-106">Questa opzione equivale alla concessione di diritti amministrativi completi che possono comportare un notevole rischio di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f633c-106">This option is equivalent to granting full administrative rights, which can pose a massive security risk.</span></span> <span data-ttu-id="f633c-107">Microsoft sconsiglia vivamente l'uso di questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="f633c-107">Microsoft strongly discourages the use of this setting.</span></span>

<span data-ttu-id="f633c-108">Per installare un pacchetto con privilegi elevati (di sistema), impostare il valore AlwaysInstallElevated su "1" in entrambe le chiavi del registro di sistema seguenti:</span><span class="sxs-lookup"><span data-stu-id="f633c-108">To install a package with elevated (system) privileges, set the AlwaysInstallElevated value to "1" under both of the following registry keys:</span></span>

<span data-ttu-id="f633c-109">**HKEY \_ Criteri \_ software utente correnti** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="f633c-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="f633c-110">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="f633c-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="f633c-111">Se il valore AlwaysInstallElevated non è impostato su "1" in entrambe le chiavi del registro di sistema precedenti, il programma di installazione utilizza privilegi elevati per installare le applicazioni gestite e utilizza il livello di privilegio dell'utente corrente per le applicazioni non gestite.</span><span class="sxs-lookup"><span data-stu-id="f633c-111">If the AlwaysInstallElevated value is not set to "1" under both of the preceding registry keys, the installer uses elevated privileges to install managed applications and uses the current user's privilege level for unmanaged applications.</span></span>

<span data-ttu-id="f633c-112">Poiché questo criterio consente agli utenti di installare applicazioni che richiedono l'accesso alle directory e alle chiavi del registro di sistema per le quali l'utente non dispone delle autorizzazioni per la visualizzazione o la modifica, è necessario valutare se fornisce agli utenti un livello di sicurezza appropriato.</span><span class="sxs-lookup"><span data-stu-id="f633c-112">Because this policy permits users to install applications that require access to directories and registry keys for which the user may not have permission to view or change, you should consider whether it provides your users with an appropriate level of security.</span></span> <span data-ttu-id="f633c-113">L'impostazione di questo criterio indica Windows Installer di utilizzare le autorizzazioni di sistema durante l'installazione dell'applicazione nel sistema.</span><span class="sxs-lookup"><span data-stu-id="f633c-113">Setting this policy directs Windows Installer to use system permissions when it installs the application on the system.</span></span> <span data-ttu-id="f633c-114">Se questo criterio non è impostato, le applicazioni non distribuite dall'amministratore vengono installate usando i privilegi dell'utente e solo le applicazioni gestite ottengono privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="f633c-114">If this policy is not set, applications not distributed by the administrator are installed using the user's privileges and only managed applications get elevated privileges.</span></span>

<span data-ttu-id="f633c-115">Si noti che quando il criterio per computer per AlwaysInstallElevated è abilitato, qualsiasi utente può impostare l'impostazione per utente.</span><span class="sxs-lookup"><span data-stu-id="f633c-115">Note that once the per-machine policy for AlwaysInstallElevated is enabled, any user can set their per-user setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="f633c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f633c-116">Remarks</span></span>

<span data-ttu-id="f633c-117">Per informazioni sull'interazione di questi criteri con le origini di installazione, vedere [gestione delle origini di installazione](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="f633c-117">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="f633c-118">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f633c-118">Data Type</span></span>

<span data-ttu-id="f633c-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f633c-119">**REG\_DWORD**</span></span>

 

 



