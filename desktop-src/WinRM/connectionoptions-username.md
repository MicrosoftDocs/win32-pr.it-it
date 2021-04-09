---
title: Proprietà ConnectionOptions. UserName (WSManDisp. h)
description: Imposta e ottiene il nome utente di un account locale o di dominio nel computer remoto. Questa proprietà determina il nome utente per l'autenticazione.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- Proprietà UserName Gestione remota Windows
- Gestione remota Windows proprietà nomeutente, oggetto ConnectionOptions
- Oggetto ConnectionOptions Gestione remota Windows, proprietà UserName
topic_type:
- apiref
api_name:
- ConnectionOptions.UserName
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4d6c751dbe579372b863566412e740c2a646a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120374"
---
# <a name="connectionoptionsusername-property"></a>Proprietà ConnectionOptions. UserName

Imposta e ottiene il nome utente di un account locale o di dominio nel computer remoto. Questa proprietà determina il nome utente per l'autenticazione. Per altre informazioni, vedere [autenticazione per le connessioni remote](authentication-for-remote-connections.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a>Valore proprietà

Stringa che contiene il nome utente di un account locale o di dominio nel computer remoto.

Se non viene specificato alcun valore e il flag **WSManFlagCredUsernamePassword** non è impostato, viene usato il nome utente dell'account che esegue lo script.

Se non viene specificato alcun valore e viene impostato il flag **WSManFlagCredUsernamePassword** , lo script richiede all'utente di immettere il nome utente e la password. Se non viene immesso un nome utente e una password validi, viene restituito un errore di accesso negato.

## <a name="remarks"></a>Commenti

Per specificare questa proprietà, viene usata la sintassi seguente.


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



È possibile specificare **nome utente** e [**password**](connectionoptions-password.md) per un account di dominio quando si usa l'autenticazione [*Negotiate*](windows-remote-management-glossary.md) o *Kerberos* o per un account locale con autenticazione di [*base*](windows-remote-management-glossary.md) . Per connettersi a un account locale, i flag [**WSMan. CreateSession**](wsman-createsession.md) devono contenere la combinazione del flag **WSManFlagUseBasic** e del flag **WsmanFlagCredUserNamePassword** . Per connettersi a un account di dominio, i flag **WSMan. CreateSession** devono contenere la combinazione del flag **WSManFlagUseNegotiate** e del flag **WsmanFlagCredUserNamePassword** oppure la combinazione del flag **WSManFlagUseKerberos** e del flag **WsmanFlagCredUserNamePassword** . Per un account di dominio, il nome **utente** deve essere specificato nel formato "computer \\ nomeutente", dove la parte "computer" della stringa può essere il nome o l'indirizzo IP. Per altre informazioni, vedere [autenticazione per le connessioni remote](authentication-for-remote-connections.md).


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



Per la connessione a un account di dominio, i flag [**WSMan. CreateSession**](wsman-createsession.md) devono contenere la combinazione del flag **WSManFlagUseNegotiate** e il flag **WsmanFlagCredUserNamePassword** per la connessione a un account di dominio, che richiede l'autenticazione Negotiate.


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseNegotiate Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
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

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





