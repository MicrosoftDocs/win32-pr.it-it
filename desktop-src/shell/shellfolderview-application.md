---
description: "Proprietà ShellFolderView.Application: contiene l'oggetto Application dell'oggetto."
ms.assetid: 305766b1-a19f-4743-a9e3-6837b3f8ffe0
title: Proprietà ShellFolderView.Application (Shldisp.h)
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
ms.openlocfilehash: 95ef542f91235b3b068e1b1b54768b4dd453d9b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083469"
---
# <a name="shellfolderviewapplication-property"></a><span data-ttu-id="0f449-103">ShellFolderView.Application - proprietà</span><span class="sxs-lookup"><span data-stu-id="0f449-103">ShellFolderView.Application property</span></span>

<span data-ttu-id="0f449-104">Contiene l'oggetto Application dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0f449-104">Contains the object's Application object.</span></span>

<span data-ttu-id="0f449-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0f449-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f449-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f449-106">Syntax</span></span>


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a><span data-ttu-id="0f449-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0f449-107">Property value</span></span>

<span data-ttu-id="0f449-108">Variabile di tipo [**IDispatch che**](/windows/win32/api/oaidl/nn-oaidl-idispatch) riceve l'oggetto Application.</span><span class="sxs-lookup"><span data-stu-id="0f449-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f449-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f449-109">Remarks</span></span>

<span data-ttu-id="0f449-110">La **proprietà Application** restituisce l'oggetto di automazione supportato dall'applicazione che contiene il controllo WebBrowser, se tale oggetto è accessibile.</span><span class="sxs-lookup"><span data-stu-id="0f449-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="0f449-111">In caso contrario, questa proprietà restituisce l'oggetto di automazione del controllo WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="0f449-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="0f449-112">Usare questa proprietà con i **comandi Set** e **CreateObject** o con il **comando GetObject** per creare e modificare un'istanza dell'applicazione Internet Explorer Windows.</span><span class="sxs-lookup"><span data-stu-id="0f449-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f449-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f449-113">Requirements</span></span>



| <span data-ttu-id="0f449-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f449-114">Requirement</span></span> | <span data-ttu-id="0f449-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0f449-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f449-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f449-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0f449-117">Windows 2000 Professional, solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0f449-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0f449-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f449-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0f449-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f449-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0f449-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f449-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f449-121"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="0f449-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0f449-122">Idl</span><span class="sxs-lookup"><span data-stu-id="0f449-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f449-123"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f449-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0f449-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0f449-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f449-125"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="0f449-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
