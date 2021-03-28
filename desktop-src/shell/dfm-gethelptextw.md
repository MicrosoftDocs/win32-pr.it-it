---
description: Consente all'oggetto callback di specificare una stringa di testo della guida.
title: Messaggio DFM_GETHELPTEXTW (Shlobj. h)
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
ms.openlocfilehash: 7ac1e41046b2d757df96e9acf5722710ae832bf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977295"
---
# <a name="dfm_gethelptextw-message"></a><span data-ttu-id="067db-103">\_Messaggio DFM GETHELPTEXTW</span><span class="sxs-lookup"><span data-stu-id="067db-103">DFM\_GETHELPTEXTW message</span></span>

<span data-ttu-id="067db-104">Consente all'oggetto callback di specificare una stringa di testo della guida.</span><span class="sxs-lookup"><span data-stu-id="067db-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="067db-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="067db-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="067db-106">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="067db-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="067db-107">La parola di basso livello di questo parametro include l'ID del comando.</span><span class="sxs-lookup"><span data-stu-id="067db-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="067db-108">La parola più ordinata include il numero di caratteri nel buffer di *pszText* .</span><span class="sxs-lookup"><span data-stu-id="067db-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="067db-109">*pszText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="067db-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="067db-110">Stringa Unicode con terminazione null contenente il testo della guida.</span><span class="sxs-lookup"><span data-stu-id="067db-110">A null-terminated Unicode string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="067db-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="067db-111">Remarks</span></span>

<span data-ttu-id="067db-112">Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda del modo in cui viene costruito l'oggetto menu di scelta rapida predefinito.</span><span class="sxs-lookup"><span data-stu-id="067db-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="067db-113">Sono disponibili due API per la relativa costruzione, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="067db-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="067db-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback.</span><span class="sxs-lookup"><span data-stu-id="067db-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="067db-115">Usare **DFM \_ INVOKECOMMANDEX** se nell'implementazione sono necessarie informazioni aggiuntive fornite da tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="067db-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="067db-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="067db-116">Requirements</span></span>



| <span data-ttu-id="067db-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="067db-117">Requirement</span></span> | <span data-ttu-id="067db-118">Valore</span><span class="sxs-lookup"><span data-stu-id="067db-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="067db-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="067db-119">Minimum supported client</span></span><br/> | <span data-ttu-id="067db-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="067db-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="067db-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="067db-121">Minimum supported server</span></span><br/> | <span data-ttu-id="067db-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="067db-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="067db-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="067db-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="067db-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="067db-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="067db-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="067db-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="067db-126">**DFM \_ GETHELPTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="067db-126">**DFM\_GETHELPTEXTW** (Unicode)</span></span><br/>                                          |



 

 




