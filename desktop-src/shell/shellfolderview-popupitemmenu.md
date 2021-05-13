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
ms.openlocfilehash: 7a2feda23d6e1759e1c0be27805fefbb6b592df7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840752"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="f51e5-103">Metodo ShellFolderView.PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="f51e5-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="f51e5-104">Crea un menu di scelta rapida per l'elemento specificato e restituisce la stringa di comando selezionata.</span><span class="sxs-lookup"><span data-stu-id="f51e5-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f51e5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f51e5-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="f51e5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f51e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f51e5-107">*vItem* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f51e5-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f51e5-108">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="f51e5-108">Type: **Variant**</span></span>

<span data-ttu-id="f51e5-109">Oggetto [**FolderItem**](folderitem.md) per il quale verrà creato il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="f51e5-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="f51e5-110">*vx* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f51e5-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f51e5-111">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="f51e5-111">Type: **Variant**</span></span>

<span data-ttu-id="f51e5-112">Posizione orizzontale del menu, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="f51e5-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="f51e5-113">*vy* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="f51e5-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f51e5-114">Tipo: **Variante**</span><span class="sxs-lookup"><span data-stu-id="f51e5-114">Type: **Variant**</span></span>

<span data-ttu-id="f51e5-115">Posizione verticale del menu, in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="f51e5-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f51e5-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f51e5-116">Return value</span></span>

<span data-ttu-id="f51e5-117">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="f51e5-117">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="f51e5-118">Stringa **che** riceve la stringa di comando.</span><span class="sxs-lookup"><span data-stu-id="f51e5-118">The **String** that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="f51e5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f51e5-119">Requirements</span></span>



| <span data-ttu-id="f51e5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f51e5-120">Requirement</span></span> | <span data-ttu-id="f51e5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f51e5-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51e5-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f51e5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f51e5-123">Solo app desktop di Windows 2000 Professional e Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f51e5-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f51e5-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f51e5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f51e5-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f51e5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f51e5-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f51e5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f51e5-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="f51e5-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f51e5-128">Idl</span><span class="sxs-lookup"><span data-stu-id="f51e5-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f51e5-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="f51e5-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f51e5-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f51e5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f51e5-131"><dt>Shell32.dll (versione 4.71 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="f51e5-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
