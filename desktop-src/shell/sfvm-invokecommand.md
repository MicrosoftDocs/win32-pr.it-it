---
description: "Notifica all'oggetto di callback che uno dei comandi di menu o barre degli strumenti è stato richiamato dall'utente. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: Messaggio SFVM_INVOKECOMMAND (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885338"
---
# <a name="sfvm_invokecommand-message"></a><span data-ttu-id="3ae33-104">\_Messaggio SFVM INVOKECOMMAND</span><span class="sxs-lookup"><span data-stu-id="3ae33-104">SFVM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="3ae33-105">Notifica all'oggetto di callback che uno dei comandi di menu o barre degli strumenti è stato richiamato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="3ae33-105">Notifies the callback object that one of its toolbar or menu commands has been invoked by the user.</span></span> <span data-ttu-id="3ae33-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="3ae33-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a><span data-ttu-id="3ae33-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ae33-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ae33-108">*idCmd* \[\]</span><span class="sxs-lookup"><span data-stu-id="3ae33-108">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ae33-109">ID del comando della barra degli strumenti o della voce di menu selezionata.</span><span class="sxs-lookup"><span data-stu-id="3ae33-109">The command ID of the selected toolbar or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ae33-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3ae33-110">Remarks</span></span>

<span data-ttu-id="3ae33-111">Questo messaggio funge essenzialmente dalla stessa funzione di un messaggio di [**\_ comando WM**](../menurc/wm-command.md) in una procedura di finestra convenzionale.</span><span class="sxs-lookup"><span data-stu-id="3ae33-111">This message serves essentially the same function as a [**WM\_COMMAND**](../menurc/wm-command.md) message in a conventional window procedure.</span></span> <span data-ttu-id="3ae33-112">Consente all'oggetto callback di gestire tutti gli elementi aggiunti alla barra dei menu o allo strumento Esplora risorse di Windows.</span><span class="sxs-lookup"><span data-stu-id="3ae33-112">It allows the callback object to handle any items that it has added to the Windows Explorer tool or menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ae33-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ae33-113">Requirements</span></span>



| <span data-ttu-id="3ae33-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ae33-114">Requirement</span></span> | <span data-ttu-id="3ae33-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3ae33-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae33-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ae33-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae33-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3ae33-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3ae33-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ae33-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae33-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3ae33-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3ae33-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ae33-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ae33-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ae33-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
