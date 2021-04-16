---
description: "Notifica all'oggetto di callback che l'utente ha fatto clic su un'intestazione di colonna per ordinare l'elenco di oggetti nella visualizzazione cartelle. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_COLUMNCLICK (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485516"
---
# <a name="sfvm_columnclick-message"></a><span data-ttu-id="49652-104">\_Messaggio SFVM COLUMNCLICK</span><span class="sxs-lookup"><span data-stu-id="49652-104">SFVM\_COLUMNCLICK message</span></span>

<span data-ttu-id="49652-105">Notifica all'oggetto di callback che l'utente ha fatto clic su un'intestazione di colonna per ordinare l'elenco di oggetti nella visualizzazione cartelle.</span><span class="sxs-lookup"><span data-stu-id="49652-105">Notifies the callback object that the user has clicked a column header to sort the list of objects in the folder view.</span></span> <span data-ttu-id="49652-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="49652-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="49652-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="49652-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49652-108">*IColumn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49652-108">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49652-109">Indice della colonna su cui è stato fatto clic.</span><span class="sxs-lookup"><span data-stu-id="49652-109">The index of the column that was clicked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49652-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="49652-110">Remarks</span></span>

<span data-ttu-id="49652-111">In risposta a questa notifica, è necessario restituire S \_ OK per ridisporre l'elenco.</span><span class="sxs-lookup"><span data-stu-id="49652-111">In response to this notification, you should return S\_OK to rearrange the list yourself.</span></span> <span data-ttu-id="49652-112">Per fare in modo che l'oggetto visualizzazione cartella di sistema ridisponga l'elenco, restituire S \_ false.</span><span class="sxs-lookup"><span data-stu-id="49652-112">To have the system folder view object rearrange the list, return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="49652-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49652-113">Requirements</span></span>



| <span data-ttu-id="49652-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="49652-114">Requirement</span></span> | <span data-ttu-id="49652-115">Valore</span><span class="sxs-lookup"><span data-stu-id="49652-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="49652-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49652-116">Minimum supported client</span></span><br/> | <span data-ttu-id="49652-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49652-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="49652-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49652-118">Minimum supported server</span></span><br/> | <span data-ttu-id="49652-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49652-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="49652-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49652-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="49652-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="49652-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
