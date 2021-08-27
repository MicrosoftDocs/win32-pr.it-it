---
title: Proprietà ConnectionOptions.UserName (WSManDisp.h)
description: Imposta e ottiene il nome utente di un account locale o di dominio nel computer remoto. Questa proprietà determina il nome utente per l'autenticazione.
ms.assetid: e8f70143-f002-4b39-97a3-006b9713262d
ms.tgt_platform: multiple
keywords:
- Proprietà UserName Windows Gestione remota
- Proprietà UserName Windows gestione remota, oggetto ConnectionOptions
- Oggetto ConnectionOptions Windows proprietà Gestione remota , UserName
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
ms.openlocfilehash: 40fa4cd5e1d4fd733431adab80241744c0b197960506cfe2908bc99315ecfdea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121781"
---
# <a name="connectionoptionsusername-property"></a>ConnectionOptions.UserName - proprietà

Imposta e ottiene il nome utente di un account locale o di dominio nel computer remoto. Questa proprietà determina il nome utente per l'autenticazione. Per altre informazioni, vedere [Autenticazione per connessioni remote.](authentication-for-remote-connections.md)

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ConnectionOptions.UserName As String
```



## <a name="property-value"></a>Valore proprietà

Stringa contenente il nome utente di un account locale o di dominio nel computer remoto.

Se non viene specificato alcun valore e il flag **WSManFlagCredUsernamePassword** non è impostato, viene utilizzato il nome utente dell'account che esegue lo script.

Se non viene specificato alcun valore e il flag **WSManFlagCredUsernamePassword** è impostato, lo script richiede all'utente di immettere il nome utente e la password. Se non vengono immessi un nome utente e una password validi, viene restituito un errore di accesso negato.

## <a name="remarks"></a>Commenti

La sintassi seguente viene utilizzata per specificare questa proprietà.


```VB
Set ConnectionOptions = wsman.CreateConnectionOptions
ConnectionOptions.UserName = "<UserName>"
```



È possibile specificare **UserName e** [**Password per**](connectionoptions-password.md) un account di dominio quando si usa l'autenticazione [*Negotiate*](windows-remote-management-glossary.md) o *Kerberos* o per un account locale con autenticazione [*di*](windows-remote-management-glossary.md) base. Per connettersi a un account locale, i flag [**WSMan.CreateSession**](wsman-createsession.md) devono contenere la combinazione del flag **WSManFlagUseBasic** e del flag **WsmanFlagCredUserNamePassword.** Per connettersi a un account di dominio, i flag **WSMan.CreateSession** devono contenere la combinazione del flag **WSManFlagUseNegotiate** e del flag **WsmanFlagCredUserNamePassword** o della combinazione del flag **WSManFlagUseKerberos** e del flag **WsmanFlagCredUserNamePassword.** Per un account di dominio, **UserName** deve essere specificato nel formato "nome utente computer", dove la parte "computer" della stringa può essere il nome o \\ l'indirizzo IP. Per altre informazioni, vedere [Autenticazione per connessioni remote.](authentication-for-remote-connections.md)


```VB
Set ConnectionOptions = Wsman.CreateConnectionOptions
ConnectionOptions.Username = "MyUserName"
ConnectionOptions.Password = "MyPassword"
Set NewSession = Wsman.CreateSession("127.0.51.1", _
  (WSMan.SessionFlagUseBasic Or _
  WSMan.SessionFlagCredUsernamePassword), ConnectionOptions)
```



Per la connessione a un account di dominio, i flag [**WSMan.CreateSession**](wsman-createsession.md) devono contenere la combinazione del flag **WSManFlagUseNegotiate** e del flag **WsmanFlagCredUserNamePassword** per la connessione a un account di dominio, che richiede l'autenticazione Negotiate.


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Connectionoptions**](connectionoptions.md)
</dt> </dl>

 

 





