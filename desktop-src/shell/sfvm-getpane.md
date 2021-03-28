---
description: SFVM \_ GetPane può essere modificato o non disponibile.
ms.assetid: 9621b921-e97f-4219-953a-7c961a81c379
title: Messaggio SFVM_GETPANE (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2800be1b7b427e13014686e587b51fc4bf7d7617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967838"
---
# <a name="sfvm_getpane-message"></a><span data-ttu-id="3d066-103">\_Messaggio GETPANE SFVM</span><span class="sxs-lookup"><span data-stu-id="3d066-103">SFVM\_GETPANE message</span></span>

<span data-ttu-id="3d066-104">\[**SFVM \_ GetPane** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="3d066-104">\[**SFVM\_GETPANE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3d066-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="3d066-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="3d066-106">Consente all'oggetto callback di fornire il riquadro della barra di stato in cui visualizzare le informazioni sull'area Internet.</span><span class="sxs-lookup"><span data-stu-id="3d066-106">Allows the callback object to provide the status bar pane in which to display the Internet zone information.</span></span> <span data-ttu-id="3d066-107">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="3d066-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETPANE
    wParam = (WPARAM)(int) paneID;
    lParam = (LPARAM)(DWORD*) pane;
            
```



## <a name="parameters"></a><span data-ttu-id="3d066-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d066-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d066-109">*paneID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d066-109">*paneID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d066-110">ID del riquadro richiesto.</span><span class="sxs-lookup"><span data-stu-id="3d066-110">ID of the requested pane.</span></span> <span data-ttu-id="3d066-111">Si tratta in genere \_ di una zona del riquadro, ma può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3d066-111">This is normally PANE\_ZONE, but can be any one of the following values.</span></span>

<dt>

<span id="PANE_NONE"></span><span id="pane_none"></span>

<span data-ttu-id="3d066-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**\_nessun riquadro**</span><span class="sxs-lookup"><span data-stu-id="3d066-112"><span id="PANE_NONE"></span><span id="pane_none"></span>**PANE\_NONE**</span></span>


</dt> <dd>

<span data-ttu-id="3d066-113">Nessun riquadro.</span><span class="sxs-lookup"><span data-stu-id="3d066-113">No pane.</span></span>

</dd> <dt>

<span id="PANE_ZONE"></span><span id="pane_zone"></span>

<span data-ttu-id="3d066-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**area del riquadro \_**</span><span class="sxs-lookup"><span data-stu-id="3d066-114"><span id="PANE_ZONE"></span><span id="pane_zone"></span>**PANE\_ZONE**</span></span>


</dt> <dd>

<span data-ttu-id="3d066-115">Riquadro dell'area Internet.</span><span class="sxs-lookup"><span data-stu-id="3d066-115">The Internet zone pane.</span></span>

</dd> <dt>

<span id="PANE_OFFLINE"></span><span id="pane_offline"></span>

<span data-ttu-id="3d066-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**RIQUADRO \_ offline**</span><span class="sxs-lookup"><span data-stu-id="3d066-116"><span id="PANE_OFFLINE"></span><span id="pane_offline"></span>**PANE\_OFFLINE**</span></span>


</dt> <dd>

<span data-ttu-id="3d066-117">Il riquadro offline.</span><span class="sxs-lookup"><span data-stu-id="3d066-117">The offline pane.</span></span>

</dd> <dt>

<span id="PANE_PRINTER"></span><span id="pane_printer"></span>

<span data-ttu-id="3d066-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**stampante riquadri \_**</span><span class="sxs-lookup"><span data-stu-id="3d066-118"><span id="PANE_PRINTER"></span><span id="pane_printer"></span>**PANE\_PRINTER**</span></span>


</dt> <dd>

<span data-ttu-id="3d066-119">Riquadro dell'indicazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="3d066-119">The print indication pane.</span></span>

</dd> <dt>

<span id="PANE_SSL"></span><span id="pane_ssl"></span>

<span data-ttu-id="3d066-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**SSL del riquadro \_**</span><span class="sxs-lookup"><span data-stu-id="3d066-120"><span id="PANE_SSL"></span><span id="pane_ssl"></span>**PANE\_SSL**</span></span>


</dt> <dd>

<span data-ttu-id="3d066-121">Il riquadro SSL.</span><span class="sxs-lookup"><span data-stu-id="3d066-121">The SSL pane.</span></span>

</dd> <dt>

<span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>

<span data-ttu-id="3d066-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**\_navigazione riquadro**</span><span class="sxs-lookup"><span data-stu-id="3d066-122"><span id="PANE_NAVIGATION"></span><span id="pane_navigation"></span>**PANE\_NAVIGATION**</span></span>


</dt> <dd>

<span data-ttu-id="3d066-123">Riquadro di spostamento.</span><span class="sxs-lookup"><span data-stu-id="3d066-123">The navigation pane.</span></span>

</dd> <dt>

<span id="PANE_PROGRESS"></span><span id="pane_progress"></span>

<span data-ttu-id="3d066-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**\_stato riquadro**</span><span class="sxs-lookup"><span data-stu-id="3d066-124"><span id="PANE_PROGRESS"></span><span id="pane_progress"></span>**PANE\_PROGRESS**</span></span>


</dt> <dd>

<span data-ttu-id="3d066-125">Riquadro indicatore di stato.</span><span class="sxs-lookup"><span data-stu-id="3d066-125">The progress bar pane.</span></span>

</dd> <dt>

<span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>

<span data-ttu-id="3d066-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**PRIVACY del riquadro \_**</span><span class="sxs-lookup"><span data-stu-id="3d066-126"><span id="PANE_PRIVACY"></span><span id="pane_privacy"></span>**PANE\_PRIVACY**</span></span>


</dt> <dd>

<span data-ttu-id="3d066-127">Riquadro dell'indicatore della privacy.</span><span class="sxs-lookup"><span data-stu-id="3d066-127">The privacy indicator pane.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3d066-128">*riquadro* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d066-128">*pane* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d066-129">Puntatore a un **valore DWORD** contenente il numero del riquadro.</span><span class="sxs-lookup"><span data-stu-id="3d066-129">Pointer to a **DWORD** containing the pane number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d066-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d066-130">Requirements</span></span>



| <span data-ttu-id="3d066-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d066-131">Requirement</span></span> | <span data-ttu-id="3d066-132">Valore</span><span class="sxs-lookup"><span data-stu-id="3d066-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3d066-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d066-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3d066-134">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3d066-134">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3d066-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d066-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3d066-136">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3d066-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3d066-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3d066-137">End of client support</span></span><br/>    | <span data-ttu-id="3d066-138">Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="3d066-138">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="3d066-139">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="3d066-139">End of server support</span></span><br/>    | <span data-ttu-id="3d066-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3d066-140">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="3d066-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d066-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d066-142"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d066-142"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
