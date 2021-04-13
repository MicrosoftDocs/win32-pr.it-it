---
description: Utilizzo dell'utilità Checkv4.exe per modificare l'applicazione IPv4 per supportare IPv6.
ms.assetid: 36b72e4f-133d-4d96-a3c9-86a852d3a479
title: Utilizzo dell'utilità Checkv4.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc9eca96b2138f9950b157a4b7690dc382f273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569074"
---
# <a name="using-the-checkv4exe-utility"></a>Utilizzo dell'utilità Checkv4.exe

> [!IMPORTANT]
> L'utilità *Checkv4.exe* non è disponibile in Windows Software Development Kit (SDK) per Windows 8, né nelle versioni successive del Windows SDK.

L'utilità *Checkv4.exe* è progettata per fornire un partner di porting del codice. utilità che consente di eseguire i passaggi della codebase, identificare i potenziali problemi o evidenziare il codice che potrebbe trarre vantaggio dalle funzioni o dalle strutture che supportano IPv6 e apporta consigli. Con l'utilità Checkv4.exe, l'attività di modifica di un'applicazione IPv4 esistente per il supporto di IPv6 diventa molto più semplice.

L'utilità *Checkv4.exe* viene installata come parte di Microsoft Windows Software Development Kit (SDK) rilasciata per gli SDK di Windows Vista e versioni successive (fino a, ma non incluso, Windows Software Development Kit (SDK) per Windows 8).

Una versione precedente dell'utilità di *Checkv4.exe* con funzionalità più limitate è stata resa disponibile anche come parte della precedente Microsoft IPv6 Technology Preview per Windows 2000.

Nelle sezioni seguenti viene descritto come utilizzare l'utilità *Checkv4.exe* , quindi viene illustrato l'approccio consigliato per la modifica di un'applicazione IPv4 esistente per il supporto di IPv6.

## <a name="recommendations-for-running-checkv4exe"></a>Suggerimenti per l'esecuzione di Checkv4.exe

-   L'utilità *Checkv4.exe* è semplice. È sufficiente eseguire *Checkv4.exe* dalla riga di comando con il nome del file che si desidera controllare come parametro. *Checkv4.exe* analizza il file e fornisce commenti e suggerimenti sulla posizione in cui sono presenti problemi di portabilità IPv6 in tale file. L'inserimento del *Checkv4.exe* nel percorso del computer rende molto più semplice l'esecuzione dell'utilità *Checkv4.exe* da qualsiasi punto della struttura di directory del codice sorgente. Se ad esempio si inserisce *Checkv4.exe* in% windir%, è possibile avviare *Checkv4.exe* da qualsiasi directory nel computer senza includere il percorso.

-   Al prompt dei comandi eseguire il comando seguente per analizzare il file SIMPLEC. c:

    **Checkv4 SIMPLEC. c**

    Si noti che alcune raccomandazioni apportate dall'utilità *Checkv4.exe* richiedono strutture disponibili solo nelle versioni recenti del file di intestazione *Ws2tcpip. h* , ad esempio la **struttura \_ IN6 di SOCKADDR** . Questi file di intestazione sono inclusi nel Windows SDK rilasciato per Windows Vista e versioni successive. Questi file di intestazione sono inclusi anche nella versione precedente del Software Development Kit (SDK) della piattaforma rilasciata per Windows Server 2003. Questi file di intestazione sono inclusi anche come parte di un abbonamento MSDN o per il download.

    Lo screenshot seguente mostra i risultati dell'uso dell'utilità *Checkv4.exe* nel file SIMPLEC. c incluso nell'appendice a:

    ![checkv4.exe segnala incompatibilità IPv6 nel file SIMPLEC. c](images/portingguide002.jpg)

    Lo screenshot seguente mostra i risultati dell'uso dell'utilità *Checkv4.exe* nel file simples. c, incluso anche nell'Appendice A:

    ![checkv4.exe segnala incompatibilità IPv6 nel file simples. c](images/portingguide003.jpg)

## <a name="the-application-modification-process-where-to-start"></a>Processo di modifica dell'applicazione: da dove iniziare

È disponibile una procedura consigliata associata all'aggiunta di funzionalità IPv6 alle applicazioni. Questa sequenza è utile perché consente agli sviluppatori di assicurarsi che vengano eseguiti tutti i passaggi necessari per modificare un'applicazione IPv4 esistente per il supporto di IPv6. Alcune applicazioni possono richiedere un'attenzione più approfondita a una di queste sequenze; un servizio di sistema, ad esempio, potrebbe probabilmente presentare problemi di interfaccia utente minori rispetto a un FTP (Graphical file Transfer Program).

**Per modificare le applicazioni IPv4 per supportare IPv6**

1.  Correzione di strutture e dichiarazioni per abilitare la compatibilità IPv6 e IPv4.
2.  Modificare le chiamate di funzione per sfruttare i vantaggi delle funzioni abilitate per IPv6, ad esempio le funzioni [**funzione getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .
3.  Esaminare il codice sorgente per l'utilizzo di indirizzi IPv4 hardcoded, ad esempio l'indirizzo di loopback, o l'utilizzo di altre stringhe letterali.
4.  Eseguire una revisione completa dell'interfaccia utente, incluse le finestre di dialogo informative. Indicare se è appropriato per le applicazioni abilitate per IPv6 specificare o fornire informazioni basate su indirizzi IP.
5.  Determinare se l'applicazione si basa su protocolli sottostanti, ad esempio RPC, e apportare le modifiche a livello di codice appropriate per gestire gli indirizzi IPv6.
6.  Usare il flag della fase di compilazione IPV6STRICT durante la compilazione di applicazioni in Windows XP e versioni successive. Questo flag genera un errore di compilazione del codice incompatibile, come indicato di seguito:

    Le applicazioni Windows Sockets 1. x con codice non compatibile non vengono compilate e restituiscono il messaggio di errore "WINSOCK2 required".

    Le applicazioni Windows Sockets 2. x con codice incompatibile generano un errore in fase di compilazione per ogni istanza di codice incompatibile. Un messaggio di errore viene generato nel formato seguente:

    `[file name] ([line number]) : [error message] '[symbol]_IPV6INCOMPATIBLE'`

    Ad esempio:

    `sample.c(8) : error C2065: 'gethostbyaddr_IPV6INCOMPATIBLE' : undeclared identifier`

 

 



