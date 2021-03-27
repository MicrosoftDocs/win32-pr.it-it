---
description: Contiene l'oggetto applicazione dell'oggetto.
ms.assetid: 305766b1-a19f-4743-a9e3-6837b3f8ffe0
title: Proprietà ShellFolderView. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ba57c407183179f580b5b616ad039c22e6fea66c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980431"
---
# <a name="shellfolderviewapplication-property"></a><span data-ttu-id="2cc74-103">Proprietà ShellFolderView. Application</span><span class="sxs-lookup"><span data-stu-id="2cc74-103">ShellFolderView.Application property</span></span>

<span data-ttu-id="2cc74-104">Contiene l'oggetto applicazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2cc74-104">Contains the object's Application object.</span></span>

<span data-ttu-id="2cc74-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2cc74-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc74-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cc74-106">Syntax</span></span>


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a><span data-ttu-id="2cc74-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2cc74-107">Property value</span></span>

<span data-ttu-id="2cc74-108">Variabile di tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto applicazione.</span><span class="sxs-lookup"><span data-stu-id="2cc74-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cc74-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cc74-109">Remarks</span></span>

<span data-ttu-id="2cc74-110">La proprietà dell' **applicazione** restituisce l'oggetto di automazione supportato dall'applicazione che contiene il controllo WebBrowser, se tale oggetto è accessibile.</span><span class="sxs-lookup"><span data-stu-id="2cc74-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="2cc74-111">In caso contrario, questa proprietà restituisce l'oggetto di automazione del controllo WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="2cc74-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="2cc74-112">Utilizzare questa proprietà con i comandi **set** e **CreateObject** oppure con il comando **GetObject** per creare e modificare un'istanza dell'applicazione Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="2cc74-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc74-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cc74-113">Requirements</span></span>



| <span data-ttu-id="2cc74-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cc74-114">Requirement</span></span> | <span data-ttu-id="2cc74-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2cc74-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc74-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cc74-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2cc74-117">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2cc74-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2cc74-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cc74-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2cc74-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2cc74-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2cc74-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cc74-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cc74-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cc74-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2cc74-122">IDL</span><span class="sxs-lookup"><span data-stu-id="2cc74-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2cc74-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2cc74-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2cc74-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2cc74-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cc74-125"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="2cc74-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
