---
description: SFVM \_ QUERYFSNOTIFY può essere modificato o non disponibile.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: Messaggio SFVM_QUERYFSNOTIFY (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4416bda249e3ec0f2a0c0f2d45ac353961e180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234090"
---
# <a name="sfvm_queryfsnotify-message"></a><span data-ttu-id="01c83-103">\_Messaggio SFVM QUERYFSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="01c83-103">SFVM\_QUERYFSNOTIFY message</span></span>

<span data-ttu-id="01c83-104">\[**SFVM \_ QUERYFSNOTIFY** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="01c83-104">\[**SFVM\_QUERYFSNOTIFY** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="01c83-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="01c83-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="01c83-106">Consente all'oggetto callback di registrare una cartella in modo che le modifiche apportate alla visualizzazione della cartella generino notifiche.</span><span class="sxs-lookup"><span data-stu-id="01c83-106">Allows the callback object to register a folder so that changes to that folder's view will generate notifications.</span></span> <span data-ttu-id="01c83-107">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="01c83-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a><span data-ttu-id="01c83-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="01c83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01c83-109">*shcne* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="01c83-109">*shcne* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="01c83-110">Struttura che deve contenere il PIDL dell'elemento da controllare per gli eventi e indica se devono essere controllate anche le sottocartelle di tale elemento.</span><span class="sxs-lookup"><span data-stu-id="01c83-110">A structure to hold the PIDL of the item to watch for events and an indication whether subfolders of that item should also be watched.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01c83-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01c83-111">Requirements</span></span>



| <span data-ttu-id="01c83-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="01c83-112">Requirement</span></span> | <span data-ttu-id="01c83-113">Valore</span><span class="sxs-lookup"><span data-stu-id="01c83-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="01c83-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01c83-114">Minimum supported client</span></span><br/> | <span data-ttu-id="01c83-115">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="01c83-115">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="01c83-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01c83-116">Minimum supported server</span></span><br/> | <span data-ttu-id="01c83-117">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="01c83-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="01c83-118">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="01c83-118">End of client support</span></span><br/>    | <span data-ttu-id="01c83-119">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="01c83-119">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="01c83-120">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="01c83-120">End of server support</span></span><br/>    | <span data-ttu-id="01c83-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="01c83-121">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="01c83-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01c83-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="01c83-123"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="01c83-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
