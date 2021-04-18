---
description: La tabella ServiceInstall viene utilizzata per installare un servizio e include le colonne seguenti.
ms.assetid: 81688d31-e560-4dd0-8d84-efb50206c76e
title: Tabella ServiceInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502583802a26c10bfd9572375149720c7c597f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314202"
---
# <a name="serviceinstall-table"></a>Tabella ServiceInstall

La tabella ServiceInstall viene utilizzata per installare un servizio e include le colonne seguenti.



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

Questa colonna è la stringa che fornisce il nome del servizio da installare. La lunghezza della stringa è massima di 256 caratteri. Il database di gestione controllo servizi conserva il caso dei caratteri nel nome del servizio, ma i confronti dei nomi di servizio non fanno distinzione tra maiuscole e minuscole. La barra (/) e la barra rovesciata ( \\ ) non sono caratteri validi per il nome del servizio.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName
</dt> <dd>

Questa colonna è la stringa localizzabile usata dai programmi dell'interfaccia utente per identificare il servizio. La lunghezza della stringa è massima di 256 caratteri. Gestione controllo servizi conserva il caso del nome visualizzato, ma i confronti dei nomi visualizzati non fanno distinzione tra maiuscole e minuscole.

</dd> <dt>

<span id="ServiceType"></span><span id="servicetype"></span><span id="SERVICETYPE"></span>ServiceType
</dt> <dd>

Questa colonna è un set di flag di bit che specificano il tipo di servizio. In questa colonna è necessario specificare uno dei seguenti tipi di servizi.



| Tipo di servizio                | Valore      | Descrizione                                                                                                                                                                                                                  |
|--------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ Processo personalizzato Win32 del servizio \_   | 0x00000010 | Un servizio Microsoft Win32 che esegue il proprio processo.                                                                                                                                                                         |
| \_Processo di \_ condivisione \_ Win32 del servizio | 0x00000020 | Un servizio Win32 che condivide un processo.                                                                                                                                                                                       |
| \_processo interattivo \_ servizio  | 0x00000100 | Un servizio Win32 che interagisce con il desktop. Questo valore non può essere usato da solo e deve essere aggiunto a uno dei due tipi precedenti. Quando si utilizza questo flag, è necessario impostare la colonna StartName su LocalSystem o null.<br/> |



 

I tipi di servizio seguenti non sono supportati.



| Tipo di servizio               | Valore      | Descrizione                   |
|-------------------------------|------------|-------------------------------|
| \_driver del kernel del servizio \_       | 0x00000001 | Un servizio driver.             |
| \_driver del file \_ System \_ di servizio | 0x00000002 | Servizio file system driver. |



 

</dd> <dt>

<span id="StartType"></span><span id="starttype"></span><span id="STARTTYPE"></span>StartType
</dt> <dd>

Questa colonna è un set di flag di bit che specificano quando avviare il servizio. In questa colonna è necessario specificare uno dei seguenti tipi di avvio del servizio.



| Tipo di avvio del servizio  | Valore      | Descrizione                                                                                                |
|------------------------|------------|------------------------------------------------------------------------------------------------------------|
| \_avvio automatico \_ servizio   | 0x00000002 | Un servizio viene avviato durante l'avvio del sistema.                                                              |
| \_avvio richiesta di servizio \_ | 0x00000003 | Un servizio viene avviato quando Gestione controllo servizi chiama la funzione [**StartService**](/windows/win32/api/winsvc/nf-winsvc-startservicea) . |
| SERVIZIO \_ disabilitato      | 0x00000004 | Specifica un servizio che non può più essere avviato.                                                         |



 

Il Windows Installer non può utilizzare le opzioni avvio del servizio e avvio del \_ \_ sistema del servizio \_ \_ .

</dd> <dt>

<span id="ErrorControl"></span><span id="errorcontrol"></span><span id="ERRORCONTROL"></span>ErrorControl
</dt> <dd>

Questa colonna specifica l'azione eseguita dal programma di avvio se il servizio non viene avviato durante l'avvio. Questi valori influiscono sugli eventi StartService di ServiceControl per i servizi installati. In questa colonna è necessario specificare uno dei seguenti flag di controllo degli errori.

L'aggiunta della costante **msidbServiceInstallErrorControlVital** (value = 0x08000) ai flag nella tabella seguente specifica che l'installazione complessiva avrà esito negativo se il servizio non può essere installato nel sistema.



| Flag di controllo degli errori       | Valore      | Azione del programma di avvio                                                                                                                                                                       |
|--------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Ignora errore \_ servizio   | 0x00000000 | Registra l'errore e continua con l'operazione di avvio.                                                                                                                                       |
| errore del servizio- \_ \_ normale   | 0x00000001 | Registra l'errore, Visualizza una finestra di messaggio e continua l'operazione di avvio.                                                                                                                    |
| errore del servizio \_ \_ critico | 0x00000003 | Registra l'errore, se possibile, e il sistema viene riavviato con l'ultima configurazione nota come corretta. Se è in corso l'avvio della configurazione Last-know-valido, l'operazione di avvio non riesce. |



 

</dd> <dt>

<span id="LoadOrderGroup"></span><span id="loadordergroup"></span><span id="LOADORDERGROUP"></span>LoadOrderGroup
</dt> <dd>

Questa colonna contiene la stringa che assegna un nome al gruppo di ordini di carico di cui questo servizio è membro. Specificare una stringa null o vuota se il servizio non appartiene a un gruppo.

</dd> <dt>

<span id="Dependencies"></span><span id="dependencies"></span><span id="DEPENDENCIES"></span>Dipendenze
</dt> <dd>

Questa colonna è un elenco di nomi di servizi o di gruppi di ordini di caricamento che il sistema deve avviare prima del servizio. Separare i nomi nell'elenco in base ai valori null. Se il servizio non ha dipendenze, specificare una stringa null o vuota. Utilizzare la sintassi \[ ~ \] per inserire un valore null. La dipendenza da un gruppo significa che questo servizio può essere eseguito se almeno un membro del gruppo è in esecuzione dopo un tentativo di avviare tutti i membri del gruppo.

Per richiedere, ad esempio, che il sistema avvii Service1 e Service2, prima di avviare il servizio elencato nella colonna ServiceInstall, immettere Service1 \[ ~ \] Service2 \[ ~ \] \[ ~ \] nella colonna dipendenze. Gli identificatori Service1 e Service2 devono essere presenti nella chiave primaria della tabella o corrispondere al nome del servizio già installato.

È necessario anteporre i nomi dei gruppi a + in modo che possano essere distinti da un nome di servizio. Per richiedere che il sistema avvii Service1 e almeno un membro del gruppo di ordini gruppo prima di avviare il servizio elencato nella colonna ServiceInstall, immettere Service1 \[ ~ \] + gruppo \[ ~ \] \[ ~ \] .

</dd> <dt>

<span id="StartName"></span><span id="startname"></span><span id="STARTNAME"></span>StartName
</dt> <dd>

Il servizio è connesso come nome fornito dalla stringa in questa colonna. Se il tipo di servizio è \_ \_ un processo personalizzato di Win32 del servizio, \_ usare un nome di account nel formato: NomeDominio \\ nome utente. Se l'account appartiene al dominio predefinito, è consentito specificarlo. \\ Nome utente. È necessario usare l'account LocalSystem se il tipo di servizio è il \_ processo di condivisione Win32 del servizio \_ o il \_ \_ \_ processo interattivo del servizio. La funzione [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) utilizza l'account LocalSystem se StartName viene specificato come null e la maggior parte dei servizi lascia la colonna vuota.

</dd> <dt>

<span id="Password"></span><span id="password"></span><span id="PASSWORD"></span>Password
</dt> <dd>

Questa stringa è la password per il nome dell'account specificato nella colonna StartName. Si noti che l'utente deve disporre delle autorizzazioni per accedere come servizio. Il servizio non dispone di password se StartName è null o una stringa vuota. Il valore iniziale di LocalSystem è null e pertanto la password in questa istanza è null, quindi la maggior parte dei servizi lascia vuota questa colonna.

Si noti che dopo l'eliminazione di un servizio che è stato installato con un nome utente e una password, il programma di installazione non è in grado di eseguire il rollback del servizio senza prima usare un'azione personalizzata per ottenere la password. Il programma di installazione può acquisire tutte le informazioni necessarie sul servizio ad eccezione della password, archiviata in una parte protetta del sistema. L'azione personalizzata acquisisce la password richiedendo all'utente, leggendo una proprietà dal database o leggendo un file. L'azione personalizzata deve quindi chiamare [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)per fornire la password, prima di reinstallare il servizio.

Windows Installer non scrive il valore immesso nel campo della password nel file di log.

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argomenti
</dt> <dd>

Questa colonna contiene gli argomenti della riga di comando o le proprietà necessarie per eseguire il servizio.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna per la colonna uno della [tabella dei componenti](component-table.md). Si noti che per installare questo servizio usando la tabella InstallService, il percorso di un elemento di questo componente deve essere il file eseguibile per il servizio.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Questa colonna contiene una Descrizione localizzabile per il servizio in corso di configurazione. Se questa colonna viene lasciata vuota, il programma di installazione utilizzerà la descrizione esistente del servizio, se disponibile. Per ulteriori informazioni, vedere \_ la descrizione del servizio in Microsoft Windows Software Development Kit (SDK). Per cancellare una descrizione esistente, immettere " \[ ~ \] " in questa colonna. In questo modo si ottiene una descrizione vuota per un servizio nuovo o esistente.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'azione [InstallServices](installservices-action.md) nelle [*tabelle Sequence*](s-gly.md) elabora le informazioni contenute in questa tabella. Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

Questa tabella contiene la maggior parte dei parametri per la funzione Win32 [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) .

Sebbene sia possibile usare l'interfaccia utente per specificare che un servizio deve essere installato come origine, il programma di installazione non supporta effettivamente questo tipo di installazione. È necessario installare i servizi eseguiti con il livello di privilegio del sistema locale per l'esecuzione dal disco rigido locale. Evitare di installare servizi che impersonano i privilegi di un determinato utente, perché possono scrivere dati di sicurezza in un log o nel registro di sistema. Questo può creare potenzialmente un problema di sicurezza, un conflitto di password o la perdita di dati di configurazione quando il sistema viene riavviato.

Per eliminare un servizio durante una disinstallazione, è necessario che sia presente un record corrispondente per il servizio nella [tabella ServiceControl](servicecontrol-table.md) e che il flag **msidbServiceControlEventUninstallDelete** venga visualizzato nella colonna evento. Il programma di installazione non elimina un servizio nella tabella ServiceInstall durante la disinstallazione senza questa voce nella tabella ServiceControl.

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

 

 
