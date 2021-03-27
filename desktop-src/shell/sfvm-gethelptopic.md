---
description: "Consente all'oggetto callback di specificare un file della Guida HTML e un argomento al suo interno. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_GETHELPTOPIC (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883422"
---
# <a name="sfvm_gethelptopic-message"></a><span data-ttu-id="dd45b-104">\_Messaggio SFVM GETHELPTOPIC</span><span class="sxs-lookup"><span data-stu-id="dd45b-104">SFVM\_GETHELPTOPIC message</span></span>

<span data-ttu-id="dd45b-105">Consente all'oggetto callback di specificare un file della Guida HTML e un argomento al suo interno.</span><span class="sxs-lookup"><span data-stu-id="dd45b-105">Allows the callback object to specify an HTML Help file and a topic within it.</span></span> <span data-ttu-id="dd45b-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="dd45b-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a><span data-ttu-id="dd45b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd45b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd45b-108">*PhtD* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dd45b-108">*phtd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd45b-109">Indirizzo di una struttura [**di \_ \_ dati SFVM HELPTOPIC**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) che specifica il file della Guida HTML e l'argomento.</span><span class="sxs-lookup"><span data-stu-id="dd45b-109">The address of a [**SFVM\_HELPTOPIC\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) structure that specifies the HTML Help file and topic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd45b-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd45b-110">Requirements</span></span>



| <span data-ttu-id="dd45b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd45b-111">Requirement</span></span> | <span data-ttu-id="dd45b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="dd45b-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dd45b-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd45b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="dd45b-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd45b-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dd45b-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd45b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="dd45b-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dd45b-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dd45b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd45b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd45b-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd45b-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
