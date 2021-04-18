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
# <a name="dfm_invokecommand-message"></a>\_Messaggio DFM INVOKECOMMAND

Inviato dall'implementazione del menu di scelta rapida predefinito per richiedere la funzione di callback che gestisce il menu ([**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)) per richiamare un comando di menu.


```C++
DFM_INVOKECOMMAND
    wParam = (WPARAM)(int) id;          
    lParam = (LPARAM)(LPWSTR) args;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

ID del comando di menu selezionato. Vengono riconosciuti i flag seguenti:

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**


</dt> <dd>

**Windows Vista e versioni successive**. Elimina l'elemento corrente.

</dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**\_spostamento cmd \_ DFM**


</dt> <dd>

**Windows Vista e versioni successive**. Spostare l'elemento corrente.

</dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_copia cmd \_ DFM**


</dt> <dd>

**Windows Vista e versioni successive**. Copiare l'elemento corrente.

</dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**\_collegamento DFM cmd \_**


</dt> <dd>

**Windows Vista e versioni successive**. Consente di creare un collegamento all'elemento corrente.

</dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Proprietà cmd \_ DFM**


</dt> <dd>

Mostra l'interfaccia utente delle **Proprietà** per l'elemento in cui il menu è stato richiamato.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**\_NewFolder cmd \_ DFM**


</dt> <dd>

Non supportata.

</dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**\_Incolla DFM cmd \_**


</dt> <dd>

**Windows Vista e versioni successive**. Incollare un elemento nella posizione corrente.

</dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**\_visualizzazione DFM cmd \_**


</dt> <dd>

Non supportata.

</dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**\_VIEWDETAILS cmd \_ DFM**


</dt> <dd>

Non supportata.

</dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**\_PASTELINK cmd \_ DFM**


</dt> <dd>

**Windows Vista e versioni successive**. Incollare un collegamento nella posizione corrente.

</dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**\_PASTESPECIAL cmd \_ DFM**


</dt> <dd>

Non supportata.

</dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**\_MODALPROP cmd \_ DFM**


</dt> <dd>

Non supportata.

</dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**ridenominazione DFM \_ cmd \_**


</dt> <dd>

**Windows Vista e versioni successive**. Rinominare l'elemento corrente.

</dd> </dl> </dd> <dt>

*argomenti* \[ in\]
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene argomenti aggiuntivi per il comando di menu selezionato. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il gestore per questo messaggio deve restituire \_ false se si desidera che l'implementazione predefinita richiami il gestore predefinito per il comando. Restituisce \_ OK se il messaggio è stato gestito. In caso contrario, restituisce un codice di errore HRESULT standard.

## <a name="remarks"></a>Commenti

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di implementazione del callback. Sono disponibili due API per la costruzione di callback, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) che accetta un puntatore a una funzione di callback o [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) che usa un oggetto callback che supporta [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).

Gli elementi su cui viene richiamato il comando vengono forniti in un oggetto dati passato alla funzione di callback o al metodo [**IContextMenuCB:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) . Questo oggetto dati viene fornito dall'origine dati che implementa il callback. Per estrarre gli elementi dall'oggetto dati, utilizzare [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback. Usare **DFM \_ INVOKECOMMANDEX** se nell'implementazione sono necessarie informazioni aggiuntive fornite da tale interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
