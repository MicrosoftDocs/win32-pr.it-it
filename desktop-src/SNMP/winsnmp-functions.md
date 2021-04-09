---
title: Funzioni WinSNMP
description: Le funzioni utilizzate con WinSNMP rientrano nei raggruppamenti funzionali seguenti. Segue un elenco alfabetico.
ms.assetid: ae95ac47-81ff-4715-b3e9-e19c07223712
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7c5ebb49e8ec56c0d0b1174fd667d847c09d3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118051"
---
# <a name="winsnmp-functions"></a>Funzioni WinSNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

Le funzioni utilizzate con WinSNMP rientrano nei raggruppamenti funzionali seguenti. Segue un elenco alfabetico.

-   [Funzioni di comunicazione](#winsnmp-communications-functions)
-   [Funzioni di entità e contesto](#winsnmp-entity-and-context-functions)
-   [Funzioni di database](#winsnmp-database-functions)
-   [Funzioni PDU](#winsnmp-pdu-functions)
-   [Funzioni di utilità](#winsnmp-utility-functions)
-   [Funzioni di associazione variabili](#winsnmp-variable-binding-functions)
-   [Elenco alfabetico delle funzioni WinSNMP](/windows)

## <a name="winsnmp-communications-functions"></a>Funzioni di comunicazione WinSNMP

Le funzioni di comunicazione WinSNMP forniscono un'interfaccia tra l'applicazione WinSNMP chiamante e l'implementazione di Microsoft WinSNMP. L'implementazione gestisce la comunicazione tra l'applicazione e altre entità di gestione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg"><strong>SnmpCancelMsg</strong></a></td>
<td>Richiede che l'implementazione di Microsoft WinSNMP Annulla i tentativi di ritrasmissione e le notifiche di timeout per un messaggio di richiesta SNMP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a></td>
<td>Informa l'implementazione che un'applicazione sta disconnettendo e che non richiede più risorse allocate.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanupex"><strong>SnmpCleanupEx</strong></a></td>
<td>Esegue la pulizia quando non sono presenti chiamate riuscite in attesa a <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> o <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> all'interno di un'applicazione WinSNMP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a></td>
<td>Consente all'implementazione di deallocare le risorse associate a una sessione e di chiudere i meccanismi di comunicazione.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a></td>
<td>Richiede all'implementazione di aprire una sessione WinSNMP e di allocare le risorse e i meccanismi di comunicazione. Quando si sviluppano nuove applicazioni WinSNMP, è consigliabile chiamare la funzione <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> per aprire una sessione WinSNMP anziché chiamare la funzione <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten"><strong>SnmpListen</strong></a></td>
<td>Registra o Annulla la registrazione di un'applicazione WinSNMP come agente SNMP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen"><strong>SnmpOpen</strong></a></td>
<td>Richiede all'implementazione di aprire una sessione WinSNMP e di allocare le risorse e i meccanismi di comunicazione. Quando si sviluppano nuove applicazioni WinSNMP, è consigliabile chiamare la funzione <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> per aprire una sessione WinSNMP anziché chiamare la funzione <strong>SnmpOpen</strong> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a></td>
<td>Restituisce i messaggi SNMP e le notifiche e i dati trap in attesa.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a></td>
<td>Informa l'implementazione che l'applicazione deve registrare o annullare la registrazione per trap e notifiche.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a></td>
<td>Richiede che l'implementazione trasmetta un'unità dati del protocollo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a></td>
<td>Notifica all'implementazione di eseguire le procedure di inizializzazione per l'applicazione. Prima di chiamare qualsiasi altra funzione WinSNMP, un'applicazione deve chiamare correttamente la funzione <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a></td>
<td>Notifica all'implementazione di Microsoft WinSNMP che l'applicazione WinSNMP richiede i servizi dell'implementazione. <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartupex"><strong>SnmpStartupEx</strong></a> Abilita il supporto per più moduli software indipendenti che usano WinSNMP all'interno della stessa applicazione.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback"><strong>SNMPAPI_CALLBACK</strong></a></td>
<td>Notifica a una sessione WinSNMP che è disponibile un messaggio SNMP o un evento asincrono.
<blockquote>
[!Note]<br />
Questa funzione di callback viene applicata solo alle sessioni aperte in seguito a una chiamata alla funzione <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a> .
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="winsnmp-entity-and-context-functions"></a>Funzioni di contesto e entità WinSNMP

Le funzioni di contesto e entità WinSNMP consentono a un'applicazione WinSNMP di specificare nomi descrittivi per entità e contesti SNMP. L'implementazione di Microsoft WinSNMP converte il nome nei relativi componenti SNMPv1 o SNMPv2C usando il database di implementazione.



| Funzione                                     | Descrizione                                                                                                            |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) | Restituisce una stringa che identifica un contesto SNMP (un set di risorse degli oggetti gestiti).                                  |
| [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)   | Restituisce una stringa che identifica un'entità di gestione SNMP.                                                            |
| [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)   | Rilascia le risorse allocate dalla funzione [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) per un contesto SNMP.         |
| [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)     | Rilascia le risorse allocate dalla funzione [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) per un'entità di gestione SNMP. |
| [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)           | Modifica la porta assegnata a un'entità di destinazione SNMP.                                                               |
| [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) | Restituisce un handle per informazioni sul contesto SNMP specifiche dell'implementazione.                                   |
| [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)   | Restituisce un handle per informazioni sull'entità di gestione SNMP specifiche dell'implementazione.                         |



 

## <a name="winsnmp-database-functions"></a>Funzioni di database WinSNMP

Le funzioni di database WinSNMP forniscono un'applicazione WinSNMP con accesso alle impostazioni correnti nell'archivio delle informazioni amministrative dell'implementazione di Microsoft WinSNMP. Queste funzioni consentono di modificare la modalità di ritrasmissione e la modalità di conversione dell'entità e del contesto. Le funzioni di database offrono inoltre all'applicazione la possibilità di modificare i valori di timeout e di numero di tentativi.



| Funzione                                               | Descrizione                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) | Restituisce l'impostazione corrente della modalità di ritrasmissione.                                               |
| [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)                   | Restituisce il valore del numero di tentativi, in unità, per la ritrasmissione delle richieste di messaggi SNMP.             |
| [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)               | Restituisce il valore di timeout, in centesimi di secondo, per la trasmissione di richieste di messaggi SNMP. |
| [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)   | Restituisce l'impostazione corrente della modalità di conversione dell'entità e del contesto.                               |
| [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)         | Recupera le informazioni che identificano il fornitore WinSNMP.                                             |
| [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) | Modifica la modalità di ritrasmissione.                                                                      |
| [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)                   | Modifica il valore del numero di tentativi per la ritrasmissione delle richieste di messaggi SNMP.                        |
| [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)               | Modifica il valore di timeout per la trasmissione di richieste di messaggi SNMP.                             |
| [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)   | Modifica la modalità di conversione dell'entità e del contesto.                                                      |



 

## <a name="winsnmp-pdu-functions"></a>Funzioni PDU WinSNMP

Le funzioni WinSNMP PDU consentono alle applicazioni WinSNMP di estrarre e aggiornare gli elementi dati (o i campi) di una PDU. Questo include PDU restituito da una chiamata alla funzione [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) o alla funzione [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg) . Le funzioni PDU costruiscono anche PDU per l'uso nelle funzioni [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) e [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .



| Funzione                                     | Descrizione                                                                                                                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)       | Crea e Inizializza un'unità dati del protocollo SNMP.                                                                                                                               |
| [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) | Duplica un'unità dati del protocollo SNMP.                                                                                                                                            |
| [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)           | Rilascia le risorse associate a un'unità dati del protocollo SNMP creata dalla funzione [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) o [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu) . |
| [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)     | Restituisce gli elementi dati selezionati da un'unità dati del protocollo SNMP specificata.                                                                                                          |
| [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)     | Aggiorna gli elementi dati selezionati in un'unità dati del protocollo SNMP specificata.                                                                                                            |



 

## <a name="winsnmp-utility-functions"></a>Funzioni di utilità WinSNMP

Le funzioni di utilità WinSNMP consentono a un'applicazione WinSNMP di gestire gli oggetti e i messaggi SNMP nell'interfaccia WinSNMP.



| Funzione                                         | Descrizione                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)           | Decodifica un messaggio SNMP codificato o serializzato nei relativi componenti costitutivi.                                      |
| [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)           | Crea un messaggio SNMP codificato.                                                                                    |
| [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) | Segnala all'implementazione di Microsoft WinSNMP che deve liberare la memoria allocata per un determinato descrittore. |
| [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)     | Restituisce il valore del codice dell'ultimo errore per l'ultima operazione SNMP.                                                      |
| [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)         | Confronta due identificatori di oggetti SNMP.                                                                               |
| [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)               | Copia un identificatore di oggetto SNMP.                                                                                   |
| [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)             | Converte la rappresentazione binaria interna di un identificatore di oggetto SNMP nel formato della stringa numerica punteggiata.       |
| [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)             | Converte il formato della stringa numerica punteggiata di un identificatore di oggetto SNMP nella relativa rappresentazione binaria interna.       |



 

## <a name="winsnmp-variable-binding-functions"></a>Funzioni di associazione variabili WinSNMP

Le funzioni di associazione variabili WinSNMP consentono alle applicazioni WinSNMP di creare e modificare elenchi di associazioni variabili e di includerle in PDU.



| Funzione                                     | Descrizione                                                                                                                                                                     |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)         | Enumera le voci di associazione variabili in un elenco di associazioni variabili specificato.                                                                                                   |
| [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)       | Crea un nuovo elenco di associazioni variabili.                                                                                                                                            |
| [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)         | Rimuove una voce di associazione variabile da un elenco di associazioni di variabili.                                                                                                                  |
| [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) | Copia un elenco di associazioni variabili.                                                                                                                                                 |
| [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)           | Rilascia le risorse per un elenco di associazioni variabili allocate in precedenza dalla funzione [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl) o [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl) . |
| [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)               | Recupera le informazioni da una voce di associazione variabile specificata.                                                                                                                  |
| [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)               | Modifica le voci di associazione variabili in un elenco di associazioni variabili; Accoda nuove voci di associazione di variabili a un elenco di associazioni variabili esistente.                                         |



 

## <a name="winsnmp-functions---alphabetic-list"></a>Elenco alfabetico delle funzioni WinSNMP

-   [**\_callback snmpapi**](/windows/desktop/api/Winsnmp/nc-winsnmp-snmpapi_callback)
-   [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg)
-   [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup)
-   [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose)
-   [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)
-   [**SnmpCountVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcountvbl)
-   [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu)
-   [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession)
-   [**SnmpCreateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl)
-   [**SnmpDecodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdecodemsg)
-   [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb)
-   [**SnmpDuplicatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu)
-   [**SnmpDuplicateVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl)
-   [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg)
-   [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)
-   [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)
-   [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor)
-   [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)
-   [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu)
-   [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl)
-   [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror)
-   [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata)
-   [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode)
-   [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry)
-   [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout)
-   [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode)
-   [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb)
-   [**SnmpGetVendorInfo**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvendorinfo)
-   [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten)
-   [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare)
-   [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy)
-   [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)
-   [**SnmpOpen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpopen)
-   [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg)
-   [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister)
-   [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)
-   [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata)
-   [**SnmpSetPort**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetport)
-   [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode)
-   [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry)
-   [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout)
-   [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode)
-   [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb)
-   [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)
-   [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext)
-   [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)
-   [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)

 

