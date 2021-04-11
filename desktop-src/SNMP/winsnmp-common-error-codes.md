---
title: Codici di errore comuni di WinSNMP
description: La funzione SnmpGetLastError può restituire un codice di errore generale dopo la mancata riuscita di una funzione WinSNMP. La tabella seguente elenca i codici di errore comuni di WinSNMP.
ms.assetid: c286750f-a542-4f61-a22c-d77debd45775
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beee49aef651784b0b8dc05c0114b7bf906be113
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047078"
---
# <a name="winsnmp-common-error-codes"></a>Codici di errore comuni di WinSNMP

\[SNMP è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. Usare invece [gestione remota Windows](/windows/desktop/WinRM/portal), ovvero l'implementazione Microsoft di WS-Man.\]

La funzione [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) può restituire un codice di errore generale dopo la mancata riuscita di una funzione WinSNMP. La tabella seguente elenca i codici di errore comuni di WinSNMP.



| Codice di errore                | Significato                                                                                                                                                                                                        | Azione consigliata                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SNMPAPI \_ non \_ inizializzato | La funzione [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) non è stata completata correttamente perché l'esecuzione del programma è iniziata o perché una chiamata alla funzione [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) è stata completata correttamente. | L'applicazione deve chiamare [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) prima di chiamare qualsiasi altra funzione API WinSNMP quando [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) ha esito negativo. La funzione [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) restituisce informazioni di errore estese sull'errore di [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup).                                                          |
| \_errore di allocazione snmpapi \_     | L'applicazione ha specificato un puntatore non valido o si è verificato un errore durante l'allocazione della memoria. L'implementazione di Microsoft WinSNMP non è in grado di ottenere risorse sufficienti per eseguire la richiesta.                | L'applicazione deve fornire puntatori di memoria validi per tutti i parametri di output. Deve liberare risorse, ridurre i requisiti delle risorse o facilitare un arresto normale. Un arresto normale include più chiamate alla funzione [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) , una per ogni sessione WinSNMP aperta. Include inoltre una chiamata alla funzione [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) . |
| \_NoOp snmpapi             | La funzione non è stata completata correttamente perché tutti i parametri di output sono **null**.                                                                                                                         | L'applicazione deve specificare almeno un parametro di output diverso da **null** quando si chiama una funzione che restituisce informazioni all'applicazione.                                                                                                                                                                                                                                  |
| SNMPAPI \_ altro \_ errore     | Si è verificato un errore sconosciuto o non definito.                                                                                                                                                                        | L'applicazione dovrebbe in genere rispondere con un arresto normale. Un arresto normale include più chiamate alla funzione [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) , una per ogni sessione WinSNMP aperta. Include inoltre una chiamata alla funzione [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) .                                                                                                           |



 

Gli errori WinSNMP che comportano informazioni specifiche del contesto sono indicati nella pagina di riferimento di ogni funzione.

 

 