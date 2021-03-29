---
description: Estende l'oggetto IShellDispatch con un'ampia gamma di nuove funzionalità.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: Oggetto IShellDispatch2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79d3abbed038e09f2e73c62e5e3d9b16545e8f60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978031"
---
# <a name="ishelldispatch2-object"></a>Oggetto IShellDispatch2

Estende l'oggetto [**IShellDispatch**](ishelldispatch.md) con un'ampia gamma di nuove funzionalità.

> [!Note]  
> **IShellDispatch2** viene implementato e accessibile tramite l'oggetto [**Shell**](shell.md) .

 

## <a name="members"></a>Membri

L'oggetto **IShellDispatch2** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'oggetto **IShellDispatch2** dispone di questi metodi.



| Metodo                                                               | Descrizione                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**CanStartStopService**](ishelldispatch2-canstartstopservice.md)   | Determina se l'utente corrente può avviare e arrestare il servizio denominato.<br/>    |
| [**FindPrinter**](ishelldispatch2-findprinter.md)                   | Consente di visualizzare la finestra di dialogo **Trova stampante** .<br/>                               |
| [**GetSystemInformation**](ishelldispatch2-getsysteminformation.md) | Recupera le informazioni di sistema.<br/>                                           |
| [**IsRestricted**](ishelldispatch2-isrestricted.md)                 | Recupera l'impostazione di restrizione di un gruppo dal registro di sistema.<br/>              |
| [**IsServiceRunning**](ishelldispatch2-isservicerunning.md)         | Restituisce un valore che indica se un particolare servizio è in esecuzione.<br/> |
| [**ServiceStart**](ishelldispatch2-servicestart.md)                 | Avvia un servizio denominato.<br/>                                                 |
| [**ServiceStop**](ishelldispatch2-servicestop.md)                   | Arresta un servizio denominato.<br/>                                                  |
| [**ShellExecute**](ishelldispatch2-shellexecute.md)                 | Esegue un'operazione specificata su un file specificato.<br/>                     |
| [**ShowBrowserBar**](ishelldispatch2-showbrowserbar.md)             | Visualizza una barra del browser.<br/>                                                 |



 

## <a name="remarks"></a>Commenti

Per informazioni sui servizi Windows, vedere la documentazione relativa ai [Servizi](../services/services.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Oggetto Shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> </dl>

 

 
