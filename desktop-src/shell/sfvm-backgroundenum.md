---
description: "Consente all'oggetto callback di richiedere l'enumerazione in un thread in background. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_BACKGROUNDENUM (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994920"
---
# <a name="sfvm_backgroundenum-message"></a><span data-ttu-id="1e6a5-104">\_Messaggio SFVM BACKGROUNDENUM</span><span class="sxs-lookup"><span data-stu-id="1e6a5-104">SFVM\_BACKGROUNDENUM message</span></span>

<span data-ttu-id="1e6a5-105">Consente all'oggetto callback di richiedere l'enumerazione in un thread in background.</span><span class="sxs-lookup"><span data-stu-id="1e6a5-105">Allows the callback object to request enumeration on a background thread.</span></span> <span data-ttu-id="1e6a5-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="1e6a5-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a><span data-ttu-id="1e6a5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e6a5-107">Parameters</span></span>

<span data-ttu-id="1e6a5-108">Questo messaggio non contiene parametri.</span><span class="sxs-lookup"><span data-stu-id="1e6a5-108">This message has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e6a5-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e6a5-109">Remarks</span></span>

<span data-ttu-id="1e6a5-110">In risposta a questa notifica, restituire S \_ OK per abilitare l'enumerazione in background.</span><span class="sxs-lookup"><span data-stu-id="1e6a5-110">In response to this notification, return S\_OK to enable background enumeration.</span></span> <span data-ttu-id="1e6a5-111">Per impostazione predefinita, l'oggetto cartella di sistema visualizzerà l'animazione "torcia" mentre è in corso l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1e6a5-111">By default, the system folder object will display the "flashlight" animation while the enumeration is taking place.</span></span> <span data-ttu-id="1e6a5-112">Per specificare un'animazione personalizzata, gestire [**SFVM \_ getanimation**](sfvm-getanimation.md).</span><span class="sxs-lookup"><span data-stu-id="1e6a5-112">To specify a custom animation, handle [**SFVM\_GETANIMATION**](sfvm-getanimation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e6a5-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e6a5-113">Requirements</span></span>



| <span data-ttu-id="1e6a5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e6a5-114">Requirement</span></span> | <span data-ttu-id="1e6a5-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1e6a5-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1e6a5-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e6a5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1e6a5-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1e6a5-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1e6a5-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e6a5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1e6a5-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1e6a5-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1e6a5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e6a5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e6a5-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e6a5-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
