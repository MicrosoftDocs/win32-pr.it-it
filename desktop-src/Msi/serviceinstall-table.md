---
description: La tabella ServiceInstall viene usata per installare un servizio e include le colonne seguenti.
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: Tabella ServiceInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3850b957df4dd0af662354c14f82717e4b86ad597f151c6a45bb8dc1bebea5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039961"
---
# <a name="serviceinstall-table"></a>Tabella ServiceInstall

La tabella ServiceInstall viene usata per installare un servizio e include le colonne seguenti.



| Colonna         | Tipo                               | Chiave | Nullable |
|----------------|------------------------------------|-----|----------|
| ServiceInstall | [Identificatore](identifier.md)       | S   | N        |
| Nome           | [Formattato](formatted.md)         | N   | N        |
| DisplayName    | [Formattato](formatted.md)         | N   | S        |
| ServiceType    | [DoubleInteger](doubleinteger.md) | N   | N        |
| StartType      | [DoubleInteger](doubleinteger.md) | N   | N        |
| ErrorControl   | [DoubleInteger](doubleinteger.md) | N   | N        |
| LoadOrderGroup | [Formattato](formatted.md)         | N   | S        |
| Dependencies   | [Formattato](formatted.md)         | N   | S        |
| StartName      | [Formattato](formatted.md)         | N   | S        |
| Password       | [Formattato](formatted.md)         | N   | S        |
| Argomenti      | [Formattato](formatted.md)         | N   | S        |
| Componente\_    | [Identificatore](identifier.md)       | N   | N        |
| Descrizione    | [Formattato](formatted.md)         | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="ServiceInstall"></span><span id="serviceinstall"></span><span id="SERVICEINSTALL"></span>ServiceInstall
</dt> <dd>

Si tratta della chiave primaria per la tabella.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Questa colonna è la stringa che fornisce il nome del servizio da installare. La stringa ha una lunghezza massima di 256 caratteri. Il database di Gestione controllo servizi mantiene la distinzione tra maiuscole e minuscole dei caratteri nel nome del servizio, ma nei confronti dei nomi di servizio non viene fatto distinzione tra maiuscole e minuscole. La barra (/) e la barra rovesciata ( \\ ) sono caratteri del nome di servizio non validi.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>Displayname
</dt> <dd>

Questa colonna è la stringa localizzabile che i programmi dell'interfaccia utente usano per identificare il servizio. La stringa ha una lunghezza massima di 256 caratteri. Gestione controllo servizi mantiene la distinzione tra maiuscole e minuscole del nome visualizzato, ma i confronti tra nomi visualizzati non esentengono la distinzione tra maiuscole e minuscole.

</dd> <dt>

<span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>Servicetype
</dt> <dd>

Questa colonna è un set di flag di bit che specificano il tipo di servizio. In questa colonna è necessario specificare uno dei tipi di servizio seguenti.



| Tipo di servizio                | Valore      | Descrizione                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROCESSO \_ WIN32 \_ DEL \_ SERVIZIO   | 0x00000010 | Un servizio Microsoft Win32 che esegue il proprio processo.                                                                                                                                                                         |
| PROCESSO \_ DI CONDIVISIONE WIN32 \_ DEL \_ SERVIZIO | 0x00000020 | Servizio Win32 che condivide un processo.                                                                                                                                                                                       |
| PROCESSO \_ INTERATTIVO DEL \_ SERVIZIO  | 0x00000100 | Servizio Win32 che interagisce con il desktop. Questo valore non può essere usato da solo e deve essere aggiunto a uno dei due tipi precedenti. Quando si usa questo flag, la colonna StartName deve essere impostata su LocalSystem o null.<br/> |



 

I tipi di servizio seguenti non sono supportati.



| Tipo di servizio               | Valore      | Descrizione                   |
|-------------------------------|------------|-------------------------------|
| DRIVER \_ DEL KERNEL DEL \_ SERVIZIO       | 0x00000001 | Un servizio driver.             |
| \_DRIVER DEL FILE SYSTEM DEL \_ \_ SERVIZIO | 0x00000002 | Servizio file system driver. |



 

</dd> <dt>

<span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType
</dt> <dd>

Questa colonna è un set di flag di bit che specificano quando avviare il servizio. In questa colonna deve essere specificato uno dei tipi di avvio del servizio seguenti.



| Tipo di avvio del servizio  | Valore      | Descrizione                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| AVVIO \_ AUTOMATICO \_ DEL SERVIZIO   | 0x00000002 | Avvio del servizio durante l'avvio del sistema.                                                              |
| AVVIO \_ DELLA RICHIESTA DI \_ SERVIZIO | 0x00000003 | Un servizio viene avviato quando il gestore di controllo del servizio chiama la [**funzione StartService.**](/windows/win32/api/winsvc/nf-winsvc-startservicea) |
| SERVIZIO \_ DISABILITATO      | 0x00000004 | Specifica un servizio che non può più essere avviato.                                                         |



 

Il Windows non può usare le opzioni SERVICE \_ BOOT START e SERVICE SYSTEM \_ \_ \_ START.

</dd> <dt>

<span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl
</dt> <dd>

Questa colonna specifica l'azione eseguita dal programma di avvio se il servizio non viene avviato durante l'avvio. Questi valori influiscono sugli eventi ServiceControl StartService per i servizi installati. In questa colonna è necessario specificare uno dei flag di controllo degli errori seguenti.

L'aggiunta della costante **msidbServiceInstallErrorControlVital** (value = 0x08000) ai flag nella tabella seguente specifica che l'installazione complessiva deve non riuscire se il servizio non può essere installato nel sistema.



| Flag di controllo degli errori       | Valore      | Azione del programma di avvio                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ DEL \_ SERVIZIO IGNORA   | 0x00000000 | Registra l'errore e continua con l'operazione di avvio.                                                                                                                                       |
| ERRORE \_ DEL \_ SERVIZIO NORMALE   | 0x00000001 | Registra l'errore, visualizza una finestra di messaggio e continua l'operazione di avvio.                                                                                                                    |
| ERRORE \_ DEL \_ SERVIZIO CRITICO | 0x00000003 | Registra l'errore se possibile e il sistema viene riavviato con l'ultima configurazione nota come valida. Se viene avviata l'ultima configurazione valida nota, l'operazione di avvio ha esito negativo. |



 

</dd> <dt>

<span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup
</dt> <dd>

Questa colonna contiene la stringa che indica il nome del gruppo di ordinamento del carico di cui il servizio è membro. Specificare null o una stringa vuota se il servizio non appartiene a un gruppo.

</dd> <dt>

<span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Dipendenze
</dt> <dd>

Questa colonna è un elenco di nomi di servizi o gruppi di ordinamento del carico che il sistema deve avviare prima di questo servizio. Separare i nomi nell'elenco da Valori Null. Se il servizio non ha dipendenze, specificare Null o una stringa vuota. Usare la \[ ~ \] sintassi per inserire un valore Null. La dipendenza da un gruppo indica che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.

Ad esempio, per richiedere che il sistema avvia service1 e service2, prima di avviare il servizio elencato nella colonna ServiceInstall immettere service1 service2 nella \[ ~ \] \[ ~ \] \[ ~ \] colonna Dependencies. Gli identificatori service1 e service2 devono essere presenti nella chiave primaria della tabella o essere il nome del servizio già installato.

È necessario aggiungere un prefisso ai nomi dei gruppi con + in modo che possano essere distinti da un nome di servizio. Per richiedere che il sistema avvia service1 e almeno un membro del gruppo di ordinamento MyGroup prima di avviare il servizio elencato nella colonna ServiceInstall, immettere service1 \[ ~ \] +MyGroup \[ ~ \] \[ ~ \] .

</dd> <dt>

<span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName
</dt> <dd>

Il servizio è connesso come nome specificato dalla stringa in questa colonna. Se il tipo di servizio è SERVICE WIN32 OWN PROCESS, usare un \_ nome account nel \_ \_ formato: NomeDominioNomeUtente. \\ Se l'account appartiene al dominio predefinito, è consentito specificare . \\ Nome utente. L'account LocalSystem deve essere usato se il tipo di servizio è SERVICE \_ WIN32 \_ SHARE PROCESS o SERVICE INTERACTIVE \_ \_ \_ PROCESS. La [**funzione CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) usa l'account LocalSystem se StartName viene specificato come Null e la maggior parte dei servizi lascia vuota questa colonna.

</dd> <dt>

<span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>Password
</dt> <dd>

Questa stringa è la password per il nome dell'account specificato nella colonna StartName. Si noti che l'utente deve avere le autorizzazioni per accedere come servizio. Il servizio non ha password se StartName è Null o una stringa vuota. Startname di LocalSystem è Null e pertanto la password in questa istanza è Null, quindi la maggior parte dei servizi lascia vuota questa colonna.

Si noti che dopo aver eliminato un servizio installato con un nome utente e una password, il programma di installazione non può eseguire il rollback del servizio senza prima usare un'azione personalizzata per ottenere la password. Il programma di installazione può acquisire tutte le informazioni necessarie sul servizio, ad eccezione della password, archiviata in una parte protetta del sistema. L'azione personalizzata acquisisce la password richiedendo all'utente, leggendo una proprietà dal database o leggendo un file. L'azione personalizzata deve quindi chiamare [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)per fornire la password prima di reinstallare il servizio.

Windows Il programma di installazione non scrive il valore immesso nel campo Password nel file di log.

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argomenti
</dt> <dd>

Questa colonna contiene tutti gli argomenti o le proprietà della riga di comando necessari per eseguire il servizio.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna alla colonna uno della [tabella dei componenti](component-table.md). Si noti che per installare questo servizio usando la tabella InstallService, keyPath per questo componente deve essere il file eseguibile per il servizio.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Questa colonna contiene una descrizione localizzabile per il servizio da configurare. Se questa colonna viene lasciata vuota, il programma di installazione usa la descrizione esistente del servizio, se presente. Per altre informazioni, vedere SERVICE \_ DESCRIPTION in Microsoft Windows Software Development Kit (SDK). Per cancellare una descrizione esistente, immettere " \[ ~ \] " in questa colonna. Verrà restituita una descrizione vuota per un servizio nuovo o esistente.

</dd> </dl>

## <a name="remarks"></a>Commenti

[L'azione InstallServices](installservices-action.md) nelle [*tabelle di sequenza*](s-gly.md) elabora le informazioni in questa tabella. Per informazioni sull'uso *delle tabelle di sequenza,* vedere [Uso di una tabella di sequenza](using-a-sequence-table.md).

Questa tabella contiene la maggior parte dei parametri per la funzione [**Win32 CreateService.**](/windows/win32/api/winsvc/nf-winsvc-createservicea)

Anche se è possibile usare l'interfaccia utente per specificare che un servizio deve essere installato come run-from-source, il programma di installazione non supporta effettivamente questo tipo di installazione. I servizi eseguiti con il livello di privilegio del sistema locale devono essere installati per l'esecuzione dal disco rigido locale. Evitare l'installazione di servizi che rappresentano i privilegi di un determinato utente, perché ciò potrebbe scrivere dati di sicurezza in un log o nel Registro di sistema. Ciò può potenzialmente creare un problema di sicurezza, un conflitto di password o la perdita di dati di configurazione al riavvio del sistema.

Per eliminare un servizio durante una disinstallazione, deve essere presente un record corrispondente per il servizio nella tabella [ServiceControl](servicecontrol-table.md) e il flag **msidbServiceControlEventUninstallDelete** deve essere visualizzato nella colonna Event. Il programma di installazione non elimina un servizio nella tabella ServiceInstall durante la disinstallazione senza questa voce nella tabella ServiceControl.

Per informazioni su come proteggere un servizio, vedere la [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE66](ice66.md)  
[ICE69](ice69.md)  
</dl>

 

 
