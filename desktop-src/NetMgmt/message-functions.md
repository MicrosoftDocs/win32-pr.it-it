---
title: Funzioni dei messaggi (gestione di rete)
description: Le funzioni dei messaggi di gestione della rete inviano messaggi e gestiscono gli alias dei messaggi. Le funzioni dei messaggi sono elencate di seguito.
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b30f88b3cbe0742b3bd06f2200475aaeb0d96d0c37bff9189efd1127ddc7d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912041"
---
# <a name="message-functions-network-management"></a>Funzioni dei messaggi (gestione di rete)

\[Le funzioni dei messaggi non sono supportate a Windows Vista perché i servizi di avviso e messenger non sono supportati.\]

Le funzioni dei messaggi di gestione della rete inviano messaggi e gestiscono gli alias dei messaggi. Le funzioni dei messaggi sono elencate di seguito.

**Windows Server 2003:** I servizi alerter e messenger sono disabilitati per impostazione predefinita. È necessario abilitare nuovamente i servizi prima di chiamare le funzioni di avviso di gestione della [rete](alert-functions.md) o le funzioni dei messaggi di gestione della rete.



| Funzione                                               | Descrizione                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Invia un messaggio a un alias di messaggio registrato.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registra un alias del messaggio nella tabella del nome del messaggio.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Elimina un alias di messaggio dalla tabella del nome del messaggio.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Elenca tutti gli alias dei messaggi archiviati nella tabella dei nomi dei messaggi.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Restituisce informazioni su un alias di messaggio specifico nella tabella del nome del messaggio. |



 

Un *messaggio* è un buffer di dati di testo inviati a un utente o a un'applicazione in rete. Per ricevere un messaggio, un utente o un'applicazione deve registrare un alias del messaggio nella tabella dei nomi dei messaggi di un computer. Gli alias seguenti vengono registrati per impostazione predefinita: "user", "machine", "domain" o \* " " (il dominio corrente del computer). L'alias "dominio" specifica il set di computer con lo stesso nome di dominio definito come dominio o come gruppo di lavoro e in ascolto delle trasmissioni nella stessa subnet. Per NetBIOS su TCP/IP, la specifica dell'alias "dominio" può avere esito positivo anche tra subnet se il nome di dominio viene risolto da un server dei nomi o se le trasmissioni di datagrammi NetBIOS vengono inoltrate tra router. Pertanto, i messaggi inviati a un dominio non hanno il recapito garantito a tutti i membri del dominio. È anche possibile che alcuni membri del dominio ricevano il messaggio più volte se sono installati più trasporti che supportano NetBIOS.

È anche possibile registrare un alias del messaggio chiamando la [**funzione NetMessageNameAdd.**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) Una *tabella dei nomi dei* messaggi contiene un elenco di alias di messaggi registrati (utenti e applicazioni) autorizzati a ricevere messaggi. Per gli alias registrati nella tabella dei nomi dei messaggi non viene fatto distinzione tra maiuscole e minuscole.

Il servizio Messenger deve essere in esecuzione nel computer ricevente per visualizzare un messaggio popup quando viene ricevuto il messaggio. Inoltre, il servizio Workstation deve essere in esecuzione nel computer locale. NetBIOS è il meccanismo di trasporto usato tra il mittente e il destinatario.

Le funzioni dei messaggi sono disponibili a due livelli di informazioni:

-   [**MSG \_ INFO \_ 0**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [**MSG \_ INFO \_ 1**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

Il **livello di informazioni \_ MSG INFO \_ 1** esiste solo per motivi di compatibilità. Il servizio Messenger non inoltra i nomi né consente l'inoltro dei nomi.

 

 




