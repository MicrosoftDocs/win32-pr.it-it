---
description: La proprietà Version dell'oggetto Installer è una proprietà di sola lettura che rappresenta la rappresentazione di stringa della versione corrente di Windows Installer. La stringa viene restituita nel formato seguente.
ms.assetid: 9af262f0-b573-471d-aac6-6a72e8cb5314
title: Proprietà Installer. Version
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Version
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 29af85b8fc1afe468dc87d5516da9a528024c73a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332162"
---
# <a name="installerversion-property"></a><span data-ttu-id="f8516-104">Proprietà Installer. Version</span><span class="sxs-lookup"><span data-stu-id="f8516-104">Installer.Version property</span></span>

<span data-ttu-id="f8516-105">La proprietà **Version** dell'oggetto [**Installer**](installer-object.md) è una proprietà di sola lettura che rappresenta la rappresentazione di stringa della versione corrente di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f8516-105">The **Version** property of the [**Installer**](installer-object.md) object is a read-only property that is the string representation of the current version of Windows Installer.</span></span> <span data-ttu-id="f8516-106">La stringa viene restituita nel formato seguente.</span><span class="sxs-lookup"><span data-stu-id="f8516-106">The string is returned in the following form.</span></span>

<span data-ttu-id="f8516-107">*principale*. *minore*. *compilazione*. *aggiornamento* di</span><span class="sxs-lookup"><span data-stu-id="f8516-107">*major*.*minor*.*build*.*update*</span></span>

<span data-ttu-id="f8516-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f8516-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8516-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8516-109">Syntax</span></span>


```JScript
propVal = Installer.Version
```



## <a name="property-value"></a><span data-ttu-id="f8516-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f8516-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="f8516-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8516-111">Requirements</span></span>



| <span data-ttu-id="f8516-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8516-112">Requirement</span></span> | <span data-ttu-id="f8516-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f8516-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8516-114">Versione</span><span class="sxs-lookup"><span data-stu-id="f8516-114">Version</span></span><br/> | <span data-ttu-id="f8516-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f8516-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f8516-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f8516-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f8516-117">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="f8516-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f8516-118">DLL</span><span class="sxs-lookup"><span data-stu-id="f8516-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="f8516-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8516-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f8516-120">IID</span><span class="sxs-lookup"><span data-stu-id="f8516-120">IID</span></span><br/>     | <span data-ttu-id="f8516-121">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f8516-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




