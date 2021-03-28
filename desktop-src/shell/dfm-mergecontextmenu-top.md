---
description: Consente al callback di aggiungere elementi nella parte superiore del menu esteso.
title: Messaggio DFM_MERGECONTEXTMENU_TOP (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: eed6aec6-11a0-4738-b5b9-a455d0e35eac
api_name:
- DFM_MERGECONTEXTMENU_TOP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5810b5b6a0fc862b4dd8a9605cb9aa5c0c83afc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525356"
---
# <a name="dfm_mergecontextmenu_top-message"></a><span data-ttu-id="3e124-103">DFM \_ MERGECONTEXTMENU- \_ messaggio principale</span><span class="sxs-lookup"><span data-stu-id="3e124-103">DFM\_MERGECONTEXTMENU\_TOP message</span></span>

<span data-ttu-id="3e124-104">Consente al callback di aggiungere elementi nella parte superiore del menu esteso.</span><span class="sxs-lookup"><span data-stu-id="3e124-104">Allows the callback to add items to the top of the extended menu.</span></span>


```C++
DFM_MERGECONTEXTMENU_TOP

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="3e124-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e124-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e124-106">*pqcminfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e124-106">*pqcminfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e124-107">Puntatore a una struttura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenente le informazioni utilizzate nell'Unione.</span><span class="sxs-lookup"><span data-stu-id="3e124-107">A pointer to a [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information used in the merge.</span></span>

</dd> <dt>

<span data-ttu-id="3e124-108">*uFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e124-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e124-109">Flag che specificano il modo in cui il menu di scelta rapida può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="3e124-109">Flags specifying how the context menu can be changed.</span></span> <span data-ttu-id="3e124-110">Questo parametro usa i \_ \* valori CMF descritti in [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="3e124-110">This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e124-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e124-111">Remarks</span></span>

<span data-ttu-id="3e124-112">Se gli elementi vengono aggiunti al menu di scelta rapida esteso, è necessario che siano supportati con routine che rispondono in modo appropriato quando uno di questi elementi viene richiamato usando [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md).</span><span class="sxs-lookup"><span data-stu-id="3e124-112">If items are added to the extended context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).</span></span>

<span data-ttu-id="3e124-113">Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di implementazione dell'oggetto menu di scelta rapida predefinito.</span><span class="sxs-lookup"><span data-stu-id="3e124-113">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="3e124-114">Sono disponibili due API per la relativa implementazione, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="3e124-114">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="3e124-115">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback.</span><span class="sxs-lookup"><span data-stu-id="3e124-115">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="3e124-116">Usare **DFM \_ INVOKECOMMANDEX** se nell'implementazione sono necessarie informazioni aggiuntive fornite da tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3e124-116">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e124-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e124-117">Requirements</span></span>



| <span data-ttu-id="3e124-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e124-118">Requirement</span></span> | <span data-ttu-id="3e124-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3e124-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3e124-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e124-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3e124-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e124-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3e124-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e124-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3e124-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e124-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3e124-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e124-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e124-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e124-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




