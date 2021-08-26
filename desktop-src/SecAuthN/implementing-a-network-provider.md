---
description: Un provider di rete è una DLL che consente al Windows operativo di supportare un protocollo di rete specifico.
ms.assetid: 21dfa941-72fd-4f2c-8bc4-379ed6ca2a4c
title: Implementazione di un provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4776bd97b9528bd04bbda25b88e0ff45a8f911429bb573e62dbbb8581abdfbac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015981"
---
# <a name="implementing-a-network-provider"></a>Implementazione di un provider di rete

Un provider di rete è una DLL che consente al Windows operativo di supportare un protocollo di rete specifico. A tale scopo, implementa l'API del provider di rete. Questa API è un set di funzioni [*chiamate MPR (Multiple Provider Router)*](../secgloss/m-gly.md) per comunicare con la rete. Il provider di rete converte quindi queste chiamate in chiamate API specifiche della rete per eseguire l'azione specificata dalla MPR. In questo modo, il Windows operativo può interagire con nuovi protocolli di rete senza dover comprendere le API specifiche della rete.

Per creare un provider di rete, scrivere una DLL che esporta la [**funzione NPGetCaps.**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps)

Il supporto delle altre funzioni nell'API del provider di rete è facoltativo. Se il provider di rete non richiede una funzione, la DLL non deve implementarla o fornire un'implementazione stub. Per altre informazioni, vedere gli argomenti relativi alle singole funzioni in [Funzioni del provider di rete](authentication-functions.md).

L'eccezione è che se si supporta una delle funzioni di enumerazione seguenti, è necessario supportare anche le altre due funzioni: [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)e [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum).

Le linee guida seguenti descrivono come scrivere un provider di rete che interagisce bene con la MPR e Windows sistema operativo. Quando possibile, il provider deve rispettare le linee guida seguenti per velocità, convalida e routing.

## <a name="speed"></a>speed

Un provider di rete deve determinare rapidamente se una risorsa di rete è propria. Ciò è dovuto al fatto che l'MPR potrebbe essere necessario scorrere molti provider per trovare il proprietario di una risorsa.

Se il provider di rete non è proprietario della risorsa, deve restituire immediatamente il codice di stato WN \_ BAD \_ NETNAME.

È anche importante che i provider che supportano [**NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) restituiranno rapidamente i risultati per questa funzione perché viene chiamata mentre WinFile disegna l'albero della directory.

## <a name="validation"></a>Convalida

L'ordine di convalida è importante. Un provider di rete deve innanzitutto determinare se la rete è avviata e quindi determinare se la rete e il provider di rete supportano l'operazione. Se, dopo questi controlli, il provider di rete riceve le risorse di rete, deve determinare se ne è proprietario. Infine, deve convalidare altri parametri.

## <a name="routing"></a>Routing

Se l'MPR deve scorrere i provider di rete, tenterà tutti i provider fino a quando uno non accetta la chiamata. In altre parole, la MPR continua sempre a cercare un provider di rete.

Prende tuttavia nota del primo errore significativo segnalato da un provider. Gli errori come ERROR \_ BAD \_ NETPATH, ERROR \_ BAD NET \_ \_ NAME, ERROR INVALID PARAMETER, ERROR INVALID \_ LEVEL \_ \_ \_ sono considerati irrilevanti perché significano semplicemente che il provider non gestisce la risorsa. Tuttavia, se il provider ha esito negativo con l'errore ERROR INVALID PASSWORD o un altro errore significativo, MPR registra questo errore e continua a scorrere \_ \_ i provider di rete. In generale, quando si esegue il routing, se nessun provider accetta la chiamata, l'MPR segnala il primo errore significativo riscontrato durante il ciclo attraverso i provider di rete.

Il provider di rete deve prendere in considerazione questo comportamento della MPR quando decide quale messaggio di errore restituire.

## <a name="implementation-note"></a>Nota sull'implementazione

Quando si implementano DLL del provider di rete, il provider non deve chiamare in altre funzioni di rete [di Windows,](../wnet/windows-networking-functions.md)API [shell](../shell/samples-usingthumbnailproviders.md)o altre query basate su percorso UNC che potrebbero causare il rientro nel sottosistema MPR. Se si effettuano chiamate di questo tipo da una DLL del provider di rete, l'applicazione o altri componenti del sistema operativo potrebbero verificarsi problemi di prestazioni o deadlock all'interno del sottosistema MPR.

 

 
