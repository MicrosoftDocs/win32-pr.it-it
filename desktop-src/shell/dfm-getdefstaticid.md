---
description: Inviato dall'implementazione del menu di scelta rapida predefinita durante la creazione, specificando il comando di menu predefinito e consentendo di eseguire una scelta alternativa. Usato da LPFNDFMCALLBACK.
title: DFM_GETDEFSTATICID messaggio (Shlobj.h)
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
ms.openlocfilehash: 4d987e085779fd58f16c2534b517c39ebb4b7e3c6e2829982881015bb3a59a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094372"
---
# <a name="dfm_getdefstaticid-message"></a>Messaggio DFM \_ GETDEFSTATICID

Inviato dall'implementazione del menu di scelta rapida predefinita durante la creazione, specificando il comando di menu predefinito e consentendo di eseguire una scelta alternativa. Utilizzato da [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*defaultID* \[ in, out\]
</dt> <dd>

Puntatore all'ID del comando di menu selezionato. Viene riconosciuto il flag seguente.

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**PROPRIETÀ DEI COMANDI DFM \_ \_**


</dt> <dd>

Visualizzare **l'interfaccia** utente proprietà per la voce su cui è stato richiamato il menu.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Per eseguire l'override della scelta del comando predefinita, il gestore deve, alla ricezione di questo messaggio, impostare il valore a cui punta *defaultID* sull'ID del comando sostitutivo e restituire S \_ OK. Restituisce un codice di errore in caso contrario.

Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda della modalità di costruzione dell'oggetto menu di scelta rapida predefinito. Per la costruzione sono disponibili due API, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce altre informazioni al callback. Usare **DFM \_ INVOKECOMMANDEX** se le informazioni aggiuntive fornite da tale interfaccia sono necessarie nell'implementazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
