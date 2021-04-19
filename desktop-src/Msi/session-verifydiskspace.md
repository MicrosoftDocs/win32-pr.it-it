---
description: La proprietà VerifyDiskSpace è una proprietà di sola lettura.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Proprietà Session. VerifyDiskSpace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333031"
---
# <a name="sessionverifydiskspace-property"></a><span data-ttu-id="90d5b-103">Proprietà Session. VerifyDiskSpace</span><span class="sxs-lookup"><span data-stu-id="90d5b-103">Session.VerifyDiskSpace property</span></span>

<span data-ttu-id="90d5b-104">La proprietà **VerifyDiskSpace** è una proprietà di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="90d5b-104">The **VerifyDiskSpace** property is a read-only property.</span></span> <span data-ttu-id="90d5b-105">Restituisce true se è disponibile spazio su disco sufficiente e false se il disco è pieno.</span><span class="sxs-lookup"><span data-stu-id="90d5b-105">It returns true if enough disk space exists and false if the disk is full.</span></span> <span data-ttu-id="90d5b-106">Poiché questa proprietà utilizza le informazioni raccolte dalle azioni di determinazione dei costi, **VerifyDiskSpace** deve essere chiamato solo dopo l' [azione CostInitialize](costinitialize-action.md), l'azione [filecost](filecost-action.md)e l' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="90d5b-106">Because this property uses information gathered by the costing actions, **VerifyDiskSpace** should only be called after the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="90d5b-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="90d5b-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d5b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90d5b-108">Syntax</span></span>


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a><span data-ttu-id="90d5b-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="90d5b-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="90d5b-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90d5b-110">Requirements</span></span>



| <span data-ttu-id="90d5b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="90d5b-111">Requirement</span></span> | <span data-ttu-id="90d5b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="90d5b-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90d5b-113">Versione</span><span class="sxs-lookup"><span data-stu-id="90d5b-113">Version</span></span><br/> | <span data-ttu-id="90d5b-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="90d5b-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="90d5b-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="90d5b-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="90d5b-116">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="90d5b-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="90d5b-117">DLL</span><span class="sxs-lookup"><span data-stu-id="90d5b-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="90d5b-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90d5b-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="90d5b-119">IID</span><span class="sxs-lookup"><span data-stu-id="90d5b-119">IID</span></span><br/>     | <span data-ttu-id="90d5b-120">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="90d5b-120">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




