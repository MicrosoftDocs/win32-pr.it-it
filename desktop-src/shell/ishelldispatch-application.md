---
description: Contiene un oggetto che rappresenta un'applicazione.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: Proprietà IShellDispatch. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5adeb5663220309310c7cccb323be877de909516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527355"
---
# <a name="ishelldispatchapplication-property"></a><span data-ttu-id="3abe5-103">Proprietà IShellDispatch. Application</span><span class="sxs-lookup"><span data-stu-id="3abe5-103">IShellDispatch.Application property</span></span>

<span data-ttu-id="3abe5-104">Contiene un oggetto che rappresenta un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3abe5-104">Contains an object that represents an application.</span></span>

<span data-ttu-id="3abe5-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="3abe5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3abe5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3abe5-106">Syntax</span></span>


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="3abe5-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3abe5-107">Property value</span></span>

<span data-ttu-id="3abe5-108">Variabile di tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) che riceve l'oggetto applicazione.</span><span class="sxs-lookup"><span data-stu-id="3abe5-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3abe5-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3abe5-109">Remarks</span></span>

<span data-ttu-id="3abe5-110">Questa proprietà viene implementata e accessibile tramite la proprietà [**Shell. EjectPC**](shell-ejectpc.md) .</span><span class="sxs-lookup"><span data-stu-id="3abe5-110">This property is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) property.</span></span>

<span data-ttu-id="3abe5-111">La proprietà dell' **applicazione** restituisce l'oggetto di automazione supportato dall'applicazione che contiene il controllo WebBrowser, se tale oggetto è accessibile.</span><span class="sxs-lookup"><span data-stu-id="3abe5-111">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="3abe5-112">In caso contrario, questa proprietà restituisce l'oggetto di automazione del controllo WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="3abe5-112">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="3abe5-113">Utilizzare questa proprietà con i comandi **set** e **CreateObject** oppure con il comando **GetObject** per creare e modificare un'istanza dell'applicazione Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3abe5-113">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="3abe5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3abe5-114">Requirements</span></span>



| <span data-ttu-id="3abe5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3abe5-115">Requirement</span></span> | <span data-ttu-id="3abe5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3abe5-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3abe5-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3abe5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3abe5-118">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3abe5-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3abe5-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3abe5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3abe5-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3abe5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3abe5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3abe5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3abe5-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3abe5-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3abe5-123">IDL</span><span class="sxs-lookup"><span data-stu-id="3abe5-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3abe5-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3abe5-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3abe5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3abe5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3abe5-126"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="3abe5-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
