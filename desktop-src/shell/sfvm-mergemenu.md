---
description: "Consente all'oggetto callback di unire le voci di menu nei menu di Esplora risorse. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_MERGEMENU (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980831"
---
# <a name="sfvm_mergemenu-message"></a><span data-ttu-id="33571-104">\_Messaggio SFVM MERGEMENU</span><span class="sxs-lookup"><span data-stu-id="33571-104">SFVM\_MERGEMENU message</span></span>

<span data-ttu-id="33571-105">Consente all'oggetto callback di unire le voci di menu nei menu di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="33571-105">Allows the callback object to merge menu items into the Windows Explorer menus.</span></span> <span data-ttu-id="33571-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="33571-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a><span data-ttu-id="33571-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="33571-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33571-108">*pInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="33571-108">*pInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33571-109">Struttura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenente le informazioni necessarie per unire gli elementi nel menu.</span><span class="sxs-lookup"><span data-stu-id="33571-109">A [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information needed to merge the items into the menu.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33571-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="33571-110">Remarks</span></span>

<span data-ttu-id="33571-111">Questo messaggio ha essenzialmente lo stesso scopo di [**IShellBrowser:: InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) e [**IShellBrowser:: SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in una visualizzazione cartella personalizzata.</span><span class="sxs-lookup"><span data-stu-id="33571-111">This message serves essentially the same purpose as the [**IShellBrowser::InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) and [**IShellBrowser::SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in a custom folder view.</span></span> <span data-ttu-id="33571-112">Per ulteriori informazioni, vedere la sezione *uso di IShellBrowser per comunicare con Esplora risorse* di [implementazione di una visualizzazione cartella](../lwef/nse-folderview.md) .</span><span class="sxs-lookup"><span data-stu-id="33571-112">See the *Using IShellBrowser to Communicate with Windows Explorer* section of [Implementing a Folder View](../lwef/nse-folderview.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="33571-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33571-113">Requirements</span></span>



| <span data-ttu-id="33571-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="33571-114">Requirement</span></span> | <span data-ttu-id="33571-115">Valore</span><span class="sxs-lookup"><span data-stu-id="33571-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="33571-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33571-116">Minimum supported client</span></span><br/> | <span data-ttu-id="33571-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33571-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="33571-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33571-118">Minimum supported server</span></span><br/> | <span data-ttu-id="33571-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33571-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="33571-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33571-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="33571-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="33571-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
