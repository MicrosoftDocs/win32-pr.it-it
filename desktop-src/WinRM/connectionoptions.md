---
title: Oggetto ConnectionOptions (WSManDisp. h)
description: L'oggetto ConnectionOptions viene passato al metodo CreateSession per fornire il nome utente e la password associati all'account locale nel computer remoto.
ms.assetid: 7a87a5f7-78ed-452c-9b9f-ad48811a3339
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows oggetto ConnectionOptions
- Oggetto ConnectionOptions Gestione remota Windows, descritto
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
ms.openlocfilehash: 164eb886ce98266cab3109e773b731e002d1abac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301956"
---
# <a name="connectionoptions-object"></a>Oggetto ConnectionOptions

L'oggetto **ConnectionOptions** viene passato al metodo [**CreateSession**](wsman-createsession.md) per fornire il nome utente e la password associati all'account locale nel computer remoto. Se non viene fornito alcun parametro, le credenziali dell'account che esegue lo script vengono impostate sui valori predefiniti.

## <a name="members"></a>Membri

L'oggetto **ConnectionOptions** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **ConnectionOptions** dispone di queste proprietà.



| Proprietà                                                  | Tipo di accesso           | Descrizione                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Password**](connectionoptions-password.md)<br/> | Sola scrittura<br/> | Imposta la password di un account locale o di dominio nel computer remoto.<br/>           |
| [**Nome utente**](connectionoptions-username.md)<br/> | Lettura/Scrittura<br/> | Imposta e ottiene il nome utente di un account locale o di dominio nel computer remoto.<br/> |



 

## <a name="remarks"></a>Commenti

L'oggetto **ConnectionOptions** corrisponde all'interfaccia [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions) .

Se un'applicazione client Gestione remota Windows viene eseguita con la rappresentazione, si verifica un errore se si imposta la proprietà [**password**](connectionoptions-password.md) . Un'applicazione client è uno script o un altro programma che invia una richiesta a WinRM nel computer locale o remoto. È possibile che l'applicazione client sia in esecuzione con la rappresentazione perché è stata chiamata funzione come [**ImpersonateClient**](/previous-versions/windows/desktop/legacy/aa375494(v=vs.85)). Una pagina Active Server (ASP) o un servizio non può richiedere un nome utente e una password se il processo ASP viene eseguito con un account che rappresenta un client.

Il flag **WSManFlagCredUserNamePassword** deve essere impostato sulla chiamata [**WSMan. CreateSession**](wsman-createsession.md) quando si usano il [**nome utente**](connectionoptions-username.md) e la [**password**](connectionoptions-password.md) per l'autenticazione.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene illustrato come creare un oggetto **ConnectionOptions** , impostare le proprietà per l'account nel computer remoto e utilizzarlo per creare un oggetto [**sessione**](session.md) .


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Autenticazione per le connessioni remote](authentication-for-remote-connections.md)
</dt> <dt>

[API di scripting WinRM](winrm-scripting-api.md)
</dt> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Utilizzo di Gestione remota Windows](using-windows-remote-management.md)
</dt> <dt>

[Creazione di script in Gestione remota Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Recupero di dati dal computer locale](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Recupero di dati da un computer remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

