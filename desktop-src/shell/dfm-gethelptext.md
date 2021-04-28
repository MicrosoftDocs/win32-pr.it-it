---
description: "DFM_GETHELPTEXT messaggio: consente all'oggetto callback di specificare una stringa di testo della Guida."
title: DFM_GETHELPTEXT messaggio (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2428fe6696ff5949a0b25487437c8f3408b95f65
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097069"
---
# <a name="dfm_gethelptext-message"></a><span data-ttu-id="00ea7-103">Messaggio DFM \_ GETHELPTEXT</span><span class="sxs-lookup"><span data-stu-id="00ea7-103">DFM\_GETHELPTEXT message</span></span>

<span data-ttu-id="00ea7-104">Consente all'oggetto callback di specificare una stringa di testo della Guida.</span><span class="sxs-lookup"><span data-stu-id="00ea7-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="00ea7-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="00ea7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ea7-106">*idCmd \_ cchMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00ea7-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00ea7-107">La parola più bassa di questo parametro contiene l'ID del comando.</span><span class="sxs-lookup"><span data-stu-id="00ea7-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="00ea7-108">La parola più alta contiene il numero di caratteri nel buffer *pszText.*</span><span class="sxs-lookup"><span data-stu-id="00ea7-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="00ea7-109">*pszText* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="00ea7-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00ea7-110">Stringa ANSI con terminazione Null contenente il testo della Guida.</span><span class="sxs-lookup"><span data-stu-id="00ea7-110">A null-terminated ANSI string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00ea7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="00ea7-111">Remarks</span></span>

<span data-ttu-id="00ea7-112">Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda di come viene costruito l'oggetto del menu di scelta rapida predefinito.</span><span class="sxs-lookup"><span data-stu-id="00ea7-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="00ea7-113">Per la costruzione sono disponibili due API, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="00ea7-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="00ea7-114">[**DFM \_ INVOKECOMMANDEX è**](dfm-invokecommandex.md) una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback.</span><span class="sxs-lookup"><span data-stu-id="00ea7-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="00ea7-115">Usare **DFM \_ INVOKECOMMANDEX** se le informazioni aggiuntive fornite da tale interfaccia sono necessarie nell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="00ea7-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="00ea7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00ea7-116">Requirements</span></span>



| <span data-ttu-id="00ea7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="00ea7-117">Requirement</span></span> | <span data-ttu-id="00ea7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="00ea7-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="00ea7-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00ea7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="00ea7-120">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="00ea7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="00ea7-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00ea7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="00ea7-122">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="00ea7-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="00ea7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00ea7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="00ea7-124"><dt>Shlobj.h</dt></span><span class="sxs-lookup"><span data-stu-id="00ea7-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="00ea7-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="00ea7-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="00ea7-126">**DFM \_ GETHELPTEXT** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="00ea7-126">**DFM\_GETHELPTEXT** (ANSI)</span></span><br/>                                              |



 

 




