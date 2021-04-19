---
title: Schtasks.exe
description: Consente a un amministratore di creare, eliminare, eseguire query, modificare, eseguire e terminare attività pianificate in un computer locale o remoto.
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
ms.openlocfilehash: 2a57ee4edae1cd1604f10a88f3fc8cf2ea0971fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326484"
---
# <a name="schtasksexe"></a>Schtasks.exe

Consente a un amministratore di creare, eliminare, eseguire query, modificare, eseguire e terminare attività pianificate in un computer locale o remoto. L'esecuzione di Schtasks.exe senza argomenti consente di visualizzare lo stato e la fase di esecuzione successiva per ogni attività registrata. 

Per ulteriori informazioni su Utilità di pianificazione, vedere questa introduzione: [utilità di pianificazione per sviluppatori](task-scheduler-start-page.md).

## <a name="creating-a-task"></a>Creazione di un'attività

La sintassi seguente consente di creare un'attività nel computer locale o remoto.

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il valore predefinito del parametro di sistema è il computer locale.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**
</dt> <dd>

Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per un contesto utente specificato. Se omesso, Schtasks.exe richiede l'input dell'utente.

</dd> <dt>

<span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span> **Nome utente** /ru
</dt> <dd>

Valore che specifica il contesto utente in cui viene eseguita l'attività. Per l'account di sistema, i valori validi sono "", "NT AUTHORITY \\ System" o "System". Per le attività Utilità di pianificazione 2,0, anche "NT AUTHORITY \\ LocalService" e "NT Authority \\ NetworkService" sono valori validi.

</dd> <dt>

<span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span> **\[ Password \]** /RP
</dt> <dd>

Valore che specifica la password per l'utente specificato con il parametro/RU. Per richiedere la password, il valore deve essere " \* " o nessun valore. Questa password viene ignorata per l'account di sistema. Questo parametro deve essere combinato con l'opzione/RU o/XML.

</dd> <dt>

<span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span> **Pianificazione** di/SC
</dt> <dd>

Valore che specifica la frequenza di pianificazione. I valori validi sono: minuti, orari, giornalieri, SETTIMANAli, MENSILi, una volta, in base al LOGO, OnIdle e OnEvent.

</dd> <dt>

<span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span> **Modificatore** /mo
</dt> <dd>

Valore che perfeziona il tipo di pianificazione per consentire un controllo più preciso sulla ricorrenza della pianificazione. I valori validi sono:

-   MINUTO: 1-1439 minuti.
-   OGNI ora: 1-23 ore.
-   OGNI giorno: 1-365 giorni.
-   SETTIMANALE: settimane 1-52.
-   ONCE: nessun modificatore.
-   OnStart: nessun modificatore.
-   ONLOGON: nessun modificatore.
-   OnIdle: nessun modificatore.
-   MENSILE: 1-12, o prima, seconda, terza, quarta, ultima e LASTDAY.
-   OnEvent: stringa di query dell'evento XPath.

</dd> <dt>

<span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **giorni**
</dt> <dd>

Valore che specifica il giorno della settimana in cui eseguire l'attività. I valori validi sono: MON, Mar, Mer, Gio, ven, SAT, SUN e per le pianificazioni MENSILi 1-31 (giorni del mese). Il carattere jolly ( \* ) specifica tutti i giorni.

</dd> <dt>

<span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **mesi**
</dt> <dd>

Valore che specifica i mesi dell'anno. Il valore predefinito è il primo giorno del mese. I valori validi sono: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV e DEC. Il carattere jolly ( \* ) specifica tutti i mesi.

</dd> <dt>

<span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **tempoinattività**
</dt> <dd>

Valore che specifica la quantità di tempo di inattività di attesa prima dell'esecuzione di un'attività OnIdle pianificata. L'intervallo valido è 1-999 minuti.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**
</dt> <dd>

Valore che specifica un nome che identifica in modo univoco l'attività pianificata.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span> **Esecuzioneattività** /TR
</dt> <dd>

Valore che specifica il percorso e il nome file dell'attività da eseguire all'ora pianificata. Ad esempio: C: \\ Windows \\ system32 \\calc.exe.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**
</dt> <dd>

Valore che specifica l'ora di inizio per l'esecuzione dell'attività. Il formato dell'ora è HH: mm (ora di 24 ore). 14:30, ad esempio, specifica 2: pm. Il valore predefinito è l'ora corrente in cui non è specificato/ST. Questa opzione è obbligatoria per Wit l'argomento/SC ONCE.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span> **Intervallo** /ri
</dt> <dd>

Valore che specifica l'intervallo di ripetizione in minuti. Questa operazione non è applicabile per i tipi di pianificazione seguenti: MINUTE, HOURly, OnStart, on LOGOn, OnIdle e OnEvent. L'intervallo valido è 1-599940 minuti. Se vengono specificati i parametri/ET o/DU, il valore predefinito è 10 minuti.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span> **EndTime** /et
</dt> <dd>

Valore che specifica l'ora di fine per l'esecuzione dell'attività. Il formato dell'ora è HH: mm (ora di 24 ore). 14:50, ad esempio, specifica 2:50PM. Questa operazione non è applicabile per i tipi di pianificazione seguenti: OnStart, ONLOGON, OnIdle e OnEvent.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span> **Durata** /du
</dt> <dd>

Valore che specifica la durata di esecuzione dell'attività. Il formato dell'ora è HH: mm (ora di 24 ore). 14:50, ad esempio, specifica 2:50PM. Questa operazione non è applicabile a/ET e per i tipi di pianificazione seguenti: OnStart, inidle e OnEvent. Per le attività/V1 (Utilità di pianificazione 1,0 attività), se si specifica/RI, il valore predefinito della durata è di un'ora.

**Windows XP:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

Valore che termina l'attività all'ora di fine o alla durata. Questa operazione non è applicabile per i tipi di pianificazione seguenti: OnStart, ONLOGON, OnIdle e OnEvent. È necessario specificare/ET o/DU.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **StartDate**
</dt> <dd>

Valore che specifica la prima data in cui eseguire l'attività. Il formato è mm/gg/aaaa. Per impostazione predefinita, questo valore viene impostato sulla data corrente. Questa operazione non è applicabile per i tipi di pianificazione seguenti: una volta, OnStart, un oggetto OnIdle e OnEvent.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**
</dt> <dd>

Valore che specifica l'ultima data in cui l'attività viene eseguita. Il formato è mm/gg/aaaa. Questa operazione non è applicabile per i tipi di pianificazione seguenti: una volta, OnStart, un oggetto OnIdle e OnEvent.

</dd> <dt>

<span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span> **Canalename** /CE
</dt> <dd>

Valore che specifica il canale dell'evento per i trigger OnEvent.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Valore che consente l'esecuzione interattiva dell'attività solo se l'utente/RU è attualmente connesso al momento dell'esecuzione dell'attività. L'attività viene eseguita solo se l'utente è connesso.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_NP_"></span><span id="_np_"></span>**/NP** 
</dt> <dd>

Valore che indica che non viene archiviata alcuna password. L'attività non viene eseguita in modo interattivo come l'utente specificato. Sono disponibili solo le risorse locali.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/Z** 
</dt> <dd>

Valore che contrassegna l'attività da eliminare dopo l'esecuzione finale.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>XMLFile **/XML** 
</dt> <dd>

Valore che crea un'attività da un file XML. Questo parametro può essere combinato con le opzioni/RU e/RP oppure con l'opzione/RP da sola quando il codice XML dell'attività contiene già il database principale.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_V1_"></span><span id="_v1_"></span>**/V1** 
</dt> <dd>

Valore che crea un'attività visibile alle piattaforme Windows 2000, Windows Server 2003 e Windows XP.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/F** 
</dt> <dd>

Valore che crea l'attività in modo forzato ed evita gli avvisi se l'attività specificata esiste già.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Livello** /RL
</dt> <dd>

Valore che imposta il livello di esecuzione per l'attività. I valori validi sono limitati e MASSIMi. Il valore predefinito è LIMITED.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span> **DelayTime** /Delay
</dt> <dd>

Valore che specifica il tempo di attesa per ritardare l'attività dopo che il trigger è stato attivato. Il formato dell'ora è mmmm: SS. Questa opzione è valida solo per i tipi di pianificazione OnStart, ONLOGON e OnEvent.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Valore che Visualizza il messaggio della Guida per Schtasks.exe.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando si crea un'attività in un computer remoto che esegue il sistema operativo Windows XP, Windows Server 2003 o Windows 2000, usare l'opzione/V1.

Non è possibile creare un'attività remota non interattiva Utilità di pianificazione 1,0 (creare un'attività senza usare l'opzione/IT e con l'opzione/V1) se nel computer remoto è abilitata l'eccezione del firewall per la condivisione di file e stampanti e l'eccezione del firewall di gestione delle attività pianificate Remote è disabilitata.

## <a name="deleting-a-task"></a>Eliminazione di un'attività

Per eliminare una o più attività pianificate, viene utilizzata la sintassi seguente.

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il valore predefinito del parametro di sistema è il computer locale.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**
</dt> <dd>

Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per il contesto utente specificato. Se omesso, Schtasks.exe richiede l'input dell'utente.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**
</dt> <dd>

Valore che specifica il nome dell'attività pianificata da eliminare. Il carattere jolly ( \* ) può essere utilizzato per eliminare tutte le attività.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/F** 
</dt> <dd>

Valore che elimina l'attività in modo forzato ed Elimina gli avvisi se l'attività specificata è in esecuzione.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valore che visualizza la guida per Schtasks.exe.

</dd> </dl>

## <a name="running-a-task"></a>Esecuzione di un'attività

La sintassi seguente viene utilizzata per eseguire immediatamente un'attività pianificata.

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il valore predefinito del parametro di sistema è il computer locale.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**
</dt> <dd>

Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per il contesto utente specificato. Se omesso, Schtasks.exe richiede l'input dell'utente.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**
</dt> <dd>

Valore che specifica il nome dell'attività pianificata da eseguire.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valore che visualizza la guida per Schtasks.exe.

</dd> </dl>

## <a name="ending-a-running-task"></a>Terminazione di un'attività in esecuzione

La sintassi seguente viene utilizzata per arrestare un'attività pianificata in esecuzione.

> [!Note]  
> Per arrestare l'esecuzione di un'attività remota, verificare che nel computer remoto siano abilitate le eccezioni del firewall per la condivisione di file e stampanti e le attività pianificate remote.

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il valore predefinito del parametro di sistema è il computer locale.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**
</dt> <dd>

Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per il contesto utente specificato. Se omesso, Schtasks.exe richiede l'input dell'utente.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**
</dt> <dd>

Valore che specifica il nome dell'attività pianificata da arrestare.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valore che visualizza la guida per Schtasks.exe.

</dd> </dl>

## <a name="querying-for-task-information"></a>Esecuzione di query per informazioni sulle attività

La sintassi seguente consente di visualizzare le attività pianificate dal computer locale o remoto.

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il valore predefinito del parametro di sistema è il computer locale.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**
</dt> <dd>

Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per il contesto utente specificato. Se omesso, Schtasks.exe richiede l'input dell'utente.

</dd> <dt>

<span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span> **Formato** /fo
</dt> <dd>

Valore che specifica il formato di output. I valori validi sono TABLE, LIST e CSV.

</dd> <dt>

<span id="_NH_"></span><span id="_nh_"></span>**/NH** 
</dt> <dd>

Valore che specifica che l'intestazione di colonna non deve essere visualizzata nell'output. Questa operazione è valida solo per i formati di tabella e CSV.

</dd> <dt>

<span id="_V_"></span><span id="_v_"></span>**/V** 
</dt> <dd>

Valore che Visualizza l'output dettagliato dell'attività.

> [!Note]  
> Se un'attività è stata pianificata per essere eseguita una sola volta, le informazioni di pianificazione visualizzate sono "la pianificazione dei dati non è disponibile in questo formato".

 

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**
</dt> <dd>

Valore che specifica il nome dell'attività per il quale recuperare le informazioni. Se non viene specificato alcun nome di attività, verranno visualizzate le informazioni relative a tutte le attività.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_XML_"></span><span id="_xml_"></span>**/XML** 
</dt> <dd>

Valore utilizzato per visualizzare le definizioni di attività in formato XML.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Valore utilizzato per visualizzare la guida per Schtasks.exe.

</dd> </dl>

## <a name="changing-a-task"></a>Modifica di un'attività

La sintassi seguente consente di modificare la modalità di esecuzione del programma o di modificare l'account utente e la password utilizzati da un'attività pianificata.

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Valore che specifica il computer remoto a cui connettersi. Se omesso, il valore predefinito del parametro di sistema è il computer locale.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome utente**
</dt> <dd>

Valore che specifica il contesto utente in cui deve essere eseguito Schtasks.exe.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ password \]**
</dt> <dd>

Valore che specifica la password per il contesto utente specificato. Se omesso, Schtasks.exe richiede l'input dell'utente.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **TaskName**
</dt> <dd>

Valore che specifica l'attività pianificata da modificare.

</dd> <dt>

<span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span> **RunAsUser** /ru
</dt> <dd>

Valore che modifica il nome utente (contesto utente) in cui viene eseguita l'attività pianificata. Per l'account di sistema, i valori validi sono "", "NT AUTHORITY \\ System" o "System". Per le attività Utilità di pianificazione 2,0, anche "NT AUTHORITY \\ LocalService" e "NT Authority \\ NetworkService" sono valori validi.

</dd> <dt>

<span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span> **RunAsPassword** /RP
</dt> <dd>

Valore che specifica una nuova password per il contesto utente esistente o la password per un nuovo account utente. Questa password viene ignorata per l'account di sistema.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span> **Esecuzioneattività** /TR
</dt> <dd>

Valore che specifica un nuovo programma che l'attività eseguirà.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**
</dt> <dd>

Valore che specifica l'ora di inizio per l'esecuzione dell'attività. Il formato dell'ora è HH: mm (ora di 24 ore). 14:30, ad esempio, specifica 2: pm.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span> **Intervallo** /ri
</dt> <dd>

Valore che specifica l'intervallo di ripetizione, in minuti. L'intervallo valido è 1-599940 minuti.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span> **EndTime** /et
</dt> <dd>

Valore che specifica l'ora di fine dell'attività. Il formato dell'ora è HH: mm (ora di 24 ore). 14:50, ad esempio, specifica 2:50PM.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span> **Durata** /du
</dt> <dd>

Valore che specifica la durata di esecuzione dell'attività. Il formato dell'ora è HH: mm (ora di 24 ore). 14:50, ad esempio, specifica 2:50PM. Questa operazione non è applicabile al parametro/ET.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

Valore che termina l'attività all'ora di fine o alla durata.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **StartDate**
</dt> <dd>

Valore che specifica la prima data in cui eseguire l'attività. Il formato è mm/gg/aaaa.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**
</dt> <dd>

Valore che specifica l'ultima data in cui l'attività viene eseguita. Il formato è mm/gg/aaaa.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Valore che consente l'esecuzione interattiva dell'attività solo se l'utente/RU è attualmente connesso al momento dell'esecuzione dell'attività. L'attività viene eseguita solo se l'utente è connesso.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Livello** /RL
</dt> <dd>

Valore che imposta il livello di esecuzione per l'attività. I valori validi sono limitati e MASSIMi.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE** 
</dt> <dd>

Valore che Abilita l'attività pianificata. È possibile eseguire un'attività abilitata e non è possibile eseguire un'attività disabilitata.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE** 
</dt> <dd>

Valore che disabilita l'esecuzione dell'attività pianificata.

> [!Note]  
> Se un'attività Utilità di pianificazione 1,0 remota viene disabilitata da Schtasks.exe e nel computer remoto è abilitata l'eccezione del firewall per la condivisione di file e stampanti e l'eccezione del firewall di gestione delle attività pianificate Remote è disabilitata, l'attività non verrà disabilitata quando viene letta da un'API Utilità di pianificazione 2,0.

 

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/Z** 
</dt> <dd>

Valore che contrassegna l'attività da eliminare dopo l'esecuzione finale.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span> **DelayTime** /Delay
</dt> <dd>

Valore che specifica il tempo di attesa per ritardare l'esecuzione dell'attività dopo che il trigger è stato attivato. Il formato dell'ora è mmmm: SS. Questa opzione è valida solo per le attività con i tipi di pianificazione OnStart, ONLOGON e OnEvent.

**Windows XP e Windows Server 2003:** Questa opzione non è disponibile.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Valore che Visualizza il messaggio della Guida per Schtasks.exe.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |



 

 





