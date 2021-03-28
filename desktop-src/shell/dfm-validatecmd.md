---
description: Inviato per verificare l'esistenza di un comando di menu.
title: Messaggio DFM_VALIDATECMD (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5aa171f19d4d08c3ba3088676a4ae5364f0826f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128454"
---
# <a name="dfm_validatecmd-message"></a><span data-ttu-id="e54a1-103">\_Messaggio DFM VALIDATECMD</span><span class="sxs-lookup"><span data-stu-id="e54a1-103">DFM\_VALIDATECMD message</span></span>

<span data-ttu-id="e54a1-104">Inviato per verificare l'esistenza di un comando di menu.</span><span class="sxs-lookup"><span data-stu-id="e54a1-104">Sent to verify the existence of a menu command.</span></span>


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a><span data-ttu-id="e54a1-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="e54a1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e54a1-106">*idCmd*</span><span class="sxs-lookup"><span data-stu-id="e54a1-106">*idCmd*</span></span> 
</dt> <dd><span data-ttu-id="e54a1-107">Offset dell'identificatore del comando di menu.</span><span class="sxs-lookup"><span data-stu-id="e54a1-107">The menu command identifier offset.</span></span></dd> <dt>

<span data-ttu-id="e54a1-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e54a1-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e54a1-109">Non usato.</span><span class="sxs-lookup"><span data-stu-id="e54a1-109">Not used.</span></span> <span data-ttu-id="e54a1-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e54a1-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e54a1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e54a1-111">Return value</span></span>

<span data-ttu-id="e54a1-112">Restituisce \_ OK se il comando esiste oppure S \_ false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e54a1-112">Returns S\_OK if the command exists, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e54a1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e54a1-113">Remarks</span></span>

<span data-ttu-id="e54a1-114">Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda del modo in cui viene costruito l'oggetto menu di scelta rapida predefinito.</span><span class="sxs-lookup"><span data-stu-id="e54a1-114">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="e54a1-115">Sono disponibili due API per la relativa costruzione, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="e54a1-115">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="e54a1-116">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback.</span><span class="sxs-lookup"><span data-stu-id="e54a1-116">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="e54a1-117">Usare **DFM \_ INVOKECOMMANDEX** se nell'implementazione sono necessarie informazioni aggiuntive fornite da tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e54a1-117">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="e54a1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e54a1-118">Requirements</span></span>



| <span data-ttu-id="e54a1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e54a1-119">Requirement</span></span> | <span data-ttu-id="e54a1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e54a1-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e54a1-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e54a1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e54a1-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e54a1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e54a1-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e54a1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e54a1-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e54a1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e54a1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e54a1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e54a1-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="e54a1-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




