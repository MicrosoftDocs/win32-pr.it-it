---
description: Contiene l'oggetto applicazione della raccolta di elementi cartella.
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: Proprietà FolderItems. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7f073b81106923f889ca5209c0aa492f4c4bbd60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127839"
---
# <a name="folderitemsapplication-property"></a><span data-ttu-id="44200-103">Proprietà FolderItems. Application</span><span class="sxs-lookup"><span data-stu-id="44200-103">FolderItems.Application property</span></span>

<span data-ttu-id="44200-104">Contiene l'oggetto **applicazione** della raccolta di elementi cartella.</span><span class="sxs-lookup"><span data-stu-id="44200-104">Contains the **Application** object of the folder items collection.</span></span>

<span data-ttu-id="44200-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="44200-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="44200-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44200-106">Syntax</span></span>


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a><span data-ttu-id="44200-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="44200-107">Property value</span></span>

<span data-ttu-id="44200-108">Riferimento all'oggetto applicazione.</span><span class="sxs-lookup"><span data-stu-id="44200-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44200-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="44200-109">Remarks</span></span>

<span data-ttu-id="44200-110">La proprietà dell' **applicazione** restituisce l'oggetto di automazione supportato dall'applicazione che contiene il controllo WebBrowser, se tale oggetto è accessibile.</span><span class="sxs-lookup"><span data-stu-id="44200-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="44200-111">In caso contrario, questa proprietà restituisce l'oggetto di automazione del controllo WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="44200-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="44200-112">Utilizzare questa proprietà con i comandi **set** e **CreateObject** oppure con il comando **GetObject** per creare e modificare un'istanza dell'applicazione Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="44200-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="44200-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44200-113">Requirements</span></span>



| <span data-ttu-id="44200-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="44200-114">Requirement</span></span> | <span data-ttu-id="44200-115">Valore</span><span class="sxs-lookup"><span data-stu-id="44200-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44200-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44200-116">Minimum supported client</span></span><br/> | <span data-ttu-id="44200-117">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="44200-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="44200-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44200-118">Minimum supported server</span></span><br/> | <span data-ttu-id="44200-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="44200-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="44200-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44200-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="44200-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="44200-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="44200-122">IDL</span><span class="sxs-lookup"><span data-stu-id="44200-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="44200-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="44200-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="44200-124">DLL</span><span class="sxs-lookup"><span data-stu-id="44200-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44200-125"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="44200-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




