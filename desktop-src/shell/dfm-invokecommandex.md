---
description: Inviato dall'implementazione del menu di scelta rapida predefinito per richiedere a LPFNDFMCALLBACK di richiamare un comando di menu esteso.
title: DFM_INVOKECOMMANDEX messaggio (Shlobj.h)
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
ms.openlocfilehash: 2b8a7fd63aa4269ee265a4ae147c99fe394e8aad725f7134f8d62daf8ee9984b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943171"
---
# <a name="dfm_invokecommandex-message"></a>Messaggio INVOKECOMMANDEX DFM \_

Inviato dall'implementazione del menu di scelta rapida predefinito per richiedere [**a LPFNDFMCALLBACK di**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback) richiamare un comando di menu esteso.


```C++
                DFM_INVOKECOMMANDEX
    wParam = (WPARAM)(int) idCmd;           
    lParam = (LPARAM)(DFMICS) PDFMICS;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*idCmd* \[ in\]
</dt> <dd>

ID del comando di menu selezionato. Vengono riconosciuti i flag seguenti.

<dt>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>

<span id="DFM_CMD_DELETE"></span><span id="dfm_cmd_delete"></span>**DFM \_ CMD \_ DELETE**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>

<span id="DFM_CMD_MOVE"></span><span id="dfm_cmd_move"></span>**DFM \_ CMD \_ MOVE**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>

<span id="DFM_CMD_COPY"></span><span id="dfm_cmd_copy"></span>**COPIA DEI COMANDI DI DFM \_ \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>

<span id="DFM_CMD_LINK"></span><span id="dfm_cmd_link"></span>**COLLEGAMENTO CMD \_ DFM \_**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**PROPRIETÀ CMD DI \_ DFM \_**


</dt> <dd>

Mostra **l'interfaccia utente** delle proprietà per la voce su cui è stato richiamato il menu.

</dd> <dt>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>

<span id="DFM_CMD_NEWFOLDER"></span><span id="dfm_cmd_newfolder"></span>**DFM \_ CMD \_ NEWFOLDER**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>

<span id="DFM_CMD_PASTE"></span><span id="dfm_cmd_paste"></span>**DFM \_ CMD \_ PASTE**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>

<span id="DFM_CMD_VIEWLIST"></span><span id="dfm_cmd_viewlist"></span>**DFM \_ CMD \_ VIEWLIST**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>

<span id="DFM_CMD_VIEWDETAILS"></span><span id="dfm_cmd_viewdetails"></span>**VISTA CMD \_ \_ DFMDETTAGLI**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>

<span id="DFM_CMD_PASTELINK"></span><span id="dfm_cmd_pastelink"></span>**DFM \_ CMD \_ PASTELINK**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>

<span id="DFM_CMD_PASTESPECIAL"></span><span id="dfm_cmd_pastespecial"></span>**DFM \_ CMD \_ PASTESPECIAL**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>

<span id="DFM_CMD_MODALPROP"></span><span id="dfm_cmd_modalprop"></span>**DFM \_ CMD \_ MODALPROP**


</dt> <dd></dd> <dt>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>

<span id="DFM_CMD_RENAME"></span><span id="dfm_cmd_rename"></span>**DFM \_ CMD \_ RENAME**


</dt> <dd></dd> </dl> </dd> <dt>

*PDFMICS* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura DFMICS**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics) che contiene argomenti aggiuntivi per il comando di menu selezionato. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="remarks"></a>Commenti

Alla ricezione di questo messaggio, la funzione deve restituire S FALSE se si vuole che l'implementazione predefinita richiama il \_ gestore predefinito per il comando. Restituisce S \_ OK se il messaggio è stato gestito. In caso contrario, restituire un codice di errore HRESULT standard.

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di implementazione del callback. Esistono due API per la costruzione di callback, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2) che accetta un puntatore a una funzione di callback o [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) che usa un oggetto callback che supporta [**IContextMenuCB.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)

Gli elementi su cui viene richiamato il comando vengono forniti in un oggetto dati passato alla funzione di callback o al [**metodo IContextMenuCB::CallBack.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenucb-callback) Questo oggetto dati viene fornito dall'origine dati che implementa il callback. Per estrarre gli elementi dall'oggetto dati, [**usare SHCreateShellItemArrayFromDataObject.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject)

[**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md) è una versione più semplice di questo messaggio che non fornisce altre informazioni al callback. Usare **DFM \_ INVOKECOMMAND** se le informazioni aggiuntive fornite da **DFM \_ INVOKECOMMANDEX** non sono necessarie nell'implementazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
