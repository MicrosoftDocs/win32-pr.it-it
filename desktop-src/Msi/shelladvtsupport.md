---
description: La proprietà ShellAdvtSupport viene impostata dal programma di installazione se l'interfaccia IShellLink del sistema supporta la risoluzione del descrittore del programma di installazione.
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: Proprietà ShellAdvtSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324410"
---
# <a name="shelladvtsupport-property"></a><span data-ttu-id="ffbcd-103">Proprietà ShellAdvtSupport</span><span class="sxs-lookup"><span data-stu-id="ffbcd-103">ShellAdvtSupport property</span></span>

<span data-ttu-id="ffbcd-104">La proprietà **ShellAdvtSupport** viene impostata dal programma di installazione se l'interfaccia [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema supporta la risoluzione del descrittore del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="ffbcd-104">The **ShellAdvtSupport** property is set by the installer if the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffbcd-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffbcd-105">Remarks</span></span>

<span data-ttu-id="ffbcd-106">Se questa proprietà è impostata, l'interfaccia [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) del sistema supporta la risoluzione del descrittore del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="ffbcd-106">If this property is set, the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span> <span data-ttu-id="ffbcd-107">Questa operazione è supportata da Windows 2000 e dai sistemi che eseguono Internet Explorer 4,01.</span><span class="sxs-lookup"><span data-stu-id="ffbcd-107">This is supported by Windows 2000 and systems running Internet Explorer 4.01.</span></span> <span data-ttu-id="ffbcd-108">Se questa proprietà non è impostata, il programma di installazione ha il comportamento predefinito della creazione di funzionalità non annunciate durante l'installazione, localmente o in esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="ffbcd-108">If this property is not set, the installer has the default behavior of creating non-advertised features during installation, either locally or run from source.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffbcd-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffbcd-109">Requirements</span></span>



| <span data-ttu-id="ffbcd-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffbcd-110">Requirement</span></span> | <span data-ttu-id="ffbcd-111">Valore</span><span class="sxs-lookup"><span data-stu-id="ffbcd-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffbcd-112">Versione</span><span class="sxs-lookup"><span data-stu-id="ffbcd-112">Version</span></span><br/> | <span data-ttu-id="ffbcd-113">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ffbcd-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ffbcd-114">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ffbcd-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ffbcd-115">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ffbcd-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ffbcd-116">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ffbcd-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ffbcd-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffbcd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffbcd-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ffbcd-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="ffbcd-119">Supporto della piattaforma per gli annunci</span><span class="sxs-lookup"><span data-stu-id="ffbcd-119">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)
</dt> </dl>

 

 
