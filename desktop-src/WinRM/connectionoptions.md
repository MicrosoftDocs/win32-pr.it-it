---
title: Oggetto ConnectionOptions (WSManDisp.h)
description: L'oggetto ConnectionOptions viene passato al metodo CreateSession per fornire il nome utente e la password associati all'account locale nel computer remoto.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- Oggetto ConnectionOptions Windows gestione remota
- Oggetto ConnectionOptions Windows Gestione remota , descritto
topic_type:
- apiref
api_name:
- ConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8665dc3a5be91fddb4332be3512ec9eec5c483495a21b95b641ec26e4e9e111
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734091"
---
# <a name="connectionoptions-object"></a>Oggetto ConnectionOptions

**L'oggetto ConnectionOptions** viene passato al [**metodo CreateSession**](wsman-createsession.md) per fornire il nome utente e la password associati all'account locale nel computer remoto. Se non viene specificato alcun parametro, le credenziali dell'account che esegue lo script vengono impostate sui valori predefiniti.

## <a name="members"></a>Membri

**L'oggetto ConnectionOptions** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto ConnectionOptions** ha queste proprietà.



| Proprietà                                                  | Tipo di accesso           | Descrizione                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Password**](connectionoptions-password.md)<br/> | Sola scrittura<br/> | Imposta la password di un account locale o di dominio nel computer remoto.<br/>           |
| [**Nome utente**](connectionoptions-username.md)<br/> | Lettura/Scrittura<br/> | Imposta e ottiene il nome utente di un account locale o di dominio nel computer remoto.<br/> |



 

## <a name="remarks"></a>Commenti

**L'oggetto ConnectionOptions** corrisponde all'interfaccia [**IWSManConnectionOptions.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)

Se un Windows'applicazione client di gestione remota è in esecuzione sotto rappresentazione, si verifica un errore se si imposta la [**proprietà Password.**](connectionoptions-password.md) Un'applicazione client è uno script o un altro programma che invia una richiesta a Gestione remota Windows nel computer locale o remoto. L'applicazione client potrebbe essere in esecuzione sotto la rappresentazione perché ha chiamato una funzione come [**ImpersonateClient.**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)) Un Active Server asp (ASP) o un servizio non può richiedere un nome utente e una password se il processo ASP viene eseguito con un account che rappresenta un client.

Il flag **WSManFlagCredUserNamePassword** deve essere impostato nella chiamata [**WSman.CreateSession**](wsman-createsession.md) quando si usano [**UserName**](connectionoptions-username.md) e [**Password**](connectionoptions-password.md) per l'autenticazione.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene illustrato come creare un oggetto **ConnectionOptions,** impostare le proprietà per l'account nel computer remoto e usarlo nella creazione di un [**oggetto Session.**](session.md)


```VB
Set objWsman = CreateObject( "Wsman.Automation" )
'Create ConnectionOptions object.
Set objConnectionOptions = objWsman.CreateConnectionOptions
objConnectionOptions.UserName = "johns "
objConnectionOptions.Password = "Dtf#4542?98"
iFlags = objWsman.SessionFlagUseBasic Or _
  objWsman.SessionFlagCredUserNamePassword
Set objSession = objWsman.CreateSession _
  ("https://172.30.168.2", iFlags, objConnectionOptions)
strResource = objSession.Get("winrm/config")
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Autenticazione per connessioni remote](authentication-for-remote-connections.md)
</dt> <dt>

[WinRM Scripting API](winrm-scripting-api.md)
</dt> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Uso Windows gestione remota](using-windows-remote-management.md)
</dt> <dt>

[Creazione di script Windows gestione remota](scripting-in-windows-remote-management.md)
</dt> <dt>

[Recupero di dati dal computer locale](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Recupero di dati da un computer remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

