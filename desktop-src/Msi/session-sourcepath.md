---
description: La proprietà SourcePath dell'oggetto Session è una proprietà di sola lettura che fornisce il percorso completo della cartella designata nel supporto di origine o nell'immagine server.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Proprietà Session. SourcePath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333035"
---
# <a name="sessionsourcepath-property"></a><span data-ttu-id="eb831-103">Proprietà Session. SourcePath</span><span class="sxs-lookup"><span data-stu-id="eb831-103">Session.SourcePath property</span></span>

<span data-ttu-id="eb831-104">La proprietà **SourcePath** dell'oggetto [**Session**](session-object.md) è una proprietà di sola lettura che fornisce il percorso completo della cartella designata nel supporto di origine o nell'immagine server.</span><span class="sxs-lookup"><span data-stu-id="eb831-104">The **SourcePath** property of the [**Session**](session-object.md) object is a read-only property that provides the full path to the designated folder on the source media or server image.</span></span>

<span data-ttu-id="eb831-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="eb831-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb831-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb831-106">Syntax</span></span>


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a><span data-ttu-id="eb831-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="eb831-107">Property value</span></span>

<span data-ttu-id="eb831-108">Obbligatorio nome con distinzione tra maiuscole e minuscole di una proprietà di cartella specificata da una chiave primaria della [tabella di directory](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb831-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="eb831-109">Se la cartella non esiste, viene generato un errore.</span><span class="sxs-lookup"><span data-stu-id="eb831-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb831-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb831-110">Remarks</span></span>

<span data-ttu-id="eb831-111">Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="eb831-111">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb831-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb831-112">Requirements</span></span>



| <span data-ttu-id="eb831-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb831-113">Requirement</span></span> | <span data-ttu-id="eb831-114">Valore</span><span class="sxs-lookup"><span data-stu-id="eb831-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb831-115">Versione</span><span class="sxs-lookup"><span data-stu-id="eb831-115">Version</span></span><br/> | <span data-ttu-id="eb831-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eb831-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="eb831-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eb831-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="eb831-118">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="eb831-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="eb831-119">DLL</span><span class="sxs-lookup"><span data-stu-id="eb831-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="eb831-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb831-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="eb831-121">IID</span><span class="sxs-lookup"><span data-stu-id="eb831-121">IID</span></span><br/>     | <span data-ttu-id="eb831-122">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="eb831-122">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




