---
description: La proprietà TargetPath dell'oggetto Session è una proprietà di lettura/scrittura che fornisce il percorso completo della cartella designata nell'unità di destinazione dell'installazione.
ms.assetid: 563b874e-c669-4f5b-b3fa-eeb6b6e578f2
title: Proprietà Session. TargetPath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.TargetPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6c5917f845da0eec944e797d5f49f52d0ec26913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333034"
---
# <a name="sessiontargetpath-property"></a><span data-ttu-id="8e2ff-103">Proprietà Session. TargetPath</span><span class="sxs-lookup"><span data-stu-id="8e2ff-103">Session.TargetPath property</span></span>

<span data-ttu-id="8e2ff-104">La proprietà **targetPath** dell'oggetto [**Session**](session-object.md) è una proprietà di lettura/scrittura che fornisce il percorso completo della cartella designata nell'unità di destinazione dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-104">The **TargetPath** property of the [**Session**](session-object.md) object is a read-write property that provides the full path to the designated folder on the installation target drive.</span></span>

<span data-ttu-id="8e2ff-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e2ff-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e2ff-106">Syntax</span></span>


```JScript
propVal = Session.TargetPath
Session.TargetPath = propVal 
```



## <a name="property-value"></a><span data-ttu-id="8e2ff-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8e2ff-107">Property value</span></span>

<span data-ttu-id="8e2ff-108">Obbligatorio nome con distinzione tra maiuscole e minuscole di una proprietà di cartella specificata da una chiave primaria della [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="8e2ff-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="8e2ff-109">Se la cartella non esiste, viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e2ff-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e2ff-110">Remarks</span></span>

<span data-ttu-id="8e2ff-111">Non tentare di configurare il percorso di destinazione se i componenti che utilizzano tali percorsi sono già installati per l'utente corrente o per un altro utente.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-111">Do not attempt to configure the target path if the components using those paths are already installed for the current user or for a different user.</span></span> <span data-ttu-id="8e2ff-112">Controllare la proprietà [**ProductState**](productstate.md) per determinare se il prodotto che contiene il componente è installato.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-112">Check the [**ProductState**](productstate.md) property to determine if the product that contains the component is installed.</span></span>

<span data-ttu-id="8e2ff-113">Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="8e2ff-113">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e2ff-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e2ff-114">Requirements</span></span>



| <span data-ttu-id="8e2ff-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e2ff-115">Requirement</span></span> | <span data-ttu-id="8e2ff-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8e2ff-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e2ff-117">Versione</span><span class="sxs-lookup"><span data-stu-id="8e2ff-117">Version</span></span><br/> | <span data-ttu-id="8e2ff-118">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8e2ff-119">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8e2ff-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8e2ff-120">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="8e2ff-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8e2ff-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8e2ff-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="8e2ff-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e2ff-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8e2ff-123">IID</span><span class="sxs-lookup"><span data-stu-id="8e2ff-123">IID</span></span><br/>     | <span data-ttu-id="8e2ff-124">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8e2ff-124">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




