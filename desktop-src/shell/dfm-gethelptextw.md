---
description: "DFM_GETHELPTEXTW messaggio: consente all'oggetto callback di specificare una stringa di testo della Guida."
title: DFM_GETHELPTEXTW messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6271b150bead5be4715259c68711ee67417f6395
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097039"
---
# <a name="dfm_gethelptextw-message"></a><span data-ttu-id="14207-103">Messaggio DFM \_ GETHELPTEXTW</span><span class="sxs-lookup"><span data-stu-id="14207-103">DFM\_GETHELPTEXTW message</span></span>

<span data-ttu-id="14207-104">Consente all'oggetto callback di specificare una stringa di testo della Guida.</span><span class="sxs-lookup"><span data-stu-id="14207-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="14207-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="14207-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14207-106">*idCmd \_ cchMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14207-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14207-107">La parola più bassa di questo parametro contiene l'ID del comando.</span><span class="sxs-lookup"><span data-stu-id="14207-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="14207-108">La parola più alta contiene il numero di caratteri nel buffer *pszText.*</span><span class="sxs-lookup"><span data-stu-id="14207-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="14207-109">*pszText* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="14207-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14207-110">Stringa Unicode con terminazione Null contenente il testo della Guida.</span><span class="sxs-lookup"><span data-stu-id="14207-110">A null-terminated Unicode string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14207-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="14207-111">Remarks</span></span>

<span data-ttu-id="14207-112">Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda di come viene costruito l'oggetto del menu di scelta rapida predefinito.</span><span class="sxs-lookup"><span data-stu-id="14207-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="14207-113">Per la costruzione sono disponibili due API, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="14207-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="14207-114">[**DFM \_ INVOKECOMMANDEX è**](dfm-invokecommandex.md) una versione estesa di questo messaggio e fornisce altre informazioni al callback.</span><span class="sxs-lookup"><span data-stu-id="14207-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="14207-115">Usare **DFM \_ INVOKECOMMANDEX** se le informazioni aggiuntive fornite da tale interfaccia sono necessarie nell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="14207-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="14207-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14207-116">Requirements</span></span>



| <span data-ttu-id="14207-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="14207-117">Requirement</span></span> | <span data-ttu-id="14207-118">Valore</span><span class="sxs-lookup"><span data-stu-id="14207-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="14207-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14207-119">Minimum supported client</span></span><br/> | <span data-ttu-id="14207-120">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="14207-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="14207-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14207-121">Minimum supported server</span></span><br/> | <span data-ttu-id="14207-122">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="14207-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="14207-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14207-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="14207-124"><dt>Shlobj.h</dt></span><span class="sxs-lookup"><span data-stu-id="14207-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="14207-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="14207-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="14207-126">**DFM \_ GETHELPTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="14207-126">**DFM\_GETHELPTEXTW** (Unicode)</span></span><br/>                                          |



 

 




