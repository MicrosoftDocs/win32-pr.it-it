---
title: CFSTR_DSOP_DS_SELECTION_LIST (objsel. h)
description: Il formato degli Appunti dell'elenco di selezione di CFSTR \_ DSOP \_ DS \_ \_ fornisce un HGLOBAL che contiene una \_ struttura di elenco di selezione DS \_ . La \_ struttura dell'elenco di selezione DS contiene i \_ dati relativi agli elementi selezionati in una finestra di dialogo di selezione oggetti directory.
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964059"
---
# <a name="cfstr_dsop_ds_selection_list"></a><span data-ttu-id="98145-104">\_elenco di \_ \_ selezione DS DSOP CFSTR \_</span><span class="sxs-lookup"><span data-stu-id="98145-104">CFSTR\_DSOP\_DS\_SELECTION\_LIST</span></span>

<dl> <dt>

<span data-ttu-id="98145-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**\_elenco di \_ \_ selezione DS DSOP CFSTR \_**</span><span class="sxs-lookup"><span data-stu-id="98145-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**CFSTR\_DSOP\_DS\_SELECTION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98145-106">"CFSTR \_ DSOP \_ DS \_ Selection \_ List"</span><span class="sxs-lookup"><span data-stu-id="98145-106">"CFSTR\_DSOP\_DS\_SELECTION\_LIST"</span></span>
</dt> <dt>



<span data-ttu-id="98145-107">Il formato degli Appunti dell' **elenco di \_ selezione CFSTR DSOP \_ DS \_ \_** viene fornito dal [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) ottenuto chiamando [**IDsObjectPicker:: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span><span class="sxs-lookup"><span data-stu-id="98145-107">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format is provided by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtained by calling [**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span></span> <span data-ttu-id="98145-108">Il formato degli Appunti dell' **elenco di selezione di CFSTR \_ DSOP \_ \_ \_ DS** fornisce un **HGLOBAL** che contiene una struttura di [**\_ \_ elenco di selezione DS**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) .</span><span class="sxs-lookup"><span data-stu-id="98145-108">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format provides an **HGLOBAL** that contains a [**DS\_SELECTION\_LIST**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) structure.</span></span> <span data-ttu-id="98145-109">La struttura dell' **\_ \_ elenco di selezione DS** contiene i dati relativi agli elementi selezionati in una finestra di dialogo di [selezione oggetti directory](directory-object-picker.md) .</span><span class="sxs-lookup"><span data-stu-id="98145-109">The **DS\_SELECTION\_LIST** structure contains data about the items selected in a [Directory Object Picker](directory-object-picker.md) dialog box.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98145-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98145-110">Requirements</span></span>



| <span data-ttu-id="98145-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="98145-111">Requirement</span></span> | <span data-ttu-id="98145-112">Valore</span><span class="sxs-lookup"><span data-stu-id="98145-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="98145-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98145-113">Minimum supported client</span></span><br/> | <span data-ttu-id="98145-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98145-114">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="98145-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98145-115">Minimum supported server</span></span><br/> | <span data-ttu-id="98145-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98145-116">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="98145-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98145-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="98145-118"><dt>Objsel. h</dt></span><span class="sxs-lookup"><span data-stu-id="98145-118"><dt>Objsel.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98145-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98145-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98145-120">**\_elenco di selezione DS \_**</span><span class="sxs-lookup"><span data-stu-id="98145-120">**DS\_SELECTION\_LIST**</span></span>](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[<span data-ttu-id="98145-121">**IDsObjectPicker::InvokeDialog**</span><span class="sxs-lookup"><span data-stu-id="98145-121">**IDsObjectPicker::InvokeDialog**</span></span>](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[<span data-ttu-id="98145-122">Selezione oggetti directory</span><span class="sxs-lookup"><span data-stu-id="98145-122">Directory Object Picker</span></span>](directory-object-picker.md)
</dt> </dl>

 

