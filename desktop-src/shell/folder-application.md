---
description: Contiene l'oggetto applicazione della cartella.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Proprietà Folder. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484037"
---
# <a name="folderapplication-property"></a><span data-ttu-id="8d437-103">Proprietà Folder. Application</span><span class="sxs-lookup"><span data-stu-id="8d437-103">Folder.Application property</span></span>

<span data-ttu-id="8d437-104">Contiene l'oggetto applicazione della cartella.</span><span class="sxs-lookup"><span data-stu-id="8d437-104">Contains the folder's Application object.</span></span>

<span data-ttu-id="8d437-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="8d437-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d437-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d437-106">Syntax</span></span>


```JScript
Application = Folder.Application
```



## <a name="property-value"></a><span data-ttu-id="8d437-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8d437-107">Property value</span></span>

<span data-ttu-id="8d437-108">Riferimento all'oggetto applicazione.</span><span class="sxs-lookup"><span data-stu-id="8d437-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d437-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d437-109">Remarks</span></span>

<span data-ttu-id="8d437-110">La proprietà dell' **applicazione** restituisce l'oggetto di automazione supportato dall'applicazione che contiene il controllo WebBrowser, se tale oggetto è accessibile.</span><span class="sxs-lookup"><span data-stu-id="8d437-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="8d437-111">In caso contrario, questa proprietà restituisce l'oggetto di automazione del controllo WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="8d437-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="8d437-112">Utilizzare questa proprietà con i comandi **set** e **CreateObject** oppure con il comando **GetObject** per creare e modificare un'istanza dell'applicazione Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8d437-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Internet Explorer application.</span></span>

> [!Note]  
> <span data-ttu-id="8d437-113">Non tutti i metodi sono implementati per tutte le cartelle.</span><span class="sxs-lookup"><span data-stu-id="8d437-113">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="8d437-114">Il metodo [**ParseName**](folder-parsename.md) , ad esempio, non è implementato per la cartella del pannello di controllo ( \_ controlli CSIDL).</span><span class="sxs-lookup"><span data-stu-id="8d437-114">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="8d437-115">Se si tenta di chiamare un metodo non implementato, viene generato un errore 0x800A01BD (decimale 445).</span><span class="sxs-lookup"><span data-stu-id="8d437-115">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8d437-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d437-116">Requirements</span></span>



| <span data-ttu-id="8d437-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d437-117">Requirement</span></span> | <span data-ttu-id="8d437-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8d437-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d437-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d437-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d437-120">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8d437-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="8d437-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d437-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d437-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8d437-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8d437-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d437-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d437-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d437-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8d437-125">IDL</span><span class="sxs-lookup"><span data-stu-id="8d437-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8d437-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8d437-126"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




