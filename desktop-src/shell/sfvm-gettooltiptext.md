---
description: "Consente all'oggetto callback di specificare una stringa di testo della descrizione comando per le voci di menu o i pulsanti della barra degli strumenti. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: Messaggio SFVM_GETTOOLTIPTEXT (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffea70f6051ec435e14640ac70d2e9617b11305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968519"
---
# <a name="sfvm_gettooltiptext-message"></a><span data-ttu-id="6f822-104">\_Messaggio SFVM GETTOOLTIPTEXT</span><span class="sxs-lookup"><span data-stu-id="6f822-104">SFVM\_GETTOOLTIPTEXT message</span></span>

<span data-ttu-id="6f822-105">Consente all'oggetto callback di specificare una stringa di testo della descrizione comando per le voci di menu o i pulsanti della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="6f822-105">Allows the callback object to specify a tooltip text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="6f822-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="6f822-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="6f822-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6f822-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f822-108">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="6f822-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f822-109">La parola di basso livello di questo parametro include l'ID del comando.</span><span class="sxs-lookup"><span data-stu-id="6f822-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="6f822-110">La parola più ordinata include il numero di caratteri nel buffer di *pszText* .</span><span class="sxs-lookup"><span data-stu-id="6f822-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6f822-111">*pszText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6f822-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f822-112">Stringa con terminazione null contenente il testo della guida.</span><span class="sxs-lookup"><span data-stu-id="6f822-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f822-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f822-113">Requirements</span></span>



| <span data-ttu-id="6f822-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f822-114">Requirement</span></span> | <span data-ttu-id="6f822-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6f822-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6f822-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f822-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6f822-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f822-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6f822-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6f822-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6f822-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6f822-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6f822-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f822-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f822-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f822-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
