---
title: Funzioni SNMP
description: Questo argomento descrive tre raggruppamenti di funzioni SNMP ed elenca le funzioni incluse in ogni gruppo
ms.assetid: 8913caa9-6b2c-424c-a778-bd54d6584dac
keywords:
- SNMP (funzioni SNMP)
- Funzioni SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f4cc98ce84fbb66f8beb59a6bf995dc4315159
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473974"
---
# <a name="snmp-functions"></a>Funzioni SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

Questo argomento descrive tre raggruppamenti di funzioni SNMP ed elenca le funzioni incluse in ogni gruppo:

-   [Funzioni API dell'agente di estensione SNMP](#snmp-extension-agent-api-functions)
-   [Funzioni API di gestione SNMP](#snmp-management-api-functions)
-   [Funzioni API dell'utilità SNMP](#snmp-utility-api-functions)

## <a name="snmp-extension-agent-api-functions"></a>Funzioni API dell'agente di estensione SNMP

Le funzioni dell'agente di estensione SNMP definiscono l'interfaccia tra il servizio SNMP e le DLL dell'agente di estensione SNMP di terze parti. Nella tabella seguente sono elencate le funzioni che possono essere utilizzate dalle applicazioni per risolvere le associazioni variabili specificate dalle unità dati del protocollo SNMP in ingresso (PDU).

| Funzione API dell'agente di estensione SNMP                    | Descrizione                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**SnmpExtensionClose**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionclose)     | Richiede all'agente di estensione SNMP di deallocare le risorse e terminare le operazioni.                                    |
| [**SnmpExtensionInit**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninit)       | Inizializza la DLL dell'agente di estensione SNMP.                                                                                |
| [**SnmpExtensionInitEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninitex)   | Identifica eventuali sottoalberi MIB (Management Information Base) aggiuntivi supportati dall'agente di estensione SNMP.             |
| [**SnmpExtensionMonitor**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionmonitor) | Fornisce all'agente di estensione SNMP le informazioni sui contatori e i parametri interni del servizio.            |
| [**SnmpExtensionQuery**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionquery)     | Risolve le richieste SNMP che contengono variabili in uno o più sottoalberi MIB registrati dell'agente di estensione SNMP. |
| [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) | Elabora le richieste SNMP che specificano le variabili in uno o più sottoalberi MIB registrati dagli agenti di estensione SNMP. |
| [**SnmpExtensionTrap**](/windows/desktop/api/Snmp/nf-snmp-snmpextensiontrap)       | Recupera le informazioni necessarie al servizio per generare trap per l'agente di estensione SNMP.                          |



 

## <a name="snmp-management-api-functions"></a>Funzioni API di gestione SNMP

Le funzioni di gestione SNMP definiscono l'interfaccia tra le applicazioni di gestione SNMP di terze parti e la libreria a collegamento dinamico (DLL) della funzione di gestione Mgmtapi.dll. La DLL funziona insieme al servizio trap SNMP (Snmptrap.exe) e può interagire con una o più applicazioni di gestione SNMP di terze parti. Nella tabella seguente sono elencate le funzioni di gestione utilizzate dalle applicazioni di gestione di terze parti per eseguire operazioni di gestione SNMP.

| Funzione API di gestione SNMP                   | Descrizione                                                                                                                                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpMgrClose**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrclose)           | Chiude le strutture di dati e i socket di comunicazione associati alla sessione specificata.                                                                                                  |
| [**SnmpMgrCtl**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrctl)               | Imposta un parametro operativo associato a una sessione SNMP.                                                                                                                                   |
| [**SnmpMgrGetTrap**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrap)       | Restituisce i dati trap in attesa che il chiamante non ha ricevuto se è abilitata la ricezione trap.                                                                                                           |
| [**SnmpMgrGetTrapEx**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrapex)   | Restituisce i dati trap in attesa che il chiamante non ha ricevuto se è abilitata la ricezione trap. Restituisce anche l'indirizzo dell'origine del trasporto e il trap della community associato alla trap. |
| [**SnmpMgrOidToStr**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgroidtostr)     | Converte una struttura dell'identificatore di oggetto interno nella relativa rappresentazione di stringa.                                                                                                                         |
| [**SnmpMgrOpen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgropen)             | Inizializza le strutture di dati e i socket di comunicazione necessari per stabilire la comunicazione con l'agente SNMP.                                                                               |
| [**Chiamata SnmpMgrRequest**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrrequest)       | Richiede che l'operazione specificata venga eseguita dall'agente specificato.                                                                                                                             |
| [**SnmpMgrStrToOid**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrstrtooid)     | Converte il formato di stringa di un identificatore di oggetto nella struttura dell'identificatore di oggetto interno.                                                                                                        |
| [**SnmpMgrTrapListen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrtraplisten) | Registra la capacità di un'applicazione di gestione SNMP di ricevere trap SNMP dal servizio trap SNMP.                                                                                                 |



 

## <a name="snmp-utility-api-functions"></a>Funzioni API dell'utilità SNMP

Le funzioni di utilità SNMP forniscono funzionalità utili durante lo sviluppo di applicazioni SNMP, inclusa la semplificazione della manipolazione delle strutture di dati SNMP. Nella tabella seguente sono elencate le funzioni di utilità SNMP.

| Funzione API utilità SNMP                                  | Descrizione                                                                                                                                                        |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpSvcGetUptime**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcgetuptime)               | Recupera l'ora, in centiseconds, per la quale è stato eseguito il servizio SNMP.                                                                                  |
| [**SnmpSvcSetLogLevel**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetloglevel)           | Regola il livello di dettaglio dell'output di debug dal servizio SNMP e dagli agenti di estensione SNMP.                                                              |
| [**SnmpSvcSetLogType**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetlogtype)             | Regola la destinazione per l'output di debug dal servizio SNMP e dagli agenti di estensione SNMP.                                                                 |
| [**SnmpUtilAsnAnyCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanycpy)             | Copia una struttura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) di origine in una struttura **AsnAny** di destinazione.                                                                      |
| [**SnmpUtilAsnAnyFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanyfree)           | Libera la memoria allocata per una struttura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) specificata.                                                                        |
| [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)               | Imposta il livello di informazioni di debug da ricevere dal servizio SNMP o da una chiamata a [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint).                       |
| [**SnmpUtilIdsToA**](/windows/desktop/api/Snmp/nf-snmp-snmputilidstoa)                   | Converte un identificatore di oggetto (OID) in una stringa a terminazione null.                                                                                                   |
| [**SnmpUtilMemAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemalloc)               | Alloca la memoria dinamica dall'heap del processo.                                                                                                                    |
| [**SnmpUtilMemFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemfree)                 | Libera l'oggetto di memoria specificato.                                                                                                                                 |
| [**SnmpUtilMemReAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemrealloc)           | Modifica le dimensioni dell'oggetto memoria specificato.                                                                                                                   |
| [**SnmpUtilOctetsCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscmp)             | Confronta due stringhe ottetto.                                                                                                                                        |
| [**SnmpUtilOctetsCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscpy)             | Copia una struttura [**AsnOctetString**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring) di origine in una struttura **AsnOctetString** di destinazione.                                              |
| [**SnmpUtilOctetsFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsfree)           | Libera la memoria allocata per la stringa di ottetto specificata.                                                                                                |
| [**SnmpUtilOctetsNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsncmp)           | Esegue un confronto tra due stringhe di ottetti e il numero specificato di sottoidentificatori.                                                                              |
| [**SnmpUtilOidAppend**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidappend)             | Accoda un identificatore di oggetto di origine, contenuto in una struttura [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) , a un identificatore di oggetto di destinazione.          |
| [**SnmpUtilOidCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcmp)                   | Confronta due identificatori di oggetto contenuti nelle strutture [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) .                                           |
| [**SnmpUtilOidCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcpy)                   | Copia una struttura [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) di origine in una struttura **AsnObjectIdentifier** di destinazione.                               |
| [**SnmpUtilOidFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidfree)                 | Libera la memoria allocata per l'identificatore di oggetto specificato.                                                                                           |
| [**SnmpUtilOidNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidncmp)                 | Confronta due identificatori di oggetto contenuti nelle strutture [**AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) al numero specificato di sottoidentificatori. |
| [**SnmpUtilOidToA**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidtoa)                   | Converte un identificatore di oggetto (OID) in una stringa a terminazione null.                                                                                                   |
| [**SnmpUtilPrintAsnAny**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintasnany)         | Stampa un valore contenuto in una struttura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) a scopo di debug e sviluppo.                                              |
| [**SnmpUtilPrintOid**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintoid)               | Formatta l'identificatore di oggetto specificato (OID) e stampa il risultato nel dispositivo di output standard.                                                                 |
| [**SnmpUtilVarBindCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindcpy)           | Copia una struttura [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) di origine in una struttura **SnmpVarBind** di destinazione.                                                       |
| [**SnmpUtilVarBindListCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistcpy)   | Copia una struttura [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) di origine in una struttura **SnmpVarBindList** di destinazione.                                           |
| [**SnmpUtilVarBindFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindfree)         | Libera la memoria allocata per la struttura [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) specificata.                                                            |
| [**SnmpUtilVarBindListFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistfree) | Libera la memoria allocata per la struttura [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) specificata.                                                    |



 

 

 