---
description: Imposta la posizione di un elemento nella visualizzazione della shell. Utilizzato dal \_ messaggio SHShellFolderView.
title: Messaggio SFVM_SETITEMPOS (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b89f2d62-095b-4cad-a47e-2d41e122cb3e
api_name:
- SFVM_SETITEMPOS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 450aeabee6e5edeba466e4a5fe64725c13eea32b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233886"
---
# <a name="sfvm_setitempos-message"></a><span data-ttu-id="af138-104">\_Messaggio SFVM SETITEMPOS</span><span class="sxs-lookup"><span data-stu-id="af138-104">SFVM\_SETITEMPOS message</span></span>

<span data-ttu-id="af138-105">Imposta la posizione di un elemento nella visualizzazione della shell.</span><span class="sxs-lookup"><span data-stu-id="af138-105">Sets the position of an item in the Shell view.</span></span> <span data-ttu-id="af138-106">Utilizzato dal [**\_ messaggio SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="af138-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_SETITEMPOS 

    lParam = (LPSFV_SETITEMPOS)&sip;

            
```



## <a name="parameters"></a><span data-ttu-id="af138-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="af138-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af138-108">*SIP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af138-108">*sip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af138-109">Puntatore a una struttura [**\_ SETITEMPOS SFV**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) .</span><span class="sxs-lookup"><span data-stu-id="af138-109">A pointer to an [**SFV\_SETITEMPOS**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af138-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af138-110">Requirements</span></span>



| <span data-ttu-id="af138-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="af138-111">Requirement</span></span> | <span data-ttu-id="af138-112">Valore</span><span class="sxs-lookup"><span data-stu-id="af138-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="af138-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af138-113">Minimum supported client</span></span><br/> | <span data-ttu-id="af138-114">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="af138-114">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="af138-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af138-115">Minimum supported server</span></span><br/> | <span data-ttu-id="af138-116">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af138-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="af138-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af138-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="af138-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="af138-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




