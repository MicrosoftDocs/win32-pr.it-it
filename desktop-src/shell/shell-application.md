---
description: Contiene l'oggetto applicazione dell'oggetto.
ms.assetid: 5335f4dd-ca80-49c8-8953-e32a6e6308e0
title: Proprietà Shell. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a9f9bd7fa28d2b277adfd8038c10c97efe16f51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885333"
---
# <a name="shellapplication-property"></a><span data-ttu-id="49c61-103">Proprietà Shell. Application</span><span class="sxs-lookup"><span data-stu-id="49c61-103">Shell.Application property</span></span>

<span data-ttu-id="49c61-104">Contiene l'oggetto applicazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="49c61-104">Contains the object's Application object.</span></span>

<span data-ttu-id="49c61-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="49c61-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="49c61-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49c61-106">Syntax</span></span>


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="49c61-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="49c61-107">Property value</span></span>

<span data-ttu-id="49c61-108">Variabile di tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto applicazione.</span><span class="sxs-lookup"><span data-stu-id="49c61-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="49c61-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="49c61-109">Remarks</span></span>

<span data-ttu-id="49c61-110">La proprietà dell' **applicazione** restituisce l'oggetto di automazione supportato dall'applicazione che contiene il controllo WebBrowser, se tale oggetto è accessibile.</span><span class="sxs-lookup"><span data-stu-id="49c61-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="49c61-111">In caso contrario, questa proprietà restituisce l'oggetto di automazione del controllo WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="49c61-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="49c61-112">Utilizzare questa proprietà con i comandi **set** e **CreateObject** oppure con il comando **GetObject** per creare e modificare un'istanza dell'applicazione Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="49c61-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="49c61-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49c61-113">Requirements</span></span>



| <span data-ttu-id="49c61-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="49c61-114">Requirement</span></span> | <span data-ttu-id="49c61-115">Valore</span><span class="sxs-lookup"><span data-stu-id="49c61-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49c61-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49c61-116">Minimum supported client</span></span><br/> | <span data-ttu-id="49c61-117">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="49c61-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="49c61-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49c61-118">Minimum supported server</span></span><br/> | <span data-ttu-id="49c61-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49c61-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="49c61-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49c61-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="49c61-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="49c61-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="49c61-122">IDL</span><span class="sxs-lookup"><span data-stu-id="49c61-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49c61-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="49c61-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="49c61-124">DLL</span><span class="sxs-lookup"><span data-stu-id="49c61-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49c61-125"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="49c61-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
