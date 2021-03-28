---
description: Inviato dall'implementazione del menu di scelta rapida predefinito durante la creazione, specificando il comando di menu predefinito e consentendo di eseguire una scelta alternativa. Usato da LPFNDFMCALLBACK.
title: Messaggio DFM_GETDEFSTATICID (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fb1635b624b4c39e91ad8c31645c9aad598c7fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401619"
---
# <a name="dfm_getdefstaticid-message"></a>\_Messaggio DFM GETDEFSTATICID

Inviato dall'implementazione del menu di scelta rapida predefinito durante la creazione, specificando il comando di menu predefinito e consentendo di eseguire una scelta alternativa. Usato da [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*defaultID* \[ in uscita\]
</dt> <dd>

Puntatore all'ID del comando di menu selezionato. Viene riconosciuto il seguente flag.

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Proprietà cmd \_ DFM**


</dt> <dd>

Mostra l'interfaccia utente delle **Proprietà** per l'elemento su cui è stato richiamato il menu.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Per eseguire l'override della scelta del comando predefinita, il gestore deve, al momento della ricezione del messaggio, impostare il valore a cui punta *defaultID* sull'ID del comando di sostituzione e restituire S \_ OK. Restituisce un codice di errore in caso contrario.

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda del modo in cui viene costruito l'oggetto menu di scelta rapida predefinito. Sono disponibili due API per la relativa costruzione, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback. Usare **DFM \_ INVOKECOMMANDEX** se nell'implementazione sono necessarie informazioni aggiuntive fornite da tale interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
