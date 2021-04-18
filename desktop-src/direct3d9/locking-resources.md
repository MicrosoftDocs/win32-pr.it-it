---
description: Il blocco di una risorsa significa concedere l'accesso alla CPU alla relativa archiviazione.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Blocco di risorse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304072"
---
# <a name="locking-resources-direct3d-9"></a>Blocco di risorse (Direct3D 9)

Il blocco di una risorsa significa concedere l'accesso alla CPU alla relativa archiviazione. Per le risorse sono definite le seguenti opzioni di blocco:

-   Eliminazione di D3DLOCK \_
-   D3DLOCK \_ ReadOnly
-   Nosovrascrive D3DLOCK \_
-   \_NOSYSLOCK D3DLOCK
-   D3DLOCK \_ nessun \_ \_ aggiornamento Dirty

Per informazioni dettagliate sui flag di blocco e sulla relativa correlazione con risorse specifiche, vedere le pagine di riferimento sui singoli metodi di blocco delle risorse. Gli sviluppatori di applicazioni devono tenere presente che i \_ flag D3DLOCK scarta, D3DLOCK \_ ReadOnly e D3DLOCK overwrite \_ sono solo hint. Il tempo di esecuzione non verifica che le applicazioni stiano seguendo la funzionalità specificata da questi flag. Un'applicazione che specifica D3DLOCK \_ ReadOnly ma quindi scrive nella risorsa dovrebbe prevedere risultati non definiti. In generale, non è garantito il funzionamento dei flag di blocco, inclusi i flag di utilizzo del blocco, nelle versioni successive e può comportare una riduzione significativa delle prestazioni.

Un'operazione di blocco è seguita da un'operazione di sblocco. Ad esempio, dopo aver bloccato una trama, l'applicazione cede in seguito l'accesso diretto alle trame bloccate, sbloccando tali trame. Oltre alla concessione dell'accesso al processore, qualsiasi altra operazione che interessa tale risorsa viene serializzata per la durata di un blocco. È consentito un solo blocco per una risorsa, anche per le aree non sovrapposte e non è possibile continuare con operazioni di accelerazione in una superficie mentre un'operazione di blocco è in attesa su tale superficie.

Ogni interfaccia di risorsa dispone di metodi per bloccare i buffer contenuti. Ogni risorsa di trama può anche bloccare una parte secondaria di tale risorsa. le risorse 2D (superfici) consentono il blocco di sottorettangoli e le risorse del volume consentono il blocco di sottovolumi o caselle. Ogni metodo Lock restituisce una struttura che contiene un puntatore all'archiviazione che supporta la risorsa e i valori che rappresentano le distanze tra le righe o i piani di dati, a seconda del tipo di risorsa. Per informazioni dettagliate, vedere gli elenchi di metodi per le interfacce delle risorse. Il puntatore restituito punta sempre al byte superiore sinistro nelle aree secondarie bloccate.

Quando si utilizzano i buffer di indice e vertice, è possibile effettuare più chiamate di blocco; Tuttavia, è necessario assicurarsi che il numero di chiamate di blocco corrisponda al numero di chiamate di sblocco.

Il DXTn archivia i pixel nei blocchi 4x4 codificati e può essere bloccato solo sui limiti 4x4.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



