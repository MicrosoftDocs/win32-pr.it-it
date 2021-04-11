---
description: Un provider di rete è una DLL che consente al sistema operativo Windows di supportare un protocollo di rete specifico.
ms.assetid: 21dfa941-72fd-4f2c-8bc4-379ed6ca2a4c
title: Implementazione di un provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97819b033c57feb25cf882f97051785123e2e382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128307"
---
# <a name="implementing-a-network-provider"></a>Implementazione di un provider di rete

Un provider di rete è una DLL che consente al sistema operativo Windows di supportare un protocollo di rete specifico. Questa operazione viene eseguita implementando l'API del provider di rete. Questa API è un set di funzioni che vengono chiamate da [*più provider router*](../secgloss/m-gly.md) (MPR) per comunicare con la rete. Il provider di rete converte quindi queste chiamate in chiamate API specifiche della rete per eseguire l'azione specificata da MPR. In questo modo, il sistema operativo Windows può interagire con i nuovi protocolli di rete senza che sia necessario comprendere le API specifiche della rete.

Per creare un provider di rete, scrivere una DLL che esporta la funzione [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) .

Il supporto delle altre funzioni nell'API del provider di rete è facoltativo. Se il provider di rete non richiede una funzione, la DLL non deve implementarla o fornire un'implementazione stub. Per ulteriori informazioni, vedere gli argomenti relativi alle singole funzioni in [funzioni del provider di rete](authentication-functions.md).

L'eccezione è che se si supporta una delle funzioni di enumerazione seguenti, è necessario supportare anche le altre due funzioni: [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)e [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum).

Le linee guida seguenti descrivono come scrivere un provider di rete che interagisce correttamente con il sistema operativo e il sistema operativo Windows. Laddove possibile, il provider deve rispettare le linee guida seguenti per la velocità, la convalida e il routing.

## <a name="speed"></a>speed

Un provider di rete deve determinare rapidamente se una risorsa di rete è propria. Ciò è dovuto al fatto che è possibile che l'MPR debba scorrere molti provider per trovare il proprietario di una risorsa.

Se il provider di rete non è il proprietario della risorsa, deve restituire immediatamente il \_ \_ codice di stato NETNAME non valido.

È inoltre importante che i provider che supportano [**NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) restituiscono rapidamente i risultati per questa funzione perché viene chiamato mentre winfile sta disegnando l'albero di directory.

## <a name="validation"></a>Convalida

L'ordine di convalida è importante. Un provider di rete deve innanzitutto determinare se la rete è avviata e quindi determinare se il provider di rete e di rete supporta l'operazione. Se, dopo questi controlli, il provider di rete riceve tutte le risorse di rete, deve determinare se è proprietario. Infine, deve convalidare altri parametri.

## <a name="routing"></a>Routing

Se il MPR deve scorrere i provider di rete, tenterà di eseguire tutti i provider fino a quando non si accetta la chiamata. In altre parole, il MPR continua sempre a provare a trovare un provider di rete.

Tuttavia, prende nota del primo errore significativo segnalato da un provider. Errori quali errore \_ NETPATH errato \_ , nome NET errato errore, \_ \_ \_ parametro errore \_ non valido \_ \_ . il livello di errore non valido \_ viene considerato non significativo perché significa semplicemente che il provider non gestisce la risorsa. Tuttavia, se il provider ha esito negativo e si verifica un errore di errore della \_ \_ password o di un altro errore significativo, MPR registra questo errore e continua a scorrere i provider di rete. In generale, durante il routing, se nessun provider accetta la chiamata, l'MPR segnala il primo errore significativo rilevato durante il ciclo dei provider di rete.

Quando si decide quale messaggio di errore restituire, il provider di rete deve tenere conto di questo comportamento di MPR.

## <a name="implementation-note"></a>Nota sull'implementazione

Quando si implementano le DLL del provider di rete, il provider non deve chiamare altre [funzioni di rete di Windows](../wnet/windows-networking-functions.md), [API shell](../shell/samples-usingthumbnailproviders.md)o altre query basate sul percorso UNC che potrebbero causare la reimmissione nel sottosistema MPR. Se si effettuano chiamate di questo tipo da una DLL del provider di rete, l'applicazione o altri componenti del sistema operativo potrebbero riscontrare conflitti, prestazioni insufficienti o deadlock nel sottosistema MPR.

 

 
