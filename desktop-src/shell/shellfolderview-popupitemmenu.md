---
description: Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.
title: Metodo ShellFolderView. PopupItemMenu (shldisp. h)
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
ms.openlocfilehash: 513f654442361da840cb02089810c814275c5867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233196"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="7697e-103">ShellFolderView. PopupItemMenu, metodo</span><span class="sxs-lookup"><span data-stu-id="7697e-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="7697e-104">Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.</span><span class="sxs-lookup"><span data-stu-id="7697e-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="7697e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7697e-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="7697e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7697e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7697e-107">*vite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7697e-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7697e-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="7697e-108">Type: **Variant**</span></span>

<span data-ttu-id="7697e-109">Oggetto [**FolderItem**](folderitem.md) per il quale verrà creato il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="7697e-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="7697e-110">*VX* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7697e-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7697e-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="7697e-111">Type: **Variant**</span></span>

<span data-ttu-id="7697e-112">Posizione orizzontale del menu, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="7697e-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="7697e-113">stato del  \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7697e-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7697e-114">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="7697e-114">Type: **Variant**</span></span>

<span data-ttu-id="7697e-115">Posizione verticale del menu, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="7697e-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7697e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7697e-116">Return value</span></span>

<span data-ttu-id="7697e-117">Tipo: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="7697e-117">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="7697e-118">_ *Stringa*\* che riceve la stringa di comando.</span><span class="sxs-lookup"><span data-stu-id="7697e-118">The _ *String*\* that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="7697e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7697e-119">Requirements</span></span>



| <span data-ttu-id="7697e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7697e-120">Requirement</span></span> | <span data-ttu-id="7697e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7697e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7697e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7697e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7697e-123">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7697e-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7697e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7697e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7697e-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7697e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7697e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7697e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7697e-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7697e-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7697e-128">IDL</span><span class="sxs-lookup"><span data-stu-id="7697e-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7697e-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7697e-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7697e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7697e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7697e-131"><dt>Shell32.dll (versione 4,71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7697e-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
