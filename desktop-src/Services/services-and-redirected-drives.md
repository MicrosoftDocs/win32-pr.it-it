---
description: Un servizio (o qualsiasi processo in esecuzione in un contesto di sicurezza diverso) che deve accedere a una risorsa remota deve usare il nome Universal Naming Convention (UNC) per accedere alla risorsa.
ms.assetid: 2582259d-077c-4089-9a87-1a377994f0bd
title: Servizi e unità reindirizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b1435e69ded3bf13a0869a0b9ad2b90bb4682c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968380"
---
# <a name="services-and-redirected-drives"></a>Servizi e unità reindirizzate

Un servizio (o qualsiasi processo in esecuzione in un contesto di sicurezza diverso) che deve accedere a una risorsa remota deve usare il nome Universal Naming Convention (UNC) per accedere alla risorsa. Il servizio deve disporre dei privilegi appropriati per accedere alla risorsa. Se un servizio lato server utilizza una connessione RPC, è necessario abilitare la delega sul server remoto.

Le lettere di unità non sono globali per il sistema. Ogni sessione di accesso riceve un proprio set di lettere di unità da a a Z. Pertanto, le unità reindirizzate non possono essere condivise tra i processi in esecuzione con account utente diversi. Inoltre, un servizio (o qualsiasi processo in esecuzione all'interno della propria sessione di accesso) non è in grado di accedere alle lettere di unità stabilite all'interno di un'altra sessione di accesso.

Un servizio non deve accedere direttamente alle risorse locali o di rete tramite lettere di unità mappate, né chiamare il comando **net use** per eseguire il mapping delle lettere di unità in fase di esecuzione. Il comando **net use** non è consigliato per diversi motivi:

-   I mapping delle unità sono presenti tra i contesti di accesso, quindi se un'applicazione è in esecuzione nel contesto dell' [account LocalService](localservice-account.md), qualsiasi altro servizio in esecuzione in tale contesto potrebbe avere accesso all'unità mappata.
-   Se il servizio fornisce credenziali esplicite a un comando **net use** , tali credenziali potrebbero essere inavvertitamente condivise all'esterno dei limiti del servizio. Il servizio deve invece usare la [rappresentazione client](/windows/desktop/SecAuthZ/client-impersonation) per rappresentare l'utente.
-   Più servizi in esecuzione nello stesso contesto possono interferire tra loro. Se entrambi i servizi eseguono un **utilizzo netto** esplicito e forniscono contemporaneamente le stesse credenziali, un servizio avrà esito negativo con un errore "già connesso".

Inoltre, un servizio non deve utilizzare le [funzioni di rete di Windows](/windows/desktop/WNet/windows-networking-functions) per gestire le lettere di unità mappate. Sebbene le funzioni WNet possano restituire correttamente, il comportamento risultante non è quello previsto. Quando il sistema stabilisce un'unità reindirizzata, viene archiviata in base ai singoli utenti. Solo l'utente è in grado di gestire l'unità reindirizzata. Il sistema tiene traccia delle unità reindirizzate in base all'ID di sicurezza (SID) di accesso dell'utente. Il SID di accesso è un identificatore univoco per la sessione di accesso dell'utente. Un singolo utente può avere più sessioni di accesso simultanee nel sistema.

Se un servizio è configurato per l'esecuzione con un account utente, il sistema crea sempre una nuova sessione di accesso per l'utente e avvia il servizio nella nuova sessione di accesso. Pertanto, un servizio non è in grado di gestire i mapping delle unità stabiliti nelle altre sessioni dell'utente.

**Windows Server 2003:** In un computer con più interfacce di rete (ovvero un computer multihomed), possono verificarsi ritardi fino a 60 secondi quando si utilizzano i percorsi UNC per accedere ai file archiviati in un server SMB (Server Message Block) remoto. Per ulteriori informazioni, vedere l' [articolo 890553](https://support.microsoft.com/kb/890553) della Knowledge base della guida e del supporto tecnico.

 

 
