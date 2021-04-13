---
title: Funzioni di messaggio (gestione della rete)
description: Le funzioni del messaggio di gestione della rete inviano messaggi e gestiscono gli alias dei messaggi. Le funzioni del messaggio sono elencate di seguito.
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3629a281637fe4ecd0c937ce0c7504beac8e11d2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400148"
---
# <a name="message-functions-network-management"></a>Funzioni di messaggio (gestione della rete)

\[Le funzioni di messaggio non sono supportate a partire da Windows Vista, perché i servizi Alerter e Messenger non sono supportati.\]

Le funzioni del messaggio di gestione della rete inviano messaggi e gestiscono gli alias dei messaggi. Le funzioni del messaggio sono elencate di seguito.

**Windows Server 2003:** I servizi Alerter e Messenger sono disabilitati per impostazione predefinita. È necessario riabilitare i servizi prima di chiamare le funzioni di [avviso](alert-functions.md) di gestione di rete o le funzioni del messaggio di gestione di rete.



| Funzione                                               | Descrizione                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Invia un messaggio a un alias di messaggio registrato.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registra un alias del messaggio nella tabella dei nomi dei messaggi.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Elimina un alias del messaggio dalla tabella dei nomi dei messaggi.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Elenca tutti gli alias di messaggio archiviati nella tabella dei nomi dei messaggi.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Restituisce informazioni su un particolare alias del messaggio nella tabella dei nomi dei messaggi. |



 

Un *messaggio* è un buffer di dati di testo inviati a un utente o a un'applicazione sulla rete. Per ricevere un messaggio, è necessario che un utente o un'applicazione registri un alias di messaggio nella tabella dei nomi dei messaggi del computer. Per impostazione predefinita, vengono registrati gli alias seguenti: "User", "Machine", "Domain" o " \* " (il dominio corrente del computer). L'alias "dominio" specifica il set di computer con lo stesso nome di dominio definito come dominio o come gruppo di lavoro e in ascolto delle trasmissioni nella stessa subnet. Per NetBIOS su TCP/IP, è possibile specificare l'alias "dominio" tra le subnet se il nome di dominio viene risolto da un server dei nomi o se le trasmissioni del datagramma NetBIOS vengono inoltrate tra i router. Pertanto, i messaggi inviati a un dominio non hanno garantito il recapito a tutti i membri del dominio. È inoltre possibile che alcuni membri del dominio ricevano il messaggio più volte se sono installati più trasporti che supportano NetBIOS.

È anche possibile registrare un alias del messaggio chiamando la funzione [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) . Una *tabella dei nomi di messaggio* contiene un elenco di alias di messaggi registrati (utenti e applicazioni) autorizzati a ricevere messaggi. Gli alias registrati nella tabella nome messaggio non fanno distinzione tra maiuscole e minuscole.

Il servizio Messenger deve essere in esecuzione nel computer ricevente per visualizzare un messaggio popup quando il messaggio viene ricevuto. Inoltre, è necessario che il servizio workstation sia in esecuzione nel computer locale. NetBIOS è il meccanismo di trasporto utilizzato tra il mittente e il destinatario.

Le funzioni di messaggio sono disponibili a due livelli di informazioni:

-   [**\_Informazioni messaggio \_ 0**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [**\_Informazioni messaggio \_ 1**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

Il livello di informazioni **msg \_ info \_ 1** esiste solo per la compatibilità. Il servizio Messenger non trasmette i nomi né consente l'invio dei nomi.

 

 




