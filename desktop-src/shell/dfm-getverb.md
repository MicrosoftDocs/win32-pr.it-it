---
description: Inviato dall'implementazione del menu di scelta rapida predefinito per ottenere il verbo per l'ID del comando specificato nel menu di scelta rapida.
title: Messaggio DFM_GETVERB (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd12a38e-4d50-43ad-9d1f-8fefa90b44f9
api_name:
- DFM_GETVERB
- DFM_GETVERBA
- DFM_GETVERBW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbb1b2fb54aa2b0e4b66cf8fc559c56eb279504d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225924"
---
# <a name="dfm_getverb-message"></a><span data-ttu-id="4d675-103">\_Messaggio GETVERB DFM</span><span class="sxs-lookup"><span data-stu-id="4d675-103">DFM\_GETVERB message</span></span>

<span data-ttu-id="4d675-104">Inviato dall'implementazione del menu di scelta rapida predefinito per ottenere il verbo per l'ID del comando specificato nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="4d675-104">Sent by the default context menu implementation to get the verb for the given command ID in the context menu.</span></span>


```C++

                DFM_GETVERB 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="4d675-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d675-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d675-106">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="4d675-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d675-107">La parola di basso livello di questo parametro include l'ID del comando.</span><span class="sxs-lookup"><span data-stu-id="4d675-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="4d675-108">La parola più ordinata include il numero di caratteri nel buffer di *pszText* .</span><span class="sxs-lookup"><span data-stu-id="4d675-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4d675-109">*pszText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4d675-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d675-110">Puntatore a una stringa con terminazione null che contiene il testo del verbo.</span><span class="sxs-lookup"><span data-stu-id="4d675-110">A pointer to a null-terminated string that contains the verb text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d675-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d675-111">Remarks</span></span>

<span data-ttu-id="4d675-112">Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda del modo in cui viene costruito l'oggetto menu di scelta rapida predefinito.</span><span class="sxs-lookup"><span data-stu-id="4d675-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="4d675-113">Sono disponibili due API per la relativa costruzione, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="4d675-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="4d675-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback.</span><span class="sxs-lookup"><span data-stu-id="4d675-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="4d675-115">Usare **DFM \_ INVOKECOMMANDEX** se nell'implementazione sono necessarie informazioni aggiuntive fornite da tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="4d675-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d675-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d675-116">Requirements</span></span>



| <span data-ttu-id="4d675-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d675-117">Requirement</span></span> | <span data-ttu-id="4d675-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4d675-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4d675-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d675-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d675-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d675-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4d675-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d675-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d675-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4d675-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4d675-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d675-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d675-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d675-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="4d675-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4d675-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4d675-126">**DFM \_ GETVERBW** (Unicode) e **DFM \_ getverba** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4d675-126">**DFM\_GETVERBW** (Unicode) and **DFM\_GETVERBA** (ANSI)</span></span><br/>                 |



 

 




