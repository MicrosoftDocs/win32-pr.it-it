---
description: Inviato dall'implementazione del menu di scelta rapida predefinito per richiedere la funzione di callback che gestisce il menu (LPFNDFMCALLBACK) per richiamare un comando di menu.
title: Messaggio DFM_INVOKECOMMAND (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd3200a6-b9e7-414c-9a01-c432cb306dba
api_name:
- DFM_INVOKECOMMAND
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 168b25833deb6bde2424ea4552f4600b83bc9679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977290"
---
# <a name="dfm_invokecommand-message"></a><span data-ttu-id="dfba5-103">\_Messaggio DFM INVOKECOMMAND</span><span class="sxs-lookup"><span data-stu-id="dfba5-103">DFM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="dfba5-104">Inviato dall'implementazione del menu di scelta rapida predefinito per richiedere la funzione di callback che gestisce il menu ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) per richiamare un comando di menu.</span><span class="sxs-lookup"><span data-stu-id="dfba5-104">Sent by the default context menu implementation to request the callback function that handles the menu ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) to invoke a menu command.</span></span>


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a><span data-ttu-id="dfba5-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="dfba5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfba5-106">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfba5-106">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfba5-107">ID del comando di menu selezionato.</span><span class="sxs-lookup"><span data-stu-id="dfba5-107">The command ID of the selected menu command.</span></span> <span data-ttu-id="dfba5-108">Vengono riconosciuti i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="dfba5-108">The following flags are recognized:</span></span>

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span data-ttu-id="dfba5-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**</span><span class="sxs-lookup"><span data-stu-id="dfba5-109"><span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM\_CMD\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-110">**Windows Vista e versioni successive**.</span><span class="sxs-lookup"><span data-stu-id="dfba5-110">**Windows Vista and later**.</span></span> <span data-ttu-id="dfba5-111">Elimina l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="dfba5-111">Delete the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span data-ttu-id="dfba5-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**\_spostamento cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="dfba5-112"><span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM\_CMD\_MOVE**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-113">**Windows Vista e versioni successive**.</span><span class="sxs-lookup"><span data-stu-id="dfba5-113">**Windows Vista and later**.</span></span> <span data-ttu-id="dfba5-114">Spostare l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="dfba5-114">Move the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span data-ttu-id="dfba5-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_copia cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="dfba5-115"><span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**DFM\_CMD\_COPY**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-116">**Windows Vista e versioni successive**.</span><span class="sxs-lookup"><span data-stu-id="dfba5-116">**Windows Vista and later**.</span></span> <span data-ttu-id="dfba5-117">Copiare l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="dfba5-117">Copy the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span data-ttu-id="dfba5-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**\_collegamento DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="dfba5-118"><span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**DFM\_CMD\_LINK**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-119">**Windows Vista e versioni successive**.</span><span class="sxs-lookup"><span data-stu-id="dfba5-119">**Windows Vista and later**.</span></span> <span data-ttu-id="dfba5-120">Consente di creare un collegamento all'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="dfba5-120">Create a link to the current item.</span></span>

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="dfba5-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Proprietà cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="dfba5-121"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-122">Mostra l'interfaccia utente delle **Proprietà** per l'elemento in cui il menu è stato richiamato.</span><span class="sxs-lookup"><span data-stu-id="dfba5-122">Show the **Properties** UI for the item on which the menu was invoked.</span></span>

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span data-ttu-id="dfba5-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**\_NewFolder cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="dfba5-123"><span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM\_CMD\_NEWFOLDER**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-124">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="dfba5-124">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span data-ttu-id="dfba5-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**\_Incolla DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="dfba5-125"><span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM\_CMD\_PASTE**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-126">**Windows Vista e versioni successive**.</span><span class="sxs-lookup"><span data-stu-id="dfba5-126">**Windows Vista and later**.</span></span> <span data-ttu-id="dfba5-127">Incollare un elemento nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="dfba5-127">Paste an item to the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span data-ttu-id="dfba5-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**\_visualizzazione DFM cmd \_**</span><span class="sxs-lookup"><span data-stu-id="dfba5-128"><span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM\_CMD\_VIEWLIST**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-129">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="dfba5-129">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span data-ttu-id="dfba5-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**\_VIEWDETAILS cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="dfba5-130"><span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**DFM\_CMD\_VIEWDETAILS**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-131">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="dfba5-131">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span data-ttu-id="dfba5-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**\_PASTELINK cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="dfba5-132"><span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM\_CMD\_PASTELINK**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-133">**Windows Vista e versioni successive**.</span><span class="sxs-lookup"><span data-stu-id="dfba5-133">**Windows Vista and later**.</span></span> <span data-ttu-id="dfba5-134">Incollare un collegamento nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="dfba5-134">Paste a link at the current location.</span></span>

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span data-ttu-id="dfba5-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**\_PASTESPECIAL cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="dfba5-135"><span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM\_CMD\_PASTESPECIAL**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-136">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="dfba5-136">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span data-ttu-id="dfba5-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**\_MODALPROP cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="dfba5-137"><span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM\_CMD\_MODALPROP**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-138">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="dfba5-138">Not supported.</span></span>

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span data-ttu-id="dfba5-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**ridenominazione DFM \_ cmd \_**</span><span class="sxs-lookup"><span data-stu-id="dfba5-139"><span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM\_CMD\_RENAME**</span></span>


</dt> <dd>

<span data-ttu-id="dfba5-140">**Windows Vista e versioni successive**.</span><span class="sxs-lookup"><span data-stu-id="dfba5-140">**Windows Vista and later**.</span></span> <span data-ttu-id="dfba5-141">Rinominare l'elemento corrente.</span><span class="sxs-lookup"><span data-stu-id="dfba5-141">Rename the current item.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="dfba5-142">*argomenti* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfba5-142">*args* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfba5-143">Puntatore a una stringa con terminazione null che contiene argomenti aggiuntivi per il comando di menu selezionato.</span><span class="sxs-lookup"><span data-stu-id="dfba5-143">A pointer to a null-terminated string that contains additional arguments to the selected menu command.</span></span> <span data-ttu-id="dfba5-144">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfba5-144">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfba5-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dfba5-145">Return value</span></span>

<span data-ttu-id="dfba5-146">Il gestore per questo messaggio deve restituire \_ false se si desidera che l'implementazione predefinita richiami il gestore predefinito per il comando.</span><span class="sxs-lookup"><span data-stu-id="dfba5-146">The handler for this message needs to return S\_FALSE if you want the default implementation to invoke the default handler for the command.</span></span> <span data-ttu-id="dfba5-147">Restituisce \_ OK se il messaggio è stato gestito.</span><span class="sxs-lookup"><span data-stu-id="dfba5-147">Return S\_OK if the message was handled.</span></span> <span data-ttu-id="dfba5-148">In caso contrario, restituisce un codice di errore HRESULT standard.</span><span class="sxs-lookup"><span data-stu-id="dfba5-148">Otherwise, return a standard HRESULT error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfba5-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfba5-149">Remarks</span></span>

<span data-ttu-id="dfba5-150">Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di implementazione del callback.</span><span class="sxs-lookup"><span data-stu-id="dfba5-150">This message is sent to either the callback function or the callback object depending on how the callback is implemented.</span></span> <span data-ttu-id="dfba5-151">Sono disponibili due API per la costruzione di callback, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) che accetta un puntatore a una funzione di callback o [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) che usa un oggetto callback che supporta [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span><span class="sxs-lookup"><span data-stu-id="dfba5-151">There are two APIs for callback construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) that takes a pointer to a callback function, or [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) that uses a callback object that supports [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).</span></span>

<span data-ttu-id="dfba5-152">Gli elementi su cui viene richiamato il comando vengono forniti in un oggetto dati passato alla funzione di callback o al metodo [**IContextMenuCB:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) .</span><span class="sxs-lookup"><span data-stu-id="dfba5-152">The items on which the command is being invoked are provided in a data object passed to the callback function or to the [**IContextMenuCB::CallBack**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) method.</span></span> <span data-ttu-id="dfba5-153">Questo oggetto dati viene fornito dall'origine dati che implementa il callback.</span><span class="sxs-lookup"><span data-stu-id="dfba5-153">This data object is provided by the data source that implements the callback.</span></span> <span data-ttu-id="dfba5-154">Per estrarre gli elementi dall'oggetto dati, utilizzare [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span><span class="sxs-lookup"><span data-stu-id="dfba5-154">To extract the items from the data object, use [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).</span></span>

<span data-ttu-id="dfba5-155">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback.</span><span class="sxs-lookup"><span data-stu-id="dfba5-155">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="dfba5-156">Usare **DFM \_ INVOKECOMMANDEX** se nell'implementazione sono necessarie informazioni aggiuntive fornite da tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="dfba5-156">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfba5-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfba5-157">Requirements</span></span>



| <span data-ttu-id="dfba5-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfba5-158">Requirement</span></span> | <span data-ttu-id="dfba5-159">Valore</span><span class="sxs-lookup"><span data-stu-id="dfba5-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dfba5-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfba5-160">Minimum supported client</span></span><br/> | <span data-ttu-id="dfba5-161">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dfba5-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dfba5-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfba5-162">Minimum supported server</span></span><br/> | <span data-ttu-id="dfba5-163">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dfba5-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dfba5-164">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dfba5-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfba5-165"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfba5-165"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
