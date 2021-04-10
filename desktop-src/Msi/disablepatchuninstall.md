---
description: Se il criterio di sistema per computer è impostato su 1, le patch non possono essere rimosse dal computer da un utente o da un amministratore.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879686"
---
# <a name="disablepatchuninstall"></a><span data-ttu-id="e16e3-103">DisablePatchUninstall</span><span class="sxs-lookup"><span data-stu-id="e16e3-103">DisablePatchUninstall</span></span>

<span data-ttu-id="e16e3-104">Se il [criterio di sistema](system-policy.md) per computer è impostato su 1, le patch non possono essere rimosse dal computer da un utente o da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="e16e3-104">If this per-machine [system policy](system-policy.md) is set to 1, patches cannot be removed from the computer by a user or an administrator.</span></span> <span data-ttu-id="e16e3-105">Il Windows Installer può comunque rimuovere una patch che non è più applicabile a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="e16e3-105">The Windows Installer can still remove a patch that is no longer applicable to a product.</span></span> <span data-ttu-id="e16e3-106">Se questo criterio non è impostato, un utente può rimuovere una patch dal computer solo se l'utente dispone dei privilegi necessari per rimuovere la patch.</span><span class="sxs-lookup"><span data-stu-id="e16e3-106">If this policy is not set, a user can remove a patch from the computer only if the user has been granted privileges to remove the patch.</span></span> <span data-ttu-id="e16e3-107">Questo può dipendere dal fatto che l'utente sia un amministratore, che siano impostate le impostazioni dei criteri [DisableMsi](disablemsi.md) e [AlwaysInstallElevated](alwaysinstallelevated.md) e che la patch sia stata installata in un contesto gestito per utente, per utente non gestito o per computer.</span><span class="sxs-lookup"><span data-stu-id="e16e3-107">This can depend on whether the user is an administrator, whether [DisableMsi](disablemsi.md) and [AlwaysInstallElevated](alwaysinstallelevated.md) policy settings are set, and whether the patch was installed in a per-user managed, per-user unmanaged, or per-machine context.</span></span>

## <a name="registry-key"></a><span data-ttu-id="e16e3-108">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e16e3-108">Registry Key</span></span>

<span data-ttu-id="e16e3-109">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="e16e3-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="e16e3-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e16e3-110">Data Type</span></span>

<span data-ttu-id="e16e3-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e16e3-111">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="e16e3-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e16e3-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e16e3-113">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="e16e3-113">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



