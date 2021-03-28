---
description: Inviato dall'implementazione del menu di scelta rapida predefinito per richiedere LPFNDFMCALLBACK per richiamare un comando di menu esteso.
title: Messaggio DFM_INVOKECOMMANDEX (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6ef885e5-2ddd-4a1b-9f8e-016a74e292b1
api_name:
- DFM_INVOKECOMMANDEX
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dc96e9d0e4c27be8dee3ed7742874de4a3fb97e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525362"
---
# <a name="dfm_invokecommandex-message"></a><span data-ttu-id="695ab-103">\_Messaggio DFM INVOKECOMMANDEX</span><span class="sxs-lookup"><span data-stu-id="695ab-103">DFM\_INVOKECOMMANDEX message</span></span>

<span data-ttu-id="695ab-104">Inviato dall'implementazione del menu di scelta rapida predefinito per richiedere [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) per richiamare un comando di menu esteso.</span><span class="sxs-lookup"><span data-stu-id="695ab-104">Sent by the default context menu implementation to request [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) to invoke an extended menu command.</span></span>


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a><span data-ttu-id="695ab-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="695ab-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="695ab-106">*idCmd* \[\]</span><span class="sxs-lookup"><span data-stu-id="695ab-106">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695ab-107">ID del comando di menu selezionato.</span><span class="sxs-lookup"><span data-stu-id="695ab-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="695ab-108">Vengono riconosciuti i flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="695ab-108">The following flags are recognized.</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="695ab-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="695ab-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="695ab-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**\_spostamento cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="695ab-110"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="695ab-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_copia cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="695ab-111"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="695ab-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**\_collegamento DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="695ab-112"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="695ab-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Proprietà cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="695ab-113"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="695ab-114">Mostra l'interfaccia utente delle **Proprietà** per l'elemento su cui è stato richiamato il menu.</span><span class="sxs-lookup"><span data-stu-id="695ab-114">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="695ab-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**\_NewFolder cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="695ab-115"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="695ab-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**\_Incolla DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="695ab-116"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="695ab-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**\_visualizzazione DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="695ab-117"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="695ab-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**\_VIEWDETAILS cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="695ab-118"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="695ab-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**\_PASTELINK cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="695ab-119"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="695ab-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**\_PASTESPECIAL cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="695ab-120"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="695ab-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**\_MODALPROP cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="695ab-121"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="695ab-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**ridenominazione DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="695ab-122"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="695ab-123">*PDFMICS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="695ab-123">*PDFMICS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695ab-124">Puntatore a una struttura [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) che contiene argomenti aggiuntivi per il comando di menu selezionato.</span><span class="sxs-lookup"><span data-stu-id="695ab-124">A pointer to a [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) structure that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="695ab-125">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="695ab-125">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="695ab-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="695ab-126">Remarks</span></span>

<span data-ttu-id="695ab-127">Alla ricezione di questo messaggio, la funzione deve restituire S \_ false se si desidera che l'implementazione predefinita richiami il gestore predefinito per il comando.</span><span class="sxs-lookup"><span data-stu-id="695ab-127">Upon receipt of this message, your function should return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="695ab-128">Restituisce \_ OK se il messaggio è stato gestito.</span><span class="sxs-lookup"><span data-stu-id="695ab-128">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="695ab-129">In caso contrario, restituisce un codice di errore HRESULT standard.</span><span class="sxs-lookup"><span data-stu-id="695ab-129">Otherwise, return a standard HRESULT error code.</span></span>

<span data-ttu-id="695ab-130">Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di implementazione del callback.</span><span class="sxs-lookup"><span data-stu-id="695ab-130">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="695ab-131">Sono disponibili due API per la costruzione di callback, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) che accetta un puntatore a una funzione di callback o [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) che usa un oggetto callback che supporta [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span><span class="sxs-lookup"><span data-stu-id="695ab-131">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="695ab-132">Gli elementi su cui viene richiamato il comando vengono forniti in un oggetto dati passato alla funzione di callback o al metodo [**IContextMenuCB:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) .</span><span class="sxs-lookup"><span data-stu-id="695ab-132">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="695ab-133">Questo oggetto dati viene fornito dall'origine dati che implementa il callback.</span><span class="sxs-lookup"><span data-stu-id="695ab-133">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="695ab-134">Per estrarre gli elementi dall'oggetto dati, utilizzare [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="695ab-134">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="695ab-135">[**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md) è una versione più semplice di questo messaggio che non fornisce la maggior parte delle informazioni al callback.</span><span class="sxs-lookup"><span data-stu-id="695ab-135">[**DFM\_INVOKECOMMAND**](dfm-invokecommand.md) is a simpler version of this message which does not provide as much information to the callback.</span></span> <span data-ttu-id="695ab-136">Usare **DFM \_ INVOKECOMMAND** se nell'implementazione non sono necessarie le informazioni aggiuntive fornite da **DFM \_ INVOKECOMMANDEX** .</span><span class="sxs-lookup"><span data-stu-id="695ab-136">Use **DFM\_INVOKECOMMAND** if the additional information provided by **DFM\_INVOKECOMMANDEX** is not needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="695ab-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="695ab-137">Requirements</span></span>



| <span data-ttu-id="695ab-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="695ab-138">Requirement</span></span> | <span data-ttu-id="695ab-139">Valore</span><span class="sxs-lookup"><span data-stu-id="695ab-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="695ab-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="695ab-140">Minimum supported client</span></span><br/> | <span data-ttu-id="695ab-141">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="695ab-141">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="695ab-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="695ab-142">Minimum supported server</span></span><br/> | <span data-ttu-id="695ab-143">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="695ab-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="695ab-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="695ab-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="695ab-145"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="695ab-145"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
