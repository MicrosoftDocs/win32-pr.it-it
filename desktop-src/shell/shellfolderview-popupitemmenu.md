---
description: "Metodo ShellFolderView.PopupItemMenu: crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata."
title: Metodo ShellFolderView.PopupItemMenu (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: cb862ba159f55d3ab82495ddeb32a87f3ce1901b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083389"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="a0552-103">Metodo ShellFolderView.PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="a0552-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="a0552-104">Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.</span><span class="sxs-lookup"><span data-stu-id="a0552-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0552-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0552-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="a0552-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0552-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0552-107">*vItem* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a0552-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0552-108">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="a0552-108">Type: **Variant**</span></span>

<span data-ttu-id="a0552-109">Oggetto [**FolderItem**](folderitem.md) per il quale verrà creato il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="a0552-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="a0552-110">*vx* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a0552-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0552-111">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="a0552-111">Type: **Variant**</span></span>

<span data-ttu-id="a0552-112">Posizione orizzontale del menu, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a0552-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a0552-113">*vy* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a0552-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a0552-114">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="a0552-114">Type: **Variant**</span></span>

<span data-ttu-id="a0552-115">Posizione verticale del menu, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a0552-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0552-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0552-116">Return value</span></span>

<span data-ttu-id="a0552-117">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="a0552-117">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="a0552-118">Stringa **che** riceve la stringa di comando.</span><span class="sxs-lookup"><span data-stu-id="a0552-118">The **String** that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0552-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0552-119">Requirements</span></span>



| <span data-ttu-id="a0552-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0552-120">Requirement</span></span> | <span data-ttu-id="a0552-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a0552-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0552-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0552-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a0552-123">Solo app desktop windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="a0552-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a0552-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0552-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a0552-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a0552-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0552-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0552-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0552-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="a0552-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="a0552-128">Idl</span><span class="sxs-lookup"><span data-stu-id="a0552-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0552-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0552-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="a0552-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a0552-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0552-131"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a0552-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
