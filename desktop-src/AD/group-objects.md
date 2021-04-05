---
title: Oggetti gruppo
description: Un gruppo è rappresentato come oggetto gruppo in Active Directory Domain Services.
ms.assetid: 2dd5a293-047a-4639-9c95-7074578952be
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a935d2a44d3350d8c24ca3bdb388f0a4bd8f16ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956323"
---
# <a name="group-objects"></a>Oggetti gruppo

Un gruppo è rappresentato come oggetto [**gruppo**](/windows/desktop/ADSchema/c-group) in Active Directory Domain Services. Nella tabella seguente sono elencati gli attributi importanti dell'oggetto **gruppo** .



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
<td>Il <strong>CN</strong> (o nome comune) è un attributo a valore singolo che corrisponde al nome distinto relativo dell'oggetto. <strong>CN</strong> è il nome del gruppo in Active Directory Domain Services. Come per tutti gli altri oggetti, il <strong>CN</strong> di un gruppo deve essere univoco tra gli oggetti di pari livello del contenitore che contiene il gruppo.<br/></td>
</tr>
<tr class="even">
<td><strong>membro</strong></td>
<td>L'attributo <strong>member</strong> è un attributo multivalore che contiene l'elenco di nomi distinti per gli oggetti utente, gruppo e contatto membri del gruppo. Ogni elemento nell'elenco è un riferimento collegato all'oggetto che rappresenta il membro. Pertanto, il server di Active Directory aggiorna automaticamente i nomi distinti nella proprietà del membro quando un oggetto membro viene spostato o rinominato.<br/></td>
</tr>
<tr class="odd">
<td><strong>groupType</strong></td>
<td>L'attributo <strong>GroupType</strong> è un attributo a valore singolo che è un numero intero che specifica il tipo di gruppo e l'ambito usando i flag di bit seguenti:
<ul>
<li><strong>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_GLOBAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_UNIVERSAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong></li>
</ul>
<br/> I primi tre flag specificano l'ambito del gruppo. Il flag di <strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong> indica il tipo di gruppo. Se questo flag è impostato, il gruppo è un gruppo di sicurezza. Se questo flag non è impostato, il gruppo è un gruppo di distribuzione. Per ulteriori informazioni, vedere <a href="#group-types">tipi di gruppo</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>memberOf</strong></td>
<td>L'attributo <strong>membro</strong> è un attributo a più valori che contiene l'elenco di nomi distinti per i gruppi che contengono il gruppo come membro. Questo attributo elenca i gruppi sotto i quali il gruppo è direttamente annidato e non contiene l'elenco ricorsivo dei predecessori annidati. Ad esempio, se il gruppo D è annidato nel gruppo C e il gruppo B e il gruppo B sono annidati nel gruppo A, l'attributo <strong>membro</strong> del gruppo d elenca il gruppo c e il gruppo b, ma non il gruppo a.<br/></td>
</tr>
<tr class="odd">
<td><strong>objectGUID</strong></td>
<td>L'attributo <strong>objectGUID</strong> è un attributo a valore singolo che rappresenta l'identificatore univoco per l'oggetto. Questo attributo è un identificatore univoco globale (GUID). Quando un oggetto viene creato nella directory, il server di Active Directory genera un GUID e lo assegna all'attributo <strong>objectGUID</strong> dell'oggetto. Il GUID è univoco nell'azienda e in qualsiasi altra posizione.<br/> <strong>ObjectGUID</strong> è una struttura GUID a 128 bit archiviata come OctetString.<br/></td>
</tr>
<tr class="even">
<td><strong>objectSid</strong></td>
<td>L'attributo <strong>objectSID</strong> è un attributo a valore singolo che specifica l'ID di sicurezza (SID) del gruppo. Il SID è un valore univoco utilizzato per identificare il gruppo come entità di sicurezza. Si tratta di un valore binario impostato dal sistema quando viene creato il gruppo.<br/> Ogni gruppo dispone di un SID univoco che il dominio del server Windows NT/Windows 2000 rilascia che è archiviato nell'attributo <strong>objectSID</strong> dell'oggetto gruppo nella directory. Ogni volta che un utente esegue l'accesso, il sistema Recupera il SID per i gruppi di cui l'utente è membro e lo inserisce nel token di accesso dell'utente. Il sistema usa i SID nel token di accesso dell'utente per identificare l'utente e le appartenenze ai gruppi in tutte le interazioni successive con la sicurezza di Windows NT/Windows 2000.<br/> Quando un SID è stato usato come identificatore univoco per un utente o un gruppo, non può mai essere usato di nuovo per identificare un altro utente o gruppo.<br/></td>
</tr>
<tr class="odd">
<td><strong>sAMAccountName</strong></td>
<td>L'attributo <strong>sAMAccountName</strong> è un attributo a valore singolo che rappresenta il nome di accesso utilizzato per supportare client e server di una versione precedente (Windows 95, Windows 98 e LAN Manager). Il valore di <strong>sAMAccountName</strong> deve essere composto da meno di 20 caratteri per supportare client e server di una versione precedente.<br/> <strong>SAMAccountName</strong> deve essere univoco tra tutti gli oggetti entità di sicurezza all'interno di un dominio.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="group-types"></a>Tipi di gruppo

Esistono due tipi di gruppi definiti da Active Directory Domain Services, *gruppi di sicurezza* e *gruppi di distribuzione*.

Un gruppo di sicurezza fornisce un raggruppamento logico di oggetti e il gruppo stesso può essere utilizzato come entità di sicurezza in un elenco di controllo di accesso (ACL). Quando a un gruppo di sicurezza viene concesso l'accesso a un oggetto, tutti i membri del gruppo di sicurezza ricevono automaticamente lo stesso accesso all'oggetto. I gruppi di sicurezza con ambito universale possono anche essere usati come entità di posta elettronica. Inviando un messaggio di posta elettronica a un gruppo di protezione universale, il messaggio viene inviato a tutti i membri del gruppo.

Un gruppo di distribuzione fornisce anche un raggruppamento logico di oggetti, ma non è in grado di fornire privilegi di accesso. I gruppi di distribuzione non sono abilitati per la sicurezza e non possono essere utilizzati come entità di sicurezza in un ACL. I gruppi di distribuzione vengono utilizzati solo a scopo di raggruppamento. Gli elenchi di distribuzione, ad esempio, possono essere usati con le applicazioni di posta elettronica, ad esempio Exchange, per inviare messaggi di posta elettronica a una raccolta di utenti.

Per ulteriori informazioni sui tipi di gruppo in Active Directory Domain Services, vedere l'argomento [tipi di gruppo](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) in [Microsoft TechNet](https://technet.microsoft.com/default.aspx).

## <a name="group-scope"></a>Ambito gruppo

Sono disponibili tre ambiti di gruppo definiti da Active Directory Domain Services, *universale*, *globale* e *locale di dominio*. L'ambito del gruppo definisce i tipi di oggetto che possono appartenere al gruppo, i tipi di gruppi di cui il gruppo può essere membro e l'ambito degli oggetti a cui è possibile assegnare l'accesso ai gruppi di sicurezza. Quando il livello di funzionalità del dominio è impostato sulla modalità mista di Windows 2000, non è possibile creare gruppi di sicurezza con ambito universale.

Nella tabella seguente sono elencati i tre ambiti di gruppo e altre informazioni su ogni ambito per un gruppo di sicurezza.

| Ambito                   | Membri possibili                                                                                                                                                                                                                                      | Conversione dell'ambito                                                                                                                                                 | Può concedere le autorizzazioni                                                       | Membro possibile di                                                                                                                                                                                                  |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Universale<br/>    | Account di qualsiasi dominio nella stessa foresta.<br/> Gruppi globali di qualsiasi dominio nella stessa foresta.<br/> Altri gruppi universali di qualsiasi dominio nella stessa foresta.<br/>                                                            | Può essere convertito nell'ambito locale di dominio.<br/> Può essere convertito in ambito globale, purché il gruppo non contenga altri gruppi universali.<br/> | In qualsiasi dominio nella stessa foresta o nelle foreste trusting.<br/>            | Altri gruppi universali nella stessa foresta.<br/> Gruppi locali di dominio nella stessa foresta o foreste trusting.<br/> Gruppi locali nei computer nella stessa foresta o nelle foreste trusting.<br/>            |
| Globale<br/>       | Account dello stesso dominio.<br/> Altri gruppi globali dallo stesso dominio.<br/>                                                                                                                                                        | Può essere convertito in ambito universale, purché il gruppo non sia membro di un altro gruppo globale.<br/>                                                   | In qualsiasi dominio nella stessa foresta o in domini o foreste trusting.<br/> | Gruppi universali di qualsiasi dominio nella stessa foresta.<br/> Altri gruppi globali dallo stesso dominio.<br/> Gruppi locali di dominio da qualsiasi dominio nella stessa foresta o da qualsiasi dominio trusting.<br/> |
| Dominio locale<br/> | Account di qualsiasi dominio o dominio trusted.<br/> Gruppi globali da qualsiasi dominio o da un dominio trusted.<br/> Gruppi universali di qualsiasi dominio nella stessa foresta.<br/> Altri gruppi locali di dominio dello stesso dominio.<br/> | Può essere convertito in ambito universale, purché il gruppo non contenga altri gruppi locali di dominio.<br/>                                              | All'interno dello stesso dominio.<br/>                                          | Altri gruppi locali di dominio dello stesso dominio.<br/> Gruppi locali nei computer nello stesso dominio, esclusi i gruppi predefiniti con SID noti.<br/>                                             |



 

 

