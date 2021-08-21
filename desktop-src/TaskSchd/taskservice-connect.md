---
title: TaskService. Connessione metodo
description: Per lo scripting, si connette a un computer remoto e associa tutte le chiamate successive su questa interfaccia a una sessione remota.
ms.assetid: 206087df-307c-4ba9-9e83-915f5287f281
keywords:
- Connessione metodo Utilità di pianificazione
- Connessione metodo Utilità di pianificazione , oggetto TaskService
- Metodo taskService Utilità di pianificazione , Connessione taskservice
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
ms.openlocfilehash: d4da8fb2aed018eab9880ab6c8a6bed310e6d89bb293d52efc5d6ac6d8baf190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059739"
---
# <a name="taskserviceconnect-method"></a>TaskService. Connessione metodo

Per lo scripting, si connette a un computer remoto e associa tutte le chiamate successive su questa interfaccia a una sessione remota. Se il parametro serverName è vuoto, questo metodo verrà eseguito nel computer locale. Se l'id utente non è specificato, viene usato il token corrente.

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

*serverName* \[ in, facoltativo\]
</dt> <dd>

Nome del computer a cui si vuole connettersi. Se il parametro serverName è vuoto, questo metodo verrà eseguito nel computer locale.

</dd> <dt>

*user* \[ in, facoltativo\]
</dt> <dd>

Nome utente utilizzato durante la connessione al computer. Se l'utente non è specificato, viene usato il token corrente.

</dd> <dt>

*dominio* \[ in, facoltativo\]
</dt> <dd>

Dominio dell'utente specificato nel *parametro user.*

</dd> <dt>

*password* \[ in, facoltativo\]
</dt> <dd>

Password utilizzata per connettersi al computer. Se il nome utente e la password non sono specificati, viene usato il token corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il **metodo TaskService.Connessione** deve essere chiamato prima di chiamare qualsiasi altro [**metodo TaskService.**](taskservice.md)

Se il Connessione non riesce, è possibile raccogliere l'identificatore di errore per trovare il significato dell'errore. Nella tabella seguente sono elencati gli identificatori di errore e le relative descrizioni.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificatore dell'errore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x80070005</td>
<td>L'accesso viene negato per connettersi al Utilità di pianificazione servizio.</td>
</tr>
<tr class="even">
<td>0x80041315</td>
<td>Il Utilità di pianificazione non è in esecuzione.</td>
</tr>
<tr class="odd">
<td>0x8007000e</td>
<td>L'applicazione non dispone di memoria sufficiente per completare <em></em> l'operazione oppure l'utente, <em></em>la <em>password</em>o il dominio ha almeno un valore Null e un valore non Null.</td>
</tr>
<tr class="even">
<td>53</td>
<td>Questo errore viene restituito nelle situazioni seguenti:
<ul>
<li>Il nome computer specificato nel <em>parametro serverName</em> non esiste.</li>
<li>Quando si tenta di connettersi a un computer Windows Server 2003 o Windows XP e nel computer remoto non è abilitata l'eccezione firewall Condivisione file e stampanti o il servizio Registro di sistema remoto non è in esecuzione.</li>
<li>Quando si tenta di connettersi a un computer Windows Vista e nel computer remoto non è abilitata l'eccezione firewall Gestione attività pianificate remote e l'eccezione firewall Condivisione file e stampanti è abilitata oppure il servizio Registro di sistema remoto non è in esecuzione.</li>
</ul></td>
</tr>
<tr class="odd">
<td>50</td>
<td>I <em>parametri utente,</em> <em>password</em>o dominio non possono essere specificati durante la connessione a un computer Windows XP o Windows Server 2003 remoto da un computer Windows Vista. <em></em></td>
</tr>
</tbody>
</table>



 

Per connettersi a un computer Windows Vista remoto da un Windows Vista, è necessario consentire l'eccezione del firewall gestione attività pianificate remote nel computer remoto. Per consentire questa eccezione, fare clic su Avvia, Pannello di controllo, Sicurezza, Consenti un programma tramite firewall Windows e quindi selezionare la casella di controllo Gestione attività pianificate remote . Fare quindi clic sul pulsante OK nella finestra Windows firewall Impostazioni finestra di dialogo.

Se ci si connette a un computer Windows XP o Windows Server 2003 remoto da un computer Windows Vista, è necessario consentire l'eccezione del firewall condivisione file e stampanti nel computer remoto. Per consentire questa eccezione, fare clic su Start, Pannello di controllo, fare doppio clic su firewall Windows, selezionare la scheda Eccezioni e quindi selezionare l'eccezione firewall Condivisione file e stampanti. Fare quindi clic sul pulsante OK nella finestra Windows firewall. Anche il servizio Registro di sistema remoto deve essere in esecuzione nel computer remoto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





