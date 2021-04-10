---
title: Metodo TaskService. Connect
description: Per lo scripting, si connette a un computer remoto e associa tutte le chiamate successive a questa interfaccia con una sessione remota.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Metodo Connect Utilità di pianificazione
- Metodo Connect Utilità di pianificazione, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, metodo Connect
topic_type:
- apiref
api_name:
- TaskService.Connect
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1db5f13e20da825cbdaf45ae399279687f6ff4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963983"
---
# <a name="taskserviceconnect-method"></a>Metodo TaskService. Connect

Per lo scripting, si connette a un computer remoto e associa tutte le chiamate successive a questa interfaccia con una sessione remota. Se il parametro serverName è vuoto, questo metodo verrà eseguito nel computer locale. Se l'ID utente non è specificato, viene utilizzato il token corrente.

## <a name="syntax"></a>Sintassi


```VB
TaskService.Connect( _
  [ ByVal serverName ], _
  [ ByVal user ], _
  [ ByVal domain ], _
  [ ByVal password ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nomeserver* \[ in, facoltativo\]
</dt> <dd>

Nome del computer a cui si desidera connettersi. Se il parametro serverName è vuoto, questo metodo verrà eseguito nel computer locale.

</dd> <dt>

*utente* \[ di in, facoltativo\]
</dt> <dd>

Nome utente utilizzato durante la connessione al computer. Se l'utente non è specificato, viene utilizzato il token corrente.

</dd> <dt>

*dominio* \[ in, facoltativo\]
</dt> <dd>

Dominio dell'utente specificato nel parametro *User* .

</dd> <dt>

*password* \[ di in, facoltativo\]
</dt> <dd>

Password utilizzata per la connessione al computer. Se il nome utente e la password non sono specificati, viene utilizzato il token corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Prima di chiamare uno degli altri metodi [**TaskService**](taskservice.md) , è necessario chiamare il metodo **TaskService. Connect** .

Se il metodo Connect ha esito negativo, è possibile raccogliere l'identificatore di errore per trovare il significato dell'errore. Nella tabella seguente sono elencati gli identificatori di errore e le relative descrizioni.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificatore errore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x80070005</td>
<td>Accesso negato per la connessione al servizio Utilità di pianificazione.</td>
</tr>
<tr class="even">
<td>0x80041315</td>
<td>Il servizio Utilità di pianificazione non è in esecuzione.</td>
</tr>
<tr class="odd">
<td>0x8007000e</td>
<td>L'applicazione non dispone di memoria sufficiente per completare l'operazione oppure l' <em>utente</em>, la <em>password</em>o il <em>dominio</em> ha almeno un valore null e un valore non null.</td>
</tr>
<tr class="even">
<td>53</td>
<td>Questo errore viene restituito nelle situazioni seguenti:
<ul>
<li>Il nome computer specificato nel parametro <em>ServerName</em> non esiste.</li>
<li>Quando si tenta di connettersi a un computer Windows Server 2003 o Windows XP e nel computer remoto non è abilitata l'eccezione del firewall condivisione file e stampanti oppure il servizio Registro di sistema remoto non è in esecuzione.</li>
<li>Quando si tenta di connettersi a un computer con Windows Vista e nel computer remoto non è abilitata l'eccezione del firewall Gestione attività pianificate remote e l'eccezione firewall condivisione file e stampanti è abilitata oppure il servizio Registro di sistema remoto non è in esecuzione.</li>
</ul></td>
</tr>
<tr class="odd">
<td>50</td>
<td>Impossibile specificare i parametri <em>User</em>, <em>password</em>o <em>Domain</em> quando ci si connette a un computer Windows XP o Windows Server 2003 remoto da un computer con Windows Vista.</td>
</tr>
</tbody>
</table>



 

Se ci si connette a un computer Windows Vista remoto da Windows Vista, è necessario consentire l'eccezione del firewall di gestione delle attività pianificate remote nel computer remoto. Per consentire questa eccezione, fare clic sul pulsante Start, pannello di controllo, sicurezza, consentire un programma tramite Windows Firewall, quindi selezionare la casella di controllo gestione remota attività pianificate. Fare quindi clic sul pulsante OK nella finestra di dialogo Impostazioni Windows Firewall.

Se ci si connette a un computer Windows XP o Windows Server 2003 remoto da un computer con Windows Vista, è necessario consentire l'eccezione del firewall per la condivisione di file e stampanti nel computer remoto. Per consentire questa eccezione, fare clic su Start, pannello di controllo, fare doppio clic su Windows Firewall, selezionare la scheda eccezioni, quindi selezionare l'eccezione firewall condivisione file e stampanti. Fare quindi clic sul pulsante OK nella finestra di dialogo Windows Firewall. Anche il servizio Registro di sistema remoto deve essere in esecuzione nel computer remoto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





