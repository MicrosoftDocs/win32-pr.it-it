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
# <a name="dfm_invokecommandex-message"></a>\_Messaggio DFM INVOKECOMMANDEX

Inviato dall'implementazione del menu di scelta rapida predefinito per richiedere [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) per richiamare un comando di menu esteso.


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd* \[\]
</dt> <dd>

ID del comando di menu selezionato. Vengono riconosciuti i flag seguenti.

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ cmd \_ Delete**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**\_spostamento cmd \_ DFM**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**\_copia cmd \_ DFM**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**\_collegamento DFM cmd \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Proprietà cmd \_ DFM**


</dt> <dd>

Mostra l'interfaccia utente delle **Proprietà** per l'elemento su cui è stato richiamato il menu.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**\_NewFolder cmd \_ DFM**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**\_Incolla DFM cmd \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**\_visualizzazione DFM cmd \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**\_VIEWDETAILS cmd \_ DFM**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**\_PASTELINK cmd \_ DFM**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**\_PASTESPECIAL cmd \_ DFM**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**\_MODALPROP cmd \_ DFM**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**ridenominazione DFM \_ cmd \_**


</dt> <dd></dd> </dl> </dd> <dt>

*PDFMICS* \[ in\]
</dt> <dd>

Puntatore a una struttura [**DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) che contiene argomenti aggiuntivi per il comando di menu selezionato. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Alla ricezione di questo messaggio, la funzione deve restituire S \_ false se si desidera che l'implementazione predefinita richiami il gestore predefinito per il comando. Restituisce \_ OK se il messaggio è stato gestito. In caso contrario, restituisce un codice di errore HRESULT standard.

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di implementazione del callback. Sono disponibili due API per la costruzione di callback, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) che accetta un puntatore a una funzione di callback o [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) che usa un oggetto callback che supporta [**IContextMenuCB**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb).

Gli elementi su cui viene richiamato il comando vengono forniti in un oggetto dati passato alla funzione di callback o al metodo [**IContextMenuCB:: callback**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) . Questo oggetto dati viene fornito dall'origine dati che implementa il callback. Per estrarre gli elementi dall'oggetto dati, utilizzare [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject).

[**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md) è una versione più semplice di questo messaggio che non fornisce la maggior parte delle informazioni al callback. Usare **DFM \_ INVOKECOMMAND** se nell'implementazione non sono necessarie le informazioni aggiuntive fornite da **DFM \_ INVOKECOMMANDEX** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
