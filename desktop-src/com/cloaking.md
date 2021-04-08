---
title: Mascheramento (COM)
description: Il cloaking è una funzionalità di sicurezza COM che determina l'identità proiettata dal client verso il server durante la rappresentazione.
ms.assetid: 5b97d9d6-8fa9-4da2-8351-64772227d9a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588651cfa37def4e174ef0f2fdba9b79b0c60ca8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "103885886"
---
# <a name="cloaking-com"></a>Mascheramento (COM)

Il cloaking è una funzionalità di sicurezza COM che determina l'identità proiettata dal client verso il server durante la rappresentazione. Quando è impostato il mascheramento, il server intermedio maschera la propria identità e presenta l'identità del client al server che chiama per conto del client. Fondamentalmente l'identità client visualizzata dal server è l'identità associata al proxy. L'identità del proxy è determinata da diversi fattori, uno dei quali è il tipo di mascheramento impostato (se presente). Il cloaking non è supportato dal provider di sicurezza Schannel.

Negli argomenti seguenti vengono fornite ulteriori informazioni sul mascheramento:

-   [Tipi di mascheramento](#types-of-cloaking)
-   [Effetti della mascheramento sull'identità client](#how-cloaking-affects-client-identity)
-   [Impostazione mascheramento](#setting-cloaking)
-   [Mascheramento e livelli di rappresentazione](#cloaking-and-impersonation-levels)
-   [Scenari di mascheramento](#cloaking-scenarios)
-   [Argomenti correlati](#related-topics)

## <a name="types-of-cloaking"></a>Tipi di mascheramento

Esistono due tipi di mascheramento: mascheramento *statico* e mascheramento *dinamico* :

-   Con il cloaking statico ( \_ \_ mascheramento statico EOAC), il server Visualizza il token del thread dalla prima chiamata da un client al server. Per la prima chiamata, se l'identità del proxy è stata impostata in precedenza durante una chiamata a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), viene utilizzata l'identità del proxy. Tuttavia, se l'identità del proxy non è stata impostata in precedenza, viene utilizzato il token del thread. Se non è presente alcun token del thread, viene utilizzato il token di processo. Per tutte le chiamate future, viene utilizzata l'identità impostata nella prima chiamata.
-   Con il mascheramento dinamico (EOAC \_ Dynamic \_ cloaking), a ogni chiamata il token del thread corrente (se è presente un token del thread) viene usato per determinare l'identità del client. Se non è presente alcun token del thread, viene utilizzato il token di processo. Ciò significa che i server chiamati per conto del client durante la rappresentazione visualizzano l'identità del client COM che ha originato la chiamata, che corrisponde in genere al comportamento desiderato. Naturalmente, affinché la rappresentazione abbia esito positivo, il client deve avere dato all'autorità del server la rappresentazione impostando un livello di rappresentazione appropriato. Per ulteriori informazioni, vedere [livelli di rappresentazione](impersonation-levels.md). Questo tipo di mascheramento è costoso.

## <a name="how-cloaking-affects-client-identity"></a>Effetti della mascheramento sull'identità client

Quando viene eseguita una chiamata crittografata e il server richiede al client la relativa identità, in genere ottiene l'identità associata al proxy. (A volte il servizio di autenticazione esegue una traduzione dall'identità reale, ma in genere l'identità del proxy è l'identità visualizzata dal server). Il proxy presenta un'identità al server che dipende dal tipo di mascheramento impostato e da altri fattori.

Per riepilogare, l'identità del client è una funzione del flag di mascheramento impostato, il token di processo, la presenza o l'assenza di un token del thread e se l'identità del proxy è stata impostata in precedenza. La tabella seguente illustra l'identità del proxy risultante (identità client) quando questi fattori variano.



| Flag di mascheramento                     | Presenza token di thread  | Identità del proxy impostata in precedenza | Identità proxy (identità client)                    |
|------------------------------------|------------------------|-------------------------------|-----------------------------------------------------|
| Mascheramento non impostato<br/>        | Non importa<br/>  | Non importa<br/>         | Token di processo o identità di autenticazione<br/> |
| \_ \_ mascheramento statico EOAC<br/>  | Presente<br/>     | No<br/>                 | Token del thread<br/>                             |
| \_ \_ mascheramento statico EOAC<br/>  | Presente<br/>     | Sì<br/>                | Identità del proxy corrente<br/>                   |
| \_ \_ mascheramento statico EOAC<br/>  | Non presente<br/> | No<br/>                 | Token di processo<br/>                            |
| \_ \_ mascheramento statico EOAC<br/>  | Non presente<br/> | Sì<br/>                | Identità del proxy corrente<br/>                   |
| \_ \_ mascheramento dinamico EOAC<br/> | Presente<br/>     | Non importa<br/>         | Token del thread<br/>                             |
| \_ \_ mascheramento dinamico EOAC<br/> | Non presente<br/> | Non importa <br/>        | Token di processo<br/>                            |



 

Il diagramma di flusso seguente illustra come viene determinata l'identità del proxy in situazioni diverse.

![Diagramma che mostra il flusso per determinare l'identità del proxy.](images/9e8409b7-8475-4824-bdff-cf6b09c139c5.png)

## <a name="setting-cloaking"></a>Impostazione mascheramento

Il cloaking viene impostato come flag di funzionalità in una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), che imposta il mascheramento per l'intero processo. La funzionalità di mascheramento viene quindi impostata fino a quando il client non la modifica tramite una chiamata a IClientSecurity::[**Seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (o a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)), che imposta il mascheramento per il proxy.

Per impostazione predefinita, il mascheramento non è impostato. Per impostarlo, passare il cloaking \_ statico EOAC \_ o \_ \_ il mascheramento dinamico EOAC al parametro *pCapabilities* in [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o in un set di elementi. [](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)

Quando il mascheramento statico viene abilitato con [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), ogni proxy preleva un token (thread o processo) la prima volta che si effettua una chiamata sul proxy. Quando il mascheramento statico viene abilitato con il [**Seblankt**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), il proxy preleva il token nel thread in quel momento. Se non è disponibile alcun token di thread quando viene chiamato il metodo **Seblankt** , il token di processo viene usato per l'identità del proxy. In sostanza, il **Seblankt** corregge l'identità del proxy.

Con il mascheramento dinamico, l'identità del proxy viene determinata allo stesso modo, indipendentemente dal fatto che il mascheramento dinamico venga impostato utilizzando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o con il set di [**celle**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). Il token del thread corrente viene usato se ne esiste uno; in caso contrario, viene utilizzato il token di processo.

Se il mascheramento viene impostato per l'intero processo tramite una chiamata a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e si desidera effettuare chiamate con il token di processo, non rappresentare durante l'esecuzione delle chiamate.

## <a name="cloaking-and-impersonation-levels"></a>Mascheramento e livelli di rappresentazione

Come indicato in precedenza, la funzionalità di mascheramento determina quale identità viene presentata a un server durante la rappresentazione. Il mascheramento consente a un server di proiettare un'identità diversa da quella relativa a un altro server che chiama per conto del client. Il livello di rappresentazione indica la quantità di autorità che il client ha assegnato al server.

La rappresentazione senza mascheramento funziona, ma potrebbe non essere la scelta migliore perché, in alcuni casi, è necessario che il server finale conosca l'identità del chiamante iniziale. Questa operazione non può essere eseguita senza usare il cloaking perché è difficile assicurarsi che solo i client autorizzati possano accedere a un computer remoto. Quando si utilizza la rappresentazione senza mascheramento, l'identità presentata a un server downstream è quella del processo chiamante immediato.

Tuttavia, il cloaking non è utile senza rappresentazione. Il cloaking è opportuno solo quando il client ha impostato un livello di rappresentazione di rappresenta o delegato. (Con livelli di rappresentazione più bassi, il server non può effettuare chiamate mascherate). Il fatto che il cloaking abbia esito positivo dipende dal numero di limiti del computer incrociato e dal livello di rappresentazione, che indica la quantità di autorità che il server deve agire per conto del client.

In alcune situazioni, è opportuno che il server imposti il mascheramento quando il client imposta il livello di rappresentazione sul livello di rappresentazione del livello di rappresentazione C di RPC \_ \_ \_ \_ . Tuttavia, sono valide alcune limitazioni. Se il client originale imposta il livello di rappresentazione su rappresentazione a \_ livello di RPC C \_ Imp \_ \_ , il server intermedio (che funge da client nello stesso computer) può mascherare in un solo limite di computer. Ciò è dovuto al fatto che un token di rappresentazione a livello di rappresentazione può essere passato attraverso un solo limite del computer. Una volta superato il limite del computer, è possibile accedere solo alle risorse locali. L'identità presentata al server dipende dal tipo di mascheramento impostato. Se non è impostato alcun mascheramento, l'identità presentata a un server sarà quella del processo che effettua la chiamata immediata.

Per mascherare i limiti di più computer, è necessario specificare sia un flag di funzionalità di mascheramento appropriato che una rappresentazione a livello di delegato. Con questo tipo di rappresentazione, le credenziali locali e di rete del client vengono assegnate al server, pertanto il token di rappresentazione può superare un numero qualsiasi di limiti del computer. Anche in questo caso, l'identità presentata al server dipende dal tipo di mascheramento impostato. Se non è impostato alcun mascheramento con rappresentazione a livello di delegato, l'identità presentata a un server è quella del processo che effettua la chiamata.

Si supponga, ad esempio, che l'elaborazione di una chiamata a B e che B chiami C. B abbia impostato il mascheramento e che il livello di rappresentazione sia impostato su Impersonate. Se A, B e C si trovano nello stesso computer, passando il token di rappresentazione da a a B e quindi a C funzionerà. Tuttavia, se A e C si trovano nello stesso computer e B non lo è, il passaggio del token funzionerà tra A e B, ma non da B a C. La chiamata da B a C avrà esito negativo perché B non è in grado di chiamare C durante il mascheramento. Tuttavia, se un oggetto imposta il livello di rappresentazione su Delegate, il token può essere passato da B a C e la chiamata potrebbe avere esito positivo.

## <a name="cloaking-scenarios"></a>Scenari di mascheramento

Nella figura seguente, Process A calls B, chiama C, chiama D quando il mascheramento non è impostato. Di conseguenza, ogni processo intermedio rileva l'identità del processo che lo ha chiamato.

![Diagramma che mostra il processo quando il mascheramento non è impostato.](images/0d2eb6cf-97d6-4c4e-b97e-abad854b1120.png)

Con il mascheramento statico, il server Visualizza l'identità del proxy impostata durante la prima chiamata dal client al server. Nella figura seguente viene illustrato un esempio dell'identità del proxy da impostare durante una chiamata da B a C. In una chiamata successiva il processo D rileva l'identità di B quando il mascheramento statico viene impostato da B e C.

![Diagramma che illustra il processo di mascheramento statico.](images/520938e0-c4a6-4ac1-937d-02baf2007a27.png)

Con il mascheramento dinamico, l'identità del chiamante durante la rappresentazione è basata sul token del thread corrente, se presente. Nella figura seguente viene illustrata la situazione in cui B e C impostano il mascheramento dinamico e D Visualizza l'identità di un, nonostante una chiamata precedente da B a C.

![Diagramma che illustra il processo di mascheramento dinamico.](images/d0848465-82f3-4d5a-851e-566d7800ada0.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Delega e rappresentazione](delegation-and-impersonation.md)
</dt> </dl>

 

