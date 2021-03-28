---
description: Inviato dall'implementazione del menu di scelta rapida predefinito per assegnare un nome a un comando di menu.
title: Messaggio DFM_MAPCOMMANDNAME (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 312817e5c530078b906af63e4e8c3d00595d3a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525357"
---
# <a name="dfm_mapcommandname-message"></a><span data-ttu-id="99417-103">\_Messaggio DFM MAPCOMMANDNAME</span><span class="sxs-lookup"><span data-stu-id="99417-103">DFM\_MAPCOMMANDNAME message</span></span>

<span data-ttu-id="99417-104">Inviato dall'implementazione del menu di scelta rapida predefinito per assegnare un nome a un comando di menu.</span><span class="sxs-lookup"><span data-stu-id="99417-104">Sent by the default context menu implementation to assign a name to a menu command.</span></span>


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a><span data-ttu-id="99417-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="99417-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99417-106">*defaultID* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="99417-106">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="99417-107">Puntatore all'ID del comando di menu selezionato.</span><span class="sxs-lookup"><span data-stu-id="99417-107">A pointer to the ID of the selected menu command.</span></span>

</dd> <dt>

<span data-ttu-id="99417-108">*pszCommandName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="99417-108">*pszCommandName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99417-109">Puntatore a una stringa Unicode che contiene il nome del comando.</span><span class="sxs-lookup"><span data-stu-id="99417-109">A pointer to a Unicode string containing the name of the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99417-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="99417-110">Remarks</span></span>

<span data-ttu-id="99417-111">Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di implementazione dell'oggetto menu di scelta rapida predefinito.</span><span class="sxs-lookup"><span data-stu-id="99417-111">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="99417-112">Sono disponibili due API per la relativa implementazione, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="99417-112">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="99417-113">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback.</span><span class="sxs-lookup"><span data-stu-id="99417-113">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="99417-114">Usare **DFM \_ INVOKECOMMANDEX** se nell'implementazione sono necessarie informazioni aggiuntive fornite da tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="99417-114">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="99417-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99417-115">Requirements</span></span>



| <span data-ttu-id="99417-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="99417-116">Requirement</span></span> | <span data-ttu-id="99417-117">Valore</span><span class="sxs-lookup"><span data-stu-id="99417-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="99417-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99417-118">Minimum supported client</span></span><br/> | <span data-ttu-id="99417-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99417-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="99417-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99417-120">Minimum supported server</span></span><br/> | <span data-ttu-id="99417-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99417-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="99417-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99417-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="99417-123"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="99417-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




