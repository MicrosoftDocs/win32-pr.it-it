---
title: Oggetti gruppo
description: Un gruppo è rappresentato come oggetto gruppo in Active Directory Domain Services.
ms.assetid: 2dd5a293-047a-4639-9c95-7074578952be
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9811a365f321a0fb81b770e87a0987bac4c52d7bc681c44c90c35cbd3e7a1d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188729"
---
# <a name="group-objects"></a>Oggetti gruppo

Un gruppo è rappresentato come oggetto [**gruppo**](/windows/desktop/ADSchema/c-group) in Active Directory Domain Services. Nella tabella seguente sono elencati gli attributi importanti **dell'oggetto** gruppo.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>cn</strong></td>
<td>Cn <strong></strong> (o Common-Name) è un attributo a valore singolo che rappresenta il nome distinto relativo dell'oggetto. Cn <strong>è</strong> il nome del gruppo in Active Directory Domain Services. Come per tutti gli altri oggetti, il <strong>cn</strong> di un gruppo deve essere univoco tra gli oggetti di pari livello nel contenitore che contiene il gruppo.<br/></td>
</tr>
<tr class="even">
<td><strong>Membro</strong></td>
<td><strong>L'attributo</strong> member è un attributo multivalore che contiene l'elenco di nomi distinti per gli oggetti utente, gruppo e contatto che sono membri del gruppo. Ogni elemento dell'elenco è un riferimento collegato all'oggetto che rappresenta il membro. Pertanto, il server Active Directory aggiorna automaticamente i nomi distinti nella proprietà del membro quando un oggetto membro viene spostato o rinominato.<br/></td>
</tr>
<tr class="odd">
<td><strong>groupType</strong></td>
<td><strong>L'attributo groupType</strong> è un attributo a valore singolo che è un intero che specifica il tipo di gruppo e l'ambito usando i flag di bit seguenti:
<ul>
<li><strong>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_GLOBAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_UNIVERSAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong></li>
</ul>
<br/> I primi tre flag specificano l'ambito del gruppo. Il <strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong> flag indica il tipo di gruppo. Se questo flag è impostato, il gruppo è un gruppo di sicurezza. Se questo flag non è impostato, il gruppo è un gruppo di distribuzione. Per altre informazioni, vedere <a href="#group-types">Tipi di gruppo.</a><br/></td>
</tr>
<tr class="even">
<td><strong>memberOf</strong></td>
<td><strong>L'attributo memberOf</strong> è un attributo a più valori che contiene l'elenco di nomi distinti per i gruppi che contengono il gruppo come membro. Questo attributo elenca i gruppi sotto i quali il gruppo è annidato direttamente e non contiene l'elenco ricorsivo di predecessori annidati. Ad esempio, se il gruppo D è annidato nel gruppo C e il gruppo B e il gruppo B sono annidati nel gruppo A, l'attributo <strong>memberOf</strong> del gruppo D elenca il gruppo C e il gruppo B, ma non il gruppo A.<br/></td>
</tr>
<tr class="odd">
<td><strong>objectGUID</strong></td>
<td><strong>L'attributo objectGUID</strong> è un attributo a valore singolo che rappresenta l'identificatore univoco per l'oggetto. Questo attributo è un identificatore univoco globale (GUID). Quando viene creato un oggetto nella directory, il server Active Directory genera un GUID e lo assegna <strong>all'attributo objectGUID</strong> dell'oggetto. Il GUID è univoco nell'organizzazione e in qualsiasi altro luogo.<br/> <strong>objectGUID è</strong> una struttura GUID a 128 bit archiviata come OctetString.<br/></td>
</tr>
<tr class="even">
<td><strong>objectSid</strong></td>
<td><strong>L'attributo objectSid</strong> è un attributo a valore singolo che specifica l'ID di sicurezza (SID) del gruppo. Il SID è un valore univoco usato per identificare il gruppo come entità di sicurezza. Si tratta di un valore binario impostato dal sistema quando viene creato il gruppo.<br/> Ogni gruppo ha un SID univoco per cui il dominio di Windows NT/Windows 2000 Server presenta problemi archiviati nell'attributo <strong>objectSid</strong> dell'oggetto gruppo nella directory. Ogni volta che un utente accede, il sistema recupera il SID per i gruppi di cui l'utente è membro e lo inserisce nel token di accesso dell'utente. Il sistema usa i SID nel token di accesso dell'utente per identificare l'utente e le relative appartenenze ai gruppi in tutte le interazioni successive con la sicurezza Windows NT/Windows 2000.<br/> Quando un SID è stato usato come identificatore univoco per un utente o un gruppo, non può essere usato di nuovo per identificare un altro utente o gruppo.<br/></td>
</tr>
<tr class="odd">
<td><strong>sAMAccountName</strong></td>
<td>L'attributo <strong>sAMAccountName</strong> è un attributo a valore singolo che rappresenta il nome di accesso usato per supportare client e server di una versione precedente (Windows 95, Windows 98 e LAN Manager). <strong>SAMAccountName deve</strong> contenere meno di 20 caratteri per supportare client e server di una versione precedente.<br/> <strong>SAMAccountName deve essere</strong> univoco tra tutti gli oggetti entità di sicurezza all'interno di un dominio.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="group-types"></a>Tipi di gruppo

Esistono due tipi di gruppi definiti da Active Directory Domain Services, gruppi *di sicurezza* e gruppi *di distribuzione.*

Un gruppo di sicurezza fornisce un raggruppamento logico di oggetti e il gruppo stesso può essere usato come entità di sicurezza in un elenco di controllo di accesso (ACL). Quando a un gruppo di sicurezza viene assegnato l'accesso a un oggetto, tutti i membri del gruppo di sicurezza ricevono automaticamente lo stesso accesso all'oggetto. I gruppi di sicurezza con ambito universale possono essere usati anche come entità di posta elettronica. L'invio di un messaggio di posta elettronica a un gruppo di sicurezza universale invia il messaggio a tutti i membri del gruppo.

Un gruppo di distribuzione fornisce anche un raggruppamento logico di oggetti, ma non può fornire privilegi di accesso. I gruppi di distribuzione non sono abilitati per la sicurezza e non possono essere usati come entità di sicurezza in un ACL. I gruppi di distribuzione vengono usati solo a scopo di raggruppamento. Ad esempio, le liste di distribuzione possono essere usate con applicazioni di posta elettronica, ad esempio Exchange, per inviare messaggi di posta elettronica a una raccolta di utenti.

Per altre informazioni sui tipi di gruppo in Active Directory Domain Services, vedere [l'argomento Tipi di](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) gruppo in Microsoft [TechNet.](https://technet.microsoft.com/default.aspx)

## <a name="group-scope"></a>Ambito gruppo

Esistono tre ambiti di gruppo definiti da Active Directory Domain Services, *universale,* *globale* *e locale di dominio.* L'ambito del gruppo definisce i tipi di oggetto che possono appartenere al gruppo, i tipi di gruppi di cui il gruppo può essere membro e l'ambito degli oggetti a cui i gruppi di sicurezza possono avere accesso. Quando il livello di funzionalità del dominio è impostato Windows modalità mista 2000, non è possibile creare gruppi di sicurezza con ambito universale.

Nella tabella seguente sono elencati i tre ambiti del gruppo e altre informazioni su ogni ambito per un gruppo di sicurezza.

| Ambito                   | Membri possibili                                                                                                                                                                                                                                      | Conversione dell'ambito                                                                                                                                                 | Può concedere le autorizzazioni                                                       | Possibile membro di                                                                                                                                                                                                  |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Universale<br/>    | Account di qualsiasi dominio nella stessa foresta.<br/> Gruppi globali da qualsiasi dominio nella stessa foresta.<br/> Altri gruppi universali da qualsiasi dominio nella stessa foresta.<br/>                                                            | Può essere convertito nell'ambito locale del dominio.<br/> Può essere convertito in ambito globale purché il gruppo non contenga altri gruppi universali.<br/> | In qualsiasi dominio nella stessa foresta o foresta trusting.<br/>            | Altri gruppi universali nella stessa foresta.<br/> Gruppi locali di dominio nella stessa foresta o foreste trusting.<br/> Gruppi locali in computer nella stessa foresta o foreste trusting.<br/>            |
| Globale<br/>       | Account dello stesso dominio.<br/> Altri gruppi globali dello stesso dominio.<br/>                                                                                                                                                        | Può essere convertito in ambito universale purché il gruppo non sia membro di qualsiasi altro gruppo globale.<br/>                                                   | In qualsiasi dominio nella stessa foresta o in domini o foreste trusting.<br/> | Gruppi universali da qualsiasi dominio nella stessa foresta.<br/> Altri gruppi globali dello stesso dominio.<br/> Gruppi locali di dominio da qualsiasi dominio nella stessa foresta o da qualsiasi dominio trusting.<br/> |
| Domain Local<br/> | Account di qualsiasi dominio o dominio trusted.<br/> Gruppi globali da qualsiasi dominio o dominio trusted.<br/> Gruppi universali da qualsiasi dominio nella stessa foresta.<br/> Altri gruppi locali di dominio dello stesso dominio.<br/> | Può essere convertito in ambito universale purché il gruppo non contenga altri gruppi locali di dominio.<br/>                                              | All'interno dello stesso dominio.<br/>                                          | Altri gruppi locali di dominio dello stesso dominio.<br/> Gruppi locali in computer nello stesso dominio, esclusi i gruppi predefiniti con SID noti.<br/>                                             |



 

 

