---
description: Questa proprietà Windows Installer indica quando il livello dell'interfaccia utente interna è stato impostato per nascondere il pulsante Annulla.
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: Proprietà MsiUIHideCancel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a25a940921dd4b0d91155765ee6768ec0d6d2bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331073"
---
# <a name="msiuihidecancel-property"></a><span data-ttu-id="7cce4-103">Proprietà MsiUIHideCancel</span><span class="sxs-lookup"><span data-stu-id="7cce4-103">MsiUIHideCancel property</span></span>

<span data-ttu-id="7cce4-104">Il programma di installazione imposta la proprietà **MsiUIHideCancel** su 1 quando il livello dell'interfaccia utente interna è stato impostato in modo da includere INSTALLUILEVEL \_ HIDECANCEL con la funzione [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) o la proprietà [UILevel](installer-uilevel.md)dell'oggetto del [**programma di installazione**](installer-object.md) o tramite opzioni della [riga di comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="7cce4-104">The installer sets the **MsiUIHideCancel** property to 1 when the internal user interface level has been set to include INSTALLUILEVEL\_HIDECANCEL with the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function or the [UILevel](installer-uilevel.md)property of the [**Installer**](installer-object.md) object or by using [Command Line Options](command-line-options.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cce4-105">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cce4-105">Requirements</span></span>



| <span data-ttu-id="7cce4-106">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cce4-106">Requirement</span></span> | <span data-ttu-id="7cce4-107">Valore</span><span class="sxs-lookup"><span data-stu-id="7cce4-107">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cce4-108">Versione</span><span class="sxs-lookup"><span data-stu-id="7cce4-108">Version</span></span><br/> | <span data-ttu-id="7cce4-109">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7cce4-109">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7cce4-110">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7cce4-110">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7cce4-111">Windows Installer 3,0 o versioni successive in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7cce4-111">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7cce4-112">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7cce4-112">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7cce4-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cce4-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cce4-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7cce4-114">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="7cce4-115">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="7cce4-115">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




