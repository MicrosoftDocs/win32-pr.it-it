---
title: Funzioni SNMP
description: Questo argomento descrive tre raggruppamenti di funzioni SNMP ed elenca le funzioni incluse in ogni gruppo
ms.assetid: 8913caa9-6b2c-424c-a778-bd54d6584dac
keywords:
- Funzioni SNMP SNMP
- Funzioni SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42028e4045d4d0dfeb183dc29a3dc85e7220ed3d5bccf39a3cc9871215188153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143014"
---
# <a name="snmp-functions"></a>Funzioni SNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece Windows [gestione remota](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

Questo argomento descrive tre raggruppamenti di funzioni SNMP ed elenca le funzioni incluse in ogni gruppo:

-   [Funzioni API dell'agente di estensione SNMP](#snmp-extension-agent-api-functions)
-   [Funzioni API Gestione SNMP](#snmp-management-api-functions)
-   [Funzioni API dell'utilità SNMP](#snmp-utility-api-functions)

## <a name="snmp-extension-agent-api-functions"></a>Funzioni API dell'agente di estensione SNMP

Le funzioni dell'agente di estensione SNMP definiscono l'interfaccia tra il servizio SNMP e le DLL dell'agente di estensione SNMP di terze parti. Nella tabella seguente sono elencate le funzioni che le applicazioni possono usare per risolvere le associazioni di variabili specificate dalle unità PTU (Protocol Data Unit) SNMP in ingresso.

| Funzione API dell'agente di estensione SNMP                    | Descrizione                                                                                                              |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**SnmpExtensionClose**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionclose)     | Richiede che l'agente di estensione SNMP dealloci le risorse e termini le operazioni.                                    |
| [**SnmpExtensionInit**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninit)       | Inizializza la DLL dell'agente di estensione SNMP.                                                                                |
| [**SnmpExtensionInitEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensioninitex)   | Identifica eventuali sottoalberi MIB (Management Information Base) aggiuntivi supportati dall'agente di estensione SNMP.             |
| [**SnmpExtensionMonitor**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionmonitor) | Fornisce all'agente di estensione SNMP informazioni sui contatori interni e sui parametri del servizio.            |
| [**SnmpExtensionQuery**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionquery)     | Risolve le richieste SNMP che contengono variabili in uno o più sottoalberi MIB registrati dell'agente di estensione SNMP. |
| [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) | Elabora le richieste SNMP che specificano variabili in uno o più sottoalberi MIB registrati dagli agenti di estensione SNMP. |
| [**SnmpExtensionTrap**](/windows/desktop/api/Snmp/nf-snmp-snmpextensiontrap)       | Recupera le informazioni richieste dal servizio per generare trap per l'agente di estensione SNMP.                          |



 

## <a name="snmp-management-api-functions"></a>Funzioni API Gestione SNMP

Le funzioni di gestione SNMP definiscono l'interfaccia tra le applicazioni di gestione SNMP di terze parti e la libreria a collegamento dinamico (DLL) della funzione di gestione Mgmtapi.dll. La DLL funziona in combinazione con il servizio trap SNMP (Snmptrap.exe) e può interagire con una o più applicazioni di gestione SNMP di terze parti. Nella tabella seguente sono elencate le funzioni di gestione usate dalle applicazioni di gestione di terze parti per eseguire operazioni di gestione SNMP.

| Funzione API Gestione SNMP                   | Descrizione                                                                                                                                                                                            |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpMgrClose**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrclose)           | Chiude i socket di comunicazione e le strutture dei dati associati alla sessione specificata.                                                                                                  |
| [**SnmpMgrCtl**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrctl)               | Imposta un parametro operativo associato a una sessione SNMP.                                                                                                                                   |
| [**SnmpMgrGetTrap**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrap)       | Restituisce i dati trap in sospeso che il chiamante non ha ricevuto se la ricezione trap è abilitata.                                                                                                           |
| [**SnmpMgrGetTrapEx**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrgettrapex)   | Restituisce i dati trap in sospeso che il chiamante non ha ricevuto se la ricezione trap è abilitata. Restituisce anche l'indirizzo dell'origine del trasporto e la trap della community associata alla trap. |
| [**SnmpMgrOidToStr**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgroidtostr)     | Converte una struttura dell'identificatore di oggetto interno nella relativa rappresentazione di stringa.                                                                                                                         |
| [**SnmpMgrOpen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgropen)             | Inizializza i socket di comunicazione e le strutture dei dati necessari per stabilire la comunicazione con l'agente SNMP.                                                                               |
| [**SnmpMgrRequest**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrrequest)       | Richiede che l'operazione specificata sia eseguita dall'agente specificato.                                                                                                                             |
| [**SnmpMgrStrToOid**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrstrtooid)     | Converte il formato stringa di un identificatore di oggetto nella struttura interna dell'identificatore di oggetto.                                                                                                        |
| [**SnmpMgrTrapListen**](/windows/desktop/api/Mgmtapi/nf-mgmtapi-snmpmgrtraplisten) | Registra la capacità di un'applicazione di gestione SNMP di ricevere trap SNMP dal servizio trap SNMP.                                                                                                 |



 

## <a name="snmp-utility-api-functions"></a>Funzioni API dell'utilità SNMP

Le funzioni di utilità SNMP offrono funzionalità utili durante lo sviluppo di applicazioni SNMP, inclusa la semplificazione della manipolazione delle strutture di dati SNMP. Nella tabella seguente sono elencate le funzioni dell'utilità SNMP.

| Funzione API dell'utilità SNMP                                  | Descrizione                                                                                                                                                        |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpSvcGetUptime**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcgetuptime)               | Recupera l'ora, in secondi, per cui è stato eseguito il servizio SNMP.                                                                                  |
| [**SnmpSvcSetLogLevel**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetloglevel)           | Regola il livello di dettaglio dell'output di debug dal servizio SNMP e dagli agenti di estensione SNMP.                                                              |
| [**SnmpSvcSetLogType**](/windows/desktop/api/Snmp/nf-snmp-snmpsvcsetlogtype)             | Regola la destinazione per l'output di debug dal servizio SNMP e dagli agenti di estensione SNMP.                                                                 |
| [**SnmpUtilAsnAnyCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanycpy)             | Copia una struttura [**AsnAny di**](/windows/desktop/api/Snmp/ns-snmp-asnany) origine in una **struttura AsnAny di** destinazione.                                                                      |
| [**SnmpUtilAsnAnyFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilasnanyfree)           | Libera la memoria allocata per una struttura [**AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) specificata.                                                                        |
| [**SnmpUtilDbgPrint**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)               | Imposta il livello di informazioni di debug da ricevere dal servizio SNMP o da una chiamata a [**SnmpUtilDbgPrint.**](/windows/desktop/api/Snmp/nf-snmp-snmputildbgprint)                       |
| [**SnmpUtilIdsToA**](/windows/desktop/api/Snmp/nf-snmp-snmputilidstoa)                   | Converte un identificatore di oggetto (OID) in una stringa con terminazione Null.                                                                                                   |
| [**SnmpUtilMemAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemalloc)               | Alloca memoria dinamica dall'heap del processo.                                                                                                                    |
| [**SnmpUtilMemFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemfree)                 | Libera l'oggetto memoria specificato.                                                                                                                                 |
| [**SnmpUtilMemReAlloc**](/windows/desktop/api/Snmp/nf-snmp-snmputilmemrealloc)           | Modifica le dimensioni dell'oggetto memoria specificato.                                                                                                                   |
| [**SnmpUtilOctetsCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscmp)             | Confronta due stringhe di ottetti.                                                                                                                                        |
| [**SnmpUtilOctetsCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetscpy)             | Copia una struttura [**AsnOctetString di**](/windows/desktop/api/Snmp/ns-snmp-asnoctetstring) origine in una **struttura AsnOctetString di** destinazione.                                              |
| [**SnmpUtilOctetsFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsfree)           | Libera la memoria allocata per la stringa di ottetti specificata.                                                                                                |
| [**SnmpUtilOctetsNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloctetsncmp)           | Esegue un confronto tra due stringhe ottetti con il numero specificato di sottoidentificatori.                                                                              |
| [**SnmpUtilOidAppend**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidappend)             | Aggiunge un identificatore di oggetto di origine, contenuto in una [**struttura AsnObjectIdentifier,**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) a un identificatore di oggetto di destinazione.          |
| [**SnmpUtilOidCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcmp)                   | Confronta due identificatori di oggetto contenuti nelle [**strutture AsnObjectIdentifier.**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier)                                           |
| [**SnmpUtilOidCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidcpy)                   | Copia una struttura [**AsnObjectIdentifier di**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) origine in una **struttura AsnObjectIdentifier di** destinazione.                               |
| [**SnmpUtilOidFree**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidfree)                 | Libera la memoria allocata per l'identificatore di oggetto specificato.                                                                                           |
| [**SnmpUtilOidNCmp**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidncmp)                 | Confronta due identificatori di oggetto contenuti nelle [**strutture AsnObjectIdentifier**](/windows/desktop/api/Snmp/ns-snmp-asnobjectidentifier) con il numero specificato di sottoidentificatori. |
| [**SnmpUtilOidToA**](/windows/desktop/api/Snmp/nf-snmp-snmputiloidtoa)                   | Converte un identificatore di oggetto (OID) in una stringa con terminazione Null.                                                                                                   |
| [**SnmpUtilPrintAsnAny**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintasnany)         | Stampa un valore contenuto in una [**struttura AsnAny**](/windows/desktop/api/Snmp/ns-snmp-asnany) a scopo di debug e sviluppo.                                              |
| [**SnmpUtilPrintOid**](/windows/desktop/api/Snmp/nf-snmp-snmputilprintoid)               | Formatta l'identificatore di oggetto (OID) specificato e stampa il risultato nel dispositivo di output standard.                                                                 |
| [**SnmpUtilVarBindCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindcpy)           | Copia una struttura [**SnmpVarBind di**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) origine in una **struttura SnmpVarBind di** destinazione.                                                       |
| [**SnmpUtilVarBindListCpy**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistcpy)   | Copia una struttura [**SnmpVarBindList di**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) origine in una **struttura SnmpVarBindList di** destinazione.                                           |
| [**SnmpUtilVarBindFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindfree)         | Libera la memoria allocata per la struttura [**SnmpVarBind**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbind) specificata.                                                            |
| [**SnmpUtilVarBindListFree**](/windows/desktop/api/Snmp/nf-snmp-snmputilvarbindlistfree) | Libera la memoria allocata per la struttura [**SnmpVarBindList**](/windows/desktop/api/Snmp/ns-snmp-snmpvarbindlist) specificata.                                                    |



 

 

 