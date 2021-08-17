---
title: Schtasks.exe
description: Consente a un amministratore di creare, eliminare, eseguire query, modificare, eseguire e terminare le attività pianificate in un computer locale o remoto.
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe Utilità di pianificazione
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 0da33bf63d999ddad42f58dfa15a1c36571a664855ac20e48ef43bfd7aecd55b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139384"
---
# <a name="schtasksexe"></a>Schtasks.exe

Consente a un amministratore di creare, eliminare, eseguire query, modificare, eseguire e terminare le attività pianificate in un computer locale o remoto. Se Schtasks.exe senza argomenti, vengono visualizzati lo stato e la successiva esecuzione per ogni attività registrata. 

Per altre informazioni sui Utilità di pianificazione, vedere questa introduzione: Utilità di pianificazione [per sviluppatori](task-scheduler-start-page.md).

## <a name="creating-a-task"></a>Creazione di un'attività

La sintassi seguente viene utilizzata per creare un'attività nel computer locale o remoto.

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

### <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**Sistema /S** 
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il parametro di sistema viene impostato sul computer locale per impostazione predefinita.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**
</dt> <dd>

Valore che specifica il contesto utente in cui deve Schtasks.exe esecuzione.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per un determinato contesto utente. Se omesso, Schtasks.exe l'input dell'utente.

</dd> <dt>

<span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/RU** **username**
</dt> <dd>

Valore che specifica il contesto utente in cui viene eseguita l'attività. Per l'account di sistema, i valori validi sono "", "NT AUTHORITY \\ SYSTEM" o "SYSTEM". Per Utilità di pianificazione 2.0, anche "NT AUTHORITY \\ LOCALSERVICE" e "NT AUTHORITY \\ NETWORKSERVICE" sono valori validi.

</dd> <dt>

<span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**/RP** **\[ \] password**
</dt> <dd>

Valore che specifica la password per l'utente specificato con il parametro /RU. Per richiedere la password, il valore deve essere " \* " o nessun valore. Questa password viene ignorata per l'account di sistema. Questo parametro deve essere combinato con l'opzione /RU o /XML.

</dd> <dt>

<span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**Pianificazione /SC** 
</dt> <dd>

Valore che specifica la frequenza di pianificazione. I valori validi sono: MINUTE, HOURLY, DAILY, WEEKLY, MONTHLY, ONCE, ONLOGON, ONIDLE e ONEVENT.

</dd> <dt>

<span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**Modificatore /MO** 
</dt> <dd>

Valore che affina il tipo di pianificazione per consentire un controllo più accurato sulla ricorrenza della pianificazione. I valori validi sono:

-   MINUTO: da 1 a 1439 minuti.
-   ORARIA: da 1 a 23 ore.
-   GIORNALIERO: da 1 a 365 giorni.
-   WEEKLY: settimane da 1 a 52.
-   ONCE: nessun modificatore.
-   ONSTART: nessun modificatore.
-   ONLOGON: nessun modificatore.
-   ONIDLE: nessun modificatore.
-   MONTHLY: 1 - 12 oppure FIRST, SECOND, THIRD, FOURTH, LAST e LASTDAY.
-   ONEVENT: stringa di query dell'evento XPath.

</dd> <dt>

<span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **giorni**
</dt> <dd>

Valore che specifica il giorno della settimana in cui eseguire l'attività. I valori validi sono: MON, TUE, WED, THU, FRI, SAT, SUN e per le pianificazioni MENSILI da 1 a 31 (giorni del mese). Il carattere jolly ( \* ) specifica tutti i giorni.

</dd> <dt>

<span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **mesi**
</dt> <dd>

Valore che specifica i mesi dell'anno. Il valore predefinito è il primo giorno del mese. I valori validi sono: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV e DEC. Il carattere jolly ( \* ) specifica tutti i mesi.

</dd> <dt>

<span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**
</dt> <dd>

Valore che specifica la quantità di tempo di inattività da attendere prima di eseguire un'attività ONIDLE pianificata. L'intervallo valido è compreso tra 1 e 999 minuti.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nome attività**
</dt> <dd>

Valore che specifica un nome che identifica in modo univoco l'attività pianificata.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**
</dt> <dd>

Valore che specifica il percorso e il nome file dell'attività da eseguire all'ora pianificata. Ad esempio: C: \\ Windows \\ System32 \\calc.exe.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**
</dt> <dd>

Valore che specifica l'ora di inizio per l'esecuzione dell'attività. Il formato dell'ora è HH:mm (24 ore). Ad esempio, 14:30 specifica le 14:30. Il valore predefinito è l'ora corrente in cui /ST non è specificato. Questa opzione è obbligatoria con l'argomento /SC ONCE.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/RI** **interval**
</dt> <dd>

Valore che specifica l'intervallo di ripetizione in minuti. Non è applicabile per i tipi di pianificazione seguenti: MINUTE, HOURLY, ONSTART, ONLOGON, ONIDLE e ONEVENT. L'intervallo valido è compreso tra 1 e 599940 minuti. Se vengono specificati i parametri /ET o /DU, il valore predefinito è 10 minuti.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**
</dt> <dd>

Valore che specifica l'ora di fine per l'esecuzione dell'attività. Il formato dell'ora è HH:mm (24 ore). Ad esempio, 14:50 specifica 14:50PM. Non è applicabile per i tipi di pianificazione seguenti: ONSTART, ONLOGON, ONIDLE e ONEVENT.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**
</dt> <dd>

Valore che specifica la durata dell'esecuzione dell'attività. Il formato dell'ora è HH:mm (24 ore). Ad esempio, 14:50 specifica 14:50PM. Non è applicabile con /ET e per i tipi di pianificazione seguenti: ONSTART, ONLOGON, ONIDLE e ONEVENT. Per le attività /V1 (Utilità di pianificazione 1.0), se si specifica /RI, la durata predefinita è un'ora.

**Windows XP:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/k** 
</dt> <dd>

Valore che termina l'attività all'ora di fine o alla durata. Non è applicabile per i tipi di pianificazione seguenti: ONSTART, ONLOGON, ONIDLE e ONEVENT. È necessario specificare /ET o /DU.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**
</dt> <dd>

Valore che specifica la prima data in cui eseguire l'attività. Il formato è mm/gg/aaaa. Il valore predefinito è la data corrente. Non è applicabile per i tipi di pianificazione seguenti: ONCE, ONSTART, ONLOGON, ONIDLE e ONEVENT.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**
</dt> <dd>

Valore che specifica l'ultima data in cui verrà eseguita l'attività. Il formato è mm/gg/aaaa. Non è applicabile per i tipi di pianificazione seguenti: ONCE, ONSTART, ONLOGON, ONIDLE e ONEVENT.

</dd> <dt>

<span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**
</dt> <dd>

Valore che specifica il canale eventi per i trigger ONEVENT.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Valore che consente l'esecuzione interattiva dell'attività solo se l'utente /RU è attualmente connesso al momento dell'esecuzione dell'attività. L'attività viene eseguita solo se l'utente è connesso.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_NP_"></span><span id="_np_"></span>**/NP** 
</dt> <dd>

Valore che indica che non è archiviata alcuna password. L'attività non viene eseguita in modo interattivo come utente specificato. Sono disponibili solo risorse locali.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/Z** 
</dt> <dd>

Valore che contrassegna l'attività da eliminare dopo l'esecuzione finale.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**
</dt> <dd>

Valore che crea un'attività da un file XML. Questo parametro può essere combinato con le opzioni /RU e /RP oppure con l'opzione /RP solo quando il codice XML dell'attività contiene già l'entità.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_V1_"></span><span id="_v1_"></span>**/V1** 
</dt> <dd>

Valore che crea un'attività visibile Windows 2000, Windows Server 2003 e Windows XP.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/f** 
</dt> <dd>

Valore che crea in modo forzato l'attività ed elimina gli avvisi se l'attività specificata esiste già.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**Livello /RL** 
</dt> <dd>

Valore che imposta il livello di esecuzione per l'attività. I valori validi sono LIMITED e HIGHEST. Il valore predefinito è LIMITED.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**
</dt> <dd>

Valore che specifica il tempo di attesa per ritardare l'attività dopo l'attivazione del trigger. Il formato dell'ora è mmmm:ss. Questa opzione è valida solo per i tipi di pianificazione ONSTART, ONLOGON e ONEVENT.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Valore che visualizza il messaggio della Guida per Schtasks.exe.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si crea un'attività in un computer remoto in esecuzione nel sistema operativo Windows XP, Windows Server 2003 o Windows 2000, usare l'opzione /V1.

Non è possibile creare un'attività remota Utilità di pianificazione 1.0 non interattiva (creare un'attività non usando l'opzione /IT e l'opzione /V1) se nel computer remoto è abilitata l'eccezione del firewall Condivisione file e stampanti e l'eccezione del firewall Gestione attività pianificate remote è disabilitata.

## <a name="deleting-a-task"></a>Eliminazione di un'attività

La sintassi seguente viene usata per eliminare una o più attività pianificate.

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

### <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**Sistema /S** 
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il parametro di sistema viene impostato sul computer locale per impostazione predefinita.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**
</dt> <dd>

Valore che specifica il contesto utente in cui Schtasks.exe deve essere eseguito.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per il contesto utente specificato. Se omesso, Schtasks.exe l'input dell'utente.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nome attività**
</dt> <dd>

Valore che specifica il nome dell'attività pianificata da eliminare. Il carattere jolly ( \* ) può essere usato per eliminare tutte le attività.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/f** 
</dt> <dd>

Valore che elimina in modo forzato l'attività ed elimina gli avvisi se l'attività specificata è in esecuzione.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valore che visualizza la Guida per Schtasks.exe.

</dd> </dl>

## <a name="running-a-task"></a>Esecuzione di un'attività

La sintassi seguente viene usata per eseguire immediatamente un'attività pianificata.

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**Sistema /S** 
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il parametro di sistema viene impostato sul computer locale per impostazione predefinita.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**
</dt> <dd>

Valore che specifica il contesto utente in cui Schtasks.exe deve essere eseguito.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per il contesto utente specificato. Se omesso, Schtasks.exe l'input dell'utente.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nome attività**
</dt> <dd>

Valore che specifica il nome dell'attività pianificata da eseguire.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valore che visualizza la Guida per Schtasks.exe.

</dd> </dl>

## <a name="ending-a-running-task"></a>Terminazione di un'attività in esecuzione

La sintassi seguente viene usata per arrestare un'attività pianificata in esecuzione.

> [!Note]  
> Per arrestare l'esecuzione di un'attività remota, verificare che nel computer remoto siano abilitate le eccezioni firewall Condivisione file e stampanti e Gestione attività pianificate remote.

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**Sistema /S** 
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il parametro di sistema viene impostato sul computer locale per impostazione predefinita.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**
</dt> <dd>

Valore che specifica il contesto utente in cui Schtasks.exe deve essere eseguito.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per il contesto utente specificato. Se omesso, Schtasks.exe l'input dell'utente.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nome attività**
</dt> <dd>

Valore che specifica il nome dell'attività pianificata da arrestare.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valore che visualizza la Guida per Schtasks.exe.

</dd> </dl>

## <a name="querying-for-task-information"></a>Esecuzione di query per ottenere informazioni sulle attività

La sintassi seguente viene utilizzata per visualizzare le attività pianificate dal computer locale o remoto.

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

### <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**Sistema /S** 
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il parametro di sistema viene impostato sul computer locale per impostazione predefinita.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**
</dt> <dd>

Valore che specifica il contesto utente in cui Schtasks.exe deve essere eseguito.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per il contesto utente specificato. Se omesso, Schtasks.exe l'input dell'utente.

</dd> <dt>

<span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**Formato /FO** 
</dt> <dd>

Valore che specifica il formato di output. I valori validi sono TABLE, LIST e CSV.

</dd> <dt>

<span id="_NH_"></span><span id="_nh_"></span>**/NH** 
</dt> <dd>

Valore che specifica che l'intestazione di colonna non deve essere visualizzata nell'output. Questa opzione è valida solo per i formati TABLE e CSV.

</dd> <dt>

<span id="_V_"></span><span id="_v_"></span>**/v** 
</dt> <dd>

Valore che visualizza l'output dettagliato dell'attività.

> [!Note]  
> Se un'attività è stata pianificata per l'esecuzione una sola volta, le informazioni sulla pianificazione visualizzate sono "I dati di pianificazione non sono disponibili in questo formato".

 

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nome attività**
</dt> <dd>

Valore che specifica il nome dell'attività per cui recuperare le informazioni. Se non viene specificato alcun nome di attività, verranno visualizzate le informazioni per tutte le attività.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_XML_"></span><span id="_xml_"></span>**/XML** 
</dt> <dd>

Valore utilizzato per visualizzare le definizioni di attività in formato XML.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valore utilizzato per visualizzare la Guida per Schtasks.exe.

</dd> </dl>

## <a name="changing-a-task"></a>Modifica di un'attività

La sintassi seguente viene usata per modificare la modalità di esecuzione del programma o per modificare l'account utente e la password usati da un'attività pianificata.

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

### <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**Sistema /S** 
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il valore predefinito del parametro di sistema è il computer locale.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**
</dt> <dd>

Valore che specifica il contesto utente in cui deve essere Schtasks.exe esecuzione.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per il contesto utente specificato. Se omesso, Schtasks.exe l'input dell'utente.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **nome attività**
</dt> <dd>

Valore che specifica l'attività pianificata da modificare.

</dd> <dt>

<span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/RU** **runasuser**
</dt> <dd>

Valore che modifica il nome utente (contesto utente) in cui verrà eseguita l'attività pianificata. Per l'account di sistema, i valori validi sono "", "NT AUTHORITY \\ SYSTEM" o "SYSTEM". Per Utilità di pianificazione 2.0, anche "NT AUTHORITY \\ LOCALSERVICE" e "NT AUTHORITY \\ NETWORKSERVICE" sono valori validi.

</dd> <dt>

<span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**
</dt> <dd>

Valore che specifica una nuova password per il contesto utente esistente o la password per un nuovo account utente. Questa password viene ignorata per l'account di sistema.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**
</dt> <dd>

Valore che specifica un nuovo programma che verrà eseguito dall'attività.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**
</dt> <dd>

Valore che specifica l'ora di inizio per l'esecuzione dell'attività. Il formato dell'ora è HH:mm (24 ore). Ad esempio, 14:30 specifica 2:30PM.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**Intervallo /RI** 
</dt> <dd>

Valore che specifica l'intervallo di ripetizione, in minuti. L'intervallo valido è compreso tra 1 e 599940 minuti.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**
</dt> <dd>

Valore che specifica l'ora di fine dell'attività. Il formato dell'ora è HH:mm (24 ore). Ad esempio, 14:50 specifica 2:50PM.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**
</dt> <dd>

Valore che specifica la durata di esecuzione dell'attività. Il formato dell'ora è HH:mm (24 ore). Ad esempio, 14:50 specifica 2:50PM. Questa operazione non è applicabile con il parametro /ET.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/k** 
</dt> <dd>

Valore che termina l'attività all'ora di fine o alla durata.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**
</dt> <dd>

Valore che specifica la prima data in cui eseguire l'attività. Il formato è mm/gg/aaa.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**
</dt> <dd>

Valore che specifica l'ultima data in cui verrà eseguita l'attività. Il formato è mm/gg/aaa.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Valore che consente l'esecuzione interattiva dell'attività solo se l'utente /RU è attualmente connesso al momento dell'esecuzione dell'attività. L'attività viene eseguita solo se l'utente è connesso.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**Livello /RL** 
</dt> <dd>

Valore che imposta il livello di esecuzione per l'attività. I valori validi sono LIMITED e HIGHEST.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE** 
</dt> <dd>

Valore che abilita l'attività pianificata. Un'attività abilitata può essere eseguita e un'attività disabilitata non può essere eseguita.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE** 
</dt> <dd>

Valore che disabilita l'esecuzione dell'attività pianificata.

> [!Note]  
> Se un'attività Utilità di pianificazione 1.0 remota è disabilitata da Schtasks.exe e nel computer remoto è abilitata l'eccezione firewall Condivisione file e stampanti e l'eccezione firewall Gestione attività pianificate remote è disabilitata, l'attività non verrà disabilitata quando viene letta da un'API Utilità di pianificazione 2.0.

 

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/Z** 
</dt> <dd>

Valore che contrassegna l'attività da eliminare dopo l'esecuzione finale.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**
</dt> <dd>

Valore che specifica il tempo di attesa per ritardare l'esecuzione dell'attività dopo l'attivazione del trigger. Il formato dell'ora è mmmm:ss. Questa opzione è valida solo per le attività con i tipi di pianificazione ONSTART, ONLOGON e ONEVENT.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Valore che visualizza il messaggio della Guida per Schtasks.exe.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |



 

 





