---
title: Cloaking (COM)
description: Cloaking è una funzionalità di sicurezza COM che determina l'identità che il client proietta verso il server durante la rappresentazione.
ms.assetid: 5b97d9d6-8fa9-4da2-8351-64772227d9a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5d36ec4561b0cc3290f21f4c46dc338b6df455bc694464812f2274b8c1345f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462981"
---
# <a name="cloaking-com"></a>Cloaking (COM)

Cloaking è una funzionalità di sicurezza COM che determina l'identità che il client proietta verso il server durante la rappresentazione. Quando il cloaking è impostato, il server intermedio maschera la propria identità e presenta l'identità del client al server che chiama per conto del client. Fondamentalmente, l'identità client che viene vista dal server è l'identità associata al proxy. L'identità del proxy è determinata da diversi fattori, uno dei quali è il tipo di cloaking impostato (se presente). Cloaking non è supportato dal provider di sicurezza Schannel.

Gli argomenti seguenti forniscono altre informazioni sul cloaking:

-   [Tipi di cloaking](#types-of-cloaking)
-   [Impatto del cloaking sull'identità del client](#how-cloaking-affects-client-identity)
-   [Impostazione del cloaking](#setting-cloaking)
-   [Cloaking e livelli di rappresentazione](#cloaking-and-impersonation-levels)
-   [Scenari di cloaking](#cloaking-scenarios)
-   [Argomenti correlati](#related-topics)

## <a name="types-of-cloaking"></a>Tipi di cloaking

Esistono due tipi di cloaking: *cloaking statico* e *cloaking* dinamico:

-   Con cloaking statico (CLOAKING STATICO EOAC), il server vede il token del thread dalla prima chiamata da \_ \_ un client al server. Per la prima chiamata, se l'identità del proxy è stata impostata in precedenza durante una chiamata a [**CoSetProxyBlanket,**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)viene usata tale identità proxy. Tuttavia, se l'identità del proxy non è stata impostata in precedenza, viene usato il token del thread. Se non è presente alcun token di thread, viene usato il token di processo. Per tutte le chiamate future, viene usata l'identità impostata alla prima chiamata.
-   Con cloaking dinamico (CLOAKING DINAMICO EOAC), in ogni chiamata viene usato il token del thread corrente (se è presente un token di thread) per determinare \_ \_ l'identità del client. Se non è presente alcun token di thread, viene usato il token di processo. Ciò significa che i server chiamati per conto del client durante la rappresentazione visualizzano l'identità del client COM che ha originato la chiamata, che in genere rappresenta il comportamento desiderato. Naturalmente, perché la rappresentazione abbia esito positivo, il client deve avere dato all'autorità del server di rappresentare impostando un livello di rappresentazione appropriato. Per altre informazioni, vedere [Livelli di rappresentazione.](impersonation-levels.md) Questo tipo di cloaking è costoso.

## <a name="how-cloaking-affects-client-identity"></a>Impatto del cloaking sull'identità del client

Quando viene effettuata una chiamata crittografata e il server richiede l'identità al client, in genere ottiene l'identità associata al proxy. A volte il servizio di autenticazione esegue una traduzione dall'identità reale, ma in genere l'identità proxy è l'identità visualizzata dal server. Il proxy presenta un'identità al server che dipende dal tipo di cloaking impostato e da altri fattori.

Per riepilogare, l'identità del client è una funzione del set di flag di cloaking, del token di processo, della presenza o dell'assenza di un token di thread e se l'identità del proxy è stata impostata in precedenza. La tabella seguente illustra l'identità proxy risultante (identità client) quando questi fattori variano.



| Flag di cloaking                     | Presenza del token di thread  | Identità proxy impostata in precedenza | Identità proxy (identità client)                    |
|------------------------------------|------------------------|-------------------------------|-----------------------------------------------------|
| Cloaking non impostato<br/>        | Non importa<br/>  | Non importa<br/>         | Elaborare il token o l'identità di autenticazione<br/> |
| \_CLOAKING STATICO DI EOAC \_<br/>  | Presente<br/>     | No<br/>                 | Token di thread<br/>                             |
| \_CLOAKING STATICO DI EOAC \_<br/>  | Presente<br/>     | Sì<br/>                | Identità proxy corrente<br/>                   |
| \_CLOAKING STATICO DI EOAC \_<br/>  | Non presente<br/> | No<br/>                 | Token di elaborazione<br/>                            |
| \_CLOAKING STATICO DI EOAC \_<br/>  | Non presente<br/> | Sì<br/>                | Identità proxy corrente<br/>                   |
| CLOAKING DINAMICO DI EOAC \_ \_<br/> | Presente<br/>     | Non importa<br/>         | Token di thread<br/>                             |
| CLOAKING DINAMICO DI EOAC \_ \_<br/> | Non presente<br/> | Non importa <br/>        | Token di elaborazione<br/>                            |



 

Il diagramma di flusso seguente illustra come viene determinata l'identità del proxy in situazioni diverse.

![Diagramma che mostra il flusso per determinare l'identità del proxy.](images/9e8409b7-8475-4824-bdff-cf6b09c139c5.png)

## <a name="setting-cloaking"></a>Impostazione del cloaking

Cloaking viene impostato come flag di funzionalità in una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), che imposta il cloaking per l'intero processo. La funzionalità di cloaking viene quindi impostata fino a quando il client non la modifica tramite una chiamata a IClientSecurity::[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (o [**a CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)), che imposta il cloaking per il proxy.

Per impostazione predefinita, il cloaking non è impostato. Per impostarlo, passare EOAC \_ STATIC \_ CLOAKING o EOAC \_ DYNAMIC CLOAKING al parametro \_ *pCapabilities* in [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket).

Quando il cloaking statico è abilitato tramite [**CoInitializeSecurity,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)ogni proxy preleva un token (thread o processo) la prima volta che si effettua una chiamata sul proxy. Quando il cloaking statico è abilitato tramite [**SetBlanket,**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)il proxy preleva il token nel thread in quel momento. Se non è disponibile alcun token di thread quando viene chiamato **SetBlanket,** il token di processo viene usato per l'identità del proxy. **Fondamentalmente, SetBlanket** corregge l'identità del proxy.

Con il cloaking dinamico, l'identità del proxy viene determinata nello stesso modo indipendentemente dal fatto che la cloaking dinamica sia impostata tramite [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**con SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). Il token di thread corrente viene usato se presente; In caso contrario, viene usato il token di processo.

Se il cloaking è impostato per l'intero processo tramite una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e si desidera effettuare chiamate con il token di processo, non rappresentare durante l'esecuzione di chiamate.

## <a name="cloaking-and-impersonation-levels"></a>Cloaking e livelli di rappresentazione

Come accennato in precedenza, la funzionalità di cloaking determina l'identità presentata a un server durante la rappresentazione. Cloaking consente a un server di proiettare un'identità diversa dalla propria in un altro server che chiama per conto del client. Il livello di rappresentazione indica la quantità di autorità che il client ha assegnato al server.

La rappresentazione senza cloaking funziona, ma potrebbe non essere la scelta migliore perché, in alcuni casi, il server finale deve conoscere l'identità del chiamante iniziale. Questa operazione non può essere ottenuta senza usare il cloaking perché è difficile garantire che solo i client autorizzati possano accedere a un computer remoto. Quando la rappresentazione viene usata senza cloaking, l'identità presentata a un server downstream è quella del processo chiamante immediato.

Tuttavia, il cloaking non è utile senza rappresentazione. Il cloaking ha senso solo quando il client ha impostato un livello di rappresentazione di rappresentazione o delegato. Con livelli di rappresentazione inferiori, il server non può effettuare chiamate mascherate. L'esito positivo del cloaking dipende dal numero di limiti del computer attraversati e dal livello di rappresentazione, che indica la quantità di autorità che il server deve agire per conto del client.

In alcune situazioni, è opportuno che il server imposta il cloaking quando il client imposta il livello di rappresentazione su RPC \_ C \_ IMP LEVEL \_ \_ IMPERSONATE. Tuttavia, sono in vigore alcune limitazioni. Se il client originale imposta il livello di rappresentazione su RPC \_ C \_ IMP LEVEL \_ IMPERSONATE, il server intermedio (che funge da client nello stesso computer) può mascherarsi attraverso un solo limite \_ del computer. Questo perché un token di rappresentazione a livello di rappresentazione può essere passato attraverso un solo limite di computer. Dopo aver oltrepassato il limite del computer, è possibile accedere solo alle risorse locali. L'identità presentata al server dipende dal tipo di cloaking impostato. Se non viene impostato alcun cloaking, l'identità presentata a un server sarà quella del processo che effettua la chiamata immediata.

Per mascherare più limiti di computer, è necessario specificare sia un flag di funzionalità di cloaking appropriato che una rappresentazione a livello di delegato. Con questo tipo di rappresentazione, le credenziali locali e di rete del client vengono fornite al server, in modo che il token di rappresentazione possa attraversare qualsiasi numero di limiti del computer. Anche in questo caso, l'identità presentata al server dipende dal tipo di cloaking impostato. Se non viene impostato alcun cloaking con rappresentazione a livello di delegato, l'identità presentata a un server è quella del processo che effettua la chiamata.

Si supponga, ad esempio, che il processo A chiami B e che B chiami C. B abbia impostato cloaking e A abbia impostato il livello di rappresentazione su impersonate. Se A, B e C sono nello stesso computer, il passaggio del token di rappresentazione da A a B e quindi a C funzionerà. Tuttavia, se A e C sono nello stesso computer e B non lo è, il passaggio del token funzionerà tra A e B, ma non da B a C. La chiamata da B a C avrà esito negativo perché B non può chiamare C durante la clonazione. Tuttavia, se A imposta il livello di rappresentazione su delegato, il token può essere passato da B a C e la chiamata può avere esito positivo.

## <a name="cloaking-scenarios"></a>Scenari di clonazione

Nella figura seguente, il processo A chiama B, chiama C, chiama D quando la clonazione non è impostata. Di conseguenza, ogni processo intermedio vede l'identità del processo che lo ha chiamato.

![Diagramma che mostra il processo quando la clonazione non è impostata.](images/0d2eb6cf-97d6-4c4e-b97e-abad854b1120.png)

Con la clonazione statica, il server vede l'identità proxy impostata durante la prima chiamata dal client al server. La figura seguente mostra un esempio dell'identità proxy impostata durante una chiamata da B a C. In una chiamata successiva, il processo D vede l'identità di B quando la clonazione statica è impostata da B e C.

![Diagramma che illustra il processo di clonazione statica.](images/520938e0-c4a6-4ac1-937d-02baf2007a27.png)

Con la clonazione dinamica, l'identità del chiamante durante la rappresentazione si basa sul token del thread corrente, se presente. La figura seguente illustra la situazione in cui B e C impostano la clonazione dinamica e D vede l'identità di A, nonostante una chiamata precedente da B a C.

![Diagramma che illustra il processo di cloaking dinamico.](images/d0848465-82f3-4d5a-851e-566d7800ada0.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Delega e rappresentazione](delegation-and-impersonation.md)
</dt> </dl>

 

