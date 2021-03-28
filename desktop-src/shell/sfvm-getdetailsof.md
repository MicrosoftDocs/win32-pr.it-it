---
description: SFVM \_ GETDETAILSOF può essere modificato o non disponibile.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: Messaggio SFVM_GETDETAILSOF (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980218"
---
# <a name="sfvm_getdetailsof-message"></a><span data-ttu-id="0f81a-103">\_Messaggio SFVM GETDETAILSOF</span><span class="sxs-lookup"><span data-stu-id="0f81a-103">SFVM\_GETDETAILSOF message</span></span>

<span data-ttu-id="0f81a-104">\[**SFVM \_ GETDETAILSOF** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="0f81a-104">\[**SFVM\_GETDETAILSOF** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0f81a-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="0f81a-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="0f81a-106">Consente all'oggetto callback di fornire i dettagli per un elemento in una cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="0f81a-106">Allows the callback object to provide the details for an item in a Shell folder.</span></span> <span data-ttu-id="0f81a-107">Usare solo se una chiamata a [**IShellFolder2:: GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) ha esito negativo e non è disponibile alcun metodo [**IShellDetails:: GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) per chiamare.</span><span class="sxs-lookup"><span data-stu-id="0f81a-107">Use only if a call to [**IShellFolder2::GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) fails and there is no [**IShellDetails::GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) method available to call.</span></span> <span data-ttu-id="0f81a-108">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="0f81a-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a><span data-ttu-id="0f81a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f81a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f81a-110">*IColumn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f81a-110">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f81a-111">ID in base zero della colonna.</span><span class="sxs-lookup"><span data-stu-id="0f81a-111">The zero-based ID of the column.</span></span>

</dd> <dt>

<span data-ttu-id="0f81a-112">*pDi* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0f81a-112">*pDi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f81a-113">Puntatore a una struttura [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) riempita con le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="0f81a-113">A pointer to a [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) structure filled with the requested information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f81a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f81a-114">Requirements</span></span>



| <span data-ttu-id="0f81a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f81a-115">Requirement</span></span> | <span data-ttu-id="0f81a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0f81a-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f81a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f81a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0f81a-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0f81a-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0f81a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f81a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0f81a-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0f81a-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f81a-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0f81a-121">End of client support</span></span><br/>    | <span data-ttu-id="0f81a-122">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="0f81a-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="0f81a-123">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="0f81a-123">End of server support</span></span><br/>    | <span data-ttu-id="0f81a-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0f81a-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="0f81a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f81a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f81a-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f81a-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
