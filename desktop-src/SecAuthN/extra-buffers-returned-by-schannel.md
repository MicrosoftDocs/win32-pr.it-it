---
description: Schannel dispone di un set di comportamenti ben definito per le informazioni incomplete o superflue incluse nei buffer di input per queste funzioni.
ms.assetid: 5fad1e76-6520-4ff7-b2b0-2cc2061062a1
title: Buffer aggiuntivi restituiti da Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c9ce7a468b1b04389ad19f91785b64fb50e74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317081"
---
# <a name="extra-buffers-returned-by-schannel"></a>Buffer aggiuntivi restituiti da Schannel

Le informazioni devono essere inviate tra il client e il server mentre viene stabilito un [*contesto di sicurezza*](/windows/desktop/SecGloss/s-gly) e successivamente perché i messaggi protetti vengono scambiati usando le funzionalità di crittografia e decrittografia fornite da Schannel. Per eseguire queste attività, vengono usate le funzioni seguenti:

-   [**AcceptSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
-   [**InitializeSecurityContext (generale)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
-   [**DecryptMessage (generale)**](/windows/win32/api/sspi/nf-sspi-decryptmessage)

Schannel dispone di un set di comportamenti ben definito per le informazioni incomplete o superflue incluse nei buffer di input per queste funzioni. Le informazioni vengono scambiate tra il client e il server nel modo seguente:

1.  L'entità locale interagisce con Schannel chiamando una funzione SSPI e passando le informazioni. In genere, le informazioni sono state ricevute dalla parte remota.
2.  La funzione restituisce un codice di stato e i buffer di output contenenti informazioni.
3.  A seconda del codice di stato, i buffer di output vengono inviati alla parte remota per mezzo di un meccanismo di comunicazione.
4.  La parte remota legge le informazioni inviate dall'entità locale.
5.  Il ciclo si ripete, con le entità locali e remote interscambiate. (L'entità remota chiama una funzione SSPI e passa le informazioni lette nel passaggio precedente).

Tutto funziona come previsto quando il buffer di input per la funzione SSPI contiene esattamente le informazioni necessarie. Tuttavia, a causa della natura orientata al flusso di alcuni protocolli di comunicazione, questo potrebbe non essere il caso. un blocco di informazioni ricevute da un'entità remota può contenere meno dati di quelli richiesti o più dati di quelli che possono essere elaborati da Schannel in una singola chiamata di funzione.

Se il buffer di input contiene informazioni insufficienti, le funzioni restituiscono un \_ \_ messaggio incompleto al secondo E \_ . Il chiamante deve ottenere dati aggiuntivi dalla parte remota e chiamare di nuovo la funzione.

Quando i buffer di input contengono troppe informazioni, Schannel non lo considera come un errore. La funzione elabora la maggior parte dell'input possibile e restituisce il codice di stato per l'attività di elaborazione. Schannel indica inoltre la presenza di informazioni non elaborate nei buffer di input restituendo un buffer di output di tipo SECBUFFER \_ extra. Il test dei buffer di output per questo tipo di buffer è l'unico modo per rilevare questa situazione. Il campo **cbBuffer** della struttura del buffer aggiuntiva indica il numero di byte di input non elaborati.

> [!Note]  
> Il campo **pvBuffer** del buffer aggiuntivo non contiene una copia dei dati in eccesso.

 

Se si riceve un buffer aggiuntivo da una funzione SSPI, è necessario rimuovere le informazioni già elaborate dal buffer di input e chiamare di nuovo la funzione. SChannel può, e spesso, restituisce solo il buffer aggiuntivo e nient'altro nei buffer di output.

 

 
