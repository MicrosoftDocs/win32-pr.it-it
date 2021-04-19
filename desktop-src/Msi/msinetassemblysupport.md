---
description: La proprietà MsiNetAssemblySupport indica se il computer supporta gli assembly Common Language Runtime.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: Proprietà MsiNetAssemblySupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326771"
---
# <a name="msinetassemblysupport-property"></a><span data-ttu-id="24a95-103">Proprietà MsiNetAssemblySupport</span><span class="sxs-lookup"><span data-stu-id="24a95-103">MsiNetAssemblySupport property</span></span>

<span data-ttu-id="24a95-104">La proprietà **MsiNetAssemblySupport** indica se il computer supporta gli assembly Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="24a95-104">The **MsiNetAssemblySupport** property indicates whether the computer supports common language run-time assemblies.</span></span> <span data-ttu-id="24a95-105">Nei sistemi che supportano gli assembly di runtime del linguaggio comune, il programma di installazione imposta il valore di **MsiNetAssemblySupport** sulla versione del file di Fusion.dll.</span><span class="sxs-lookup"><span data-stu-id="24a95-105">On systems that support common language run-time assemblies, the installer sets the value of **MsiNetAssemblySupport** to the file version of Fusion.dll.</span></span> <span data-ttu-id="24a95-106">Il programma di installazione non imposta questa proprietà se il sistema operativo non supporta gli assembly Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="24a95-106">The installer does not set this property if the operating system does not support common language run-time assemblies.</span></span> <span data-ttu-id="24a95-107">Quando più versioni di Fusion.dll vengono installate side-by-side nel computer dell'utente, questa proprietà viene impostata sulla versione più recente del file di Fusion.dll.</span><span class="sxs-lookup"><span data-stu-id="24a95-107">When multiple versions of Fusion.dll are installed side-by-side on the user's computer, this property is set to the latest version of the Fusion.dll file.</span></span> <span data-ttu-id="24a95-108">Se, ad esempio, .NET Framework versione 1.0.3705 (Fusion.dll versione 1.0.3705.15) e .NET Framework versione 1.1.4322 (Fusion.dll versione 1.1.4322.314) vengono installate side-by-Side, la proprietà **MsiNetAssemblySupport** è impostata su 1.1.4322.314.</span><span class="sxs-lookup"><span data-stu-id="24a95-108">For example, if .NET Framework version 1.0.3705 (Fusion.dll version 1.0.3705.15)and .NET Framework version 1.1.4322 (Fusion.dll version 1.1.4322.314) are installed side-by-side, the **MsiNetAssemblySupport** property is set to 1.1.4322.314.</span></span> <span data-ttu-id="24a95-109">Per ulteriori informazioni, vedere [assembly](assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="24a95-109">For more information, see [Assemblies](assemblies.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24a95-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24a95-110">Requirements</span></span>



| <span data-ttu-id="24a95-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="24a95-111">Requirement</span></span> | <span data-ttu-id="24a95-112">Valore</span><span class="sxs-lookup"><span data-stu-id="24a95-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24a95-113">Versione</span><span class="sxs-lookup"><span data-stu-id="24a95-113">Version</span></span><br/> | <span data-ttu-id="24a95-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="24a95-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="24a95-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="24a95-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="24a95-116">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="24a95-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="24a95-117">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="24a95-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24a95-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24a95-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a95-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="24a95-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




