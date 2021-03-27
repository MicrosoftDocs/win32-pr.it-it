---
description: "Consente all'oggetto callback di specificare una stringa di testo della Guida per le voci di menu o i pulsanti della barra degli strumenti. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_GETHELPTEXT (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b33bd99c2dd1e6d1013da9015a5ff70bc111c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757841"
---
# <a name="sfvm_gethelptext-message"></a><span data-ttu-id="79d8c-104">\_Messaggio SFVM GETHELPTEXT</span><span class="sxs-lookup"><span data-stu-id="79d8c-104">SFVM\_GETHELPTEXT message</span></span>

<span data-ttu-id="79d8c-105">Consente all'oggetto callback di specificare una stringa di testo della Guida per le voci di menu o i pulsanti della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="79d8c-105">Allows the callback object to specify a help text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="79d8c-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="79d8c-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="79d8c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="79d8c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79d8c-108">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="79d8c-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79d8c-109">La parola di basso livello di questo parametro include l'ID del comando.</span><span class="sxs-lookup"><span data-stu-id="79d8c-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="79d8c-110">La parola più ordinata include il numero di caratteri nel buffer di *pszText* .</span><span class="sxs-lookup"><span data-stu-id="79d8c-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="79d8c-111">*pszText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="79d8c-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79d8c-112">Stringa con terminazione null contenente il testo della guida.</span><span class="sxs-lookup"><span data-stu-id="79d8c-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79d8c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79d8c-113">Requirements</span></span>



| <span data-ttu-id="79d8c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="79d8c-114">Requirement</span></span> | <span data-ttu-id="79d8c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="79d8c-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="79d8c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79d8c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="79d8c-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="79d8c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="79d8c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="79d8c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="79d8c-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="79d8c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="79d8c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79d8c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="79d8c-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="79d8c-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
