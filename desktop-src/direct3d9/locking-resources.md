---
description: Bloccare una risorsa significa concedere alla CPU l'accesso alla propria risorsa di archiviazione.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Blocco delle risorse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6cdb7cde646bd5073bc0c5b574694be69f05f1bf15d8c5c08e00b7182cfe044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799494"
---
# <a name="locking-resources-direct3d-9"></a>Blocco delle risorse (Direct3D 9)

Bloccare una risorsa significa concedere alla CPU l'accesso alla propria risorsa di archiviazione. Per le risorse sono definite le opzioni di blocco seguenti:

-   D3DLOCK \_ DISCARD
-   D3DLOCK \_ READONLY
-   D3DLOCK \_ NOOVERWRITE
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ NO \_ DIRTY \_ UPDATE

Per informazioni dettagliate sui flag di blocco e sul modo in cui sono correlati a risorse specifiche, vedere le pagine di riferimento sui singoli metodi di blocco delle risorse. Gli sviluppatori di applicazioni devono notare che i flag D3DLOCK \_ DISCARD, D3DLOCK READONLY e \_ D3DLOCK \_ NOOVERWRITE sono solo hint. In fase di esecuzione non viene verificata la presenza di applicazioni che stanno seguendo la funzionalità specificata da questi flag. Un'applicazione che specifica D3DLOCK READONLY ma quindi scrive \_ nella risorsa deve prevedere risultati non definiti. In generale, l'uso dei flag di blocco, inclusi i flag di utilizzo di blocco, non è garantito nelle versioni successive e può causare una riduzione significativa delle prestazioni.

Un'operazione di blocco è seguita da un'operazione di sblocco. Ad esempio, dopo aver bloccato una trama, l'applicazione successivamente rinuncia all'accesso diretto alle trame bloccate sbloccandole. Oltre a concedere l'accesso al processore, tutte le altre operazioni che coinvolgono tale risorsa vengono serializzate per la durata di un blocco. È consentito un solo blocco per una risorsa, anche per le aree non sovrapposte, e nessuna operazione dell'acceleratore su una superficie può essere in corso mentre un'operazione di blocco è in sospeso su tale superficie.

Ogni interfaccia di risorsa dispone di metodi per bloccare i buffer contenuti. Ogni risorsa trama può anche bloccare una sotto-parte di tale risorsa. Le risorse 2D (superfici) consentono il blocco dei rettangoli secondari e le risorse di volume consentono il blocco di sotto-volumi o caselle. Ogni metodo di blocco restituisce una struttura che contiene un puntatore all'archiviazione che contiene la risorsa e i valori che rappresentano le distanze tra righe o piani di dati, a seconda del tipo di risorsa. Per informazioni dettagliate, vedere gli elenchi di metodi per le interfacce delle risorse. Il puntatore restituito punta sempre al byte superiore sinistro nelle sottoaree bloccate.

Quando si lavora con i buffer di indice e vertice, è possibile effettuare più chiamate di blocco. Tuttavia, è necessario assicurarsi che il numero di chiamate di blocco corrisponda al numero di chiamate di sblocco.

Il DXTn archivia i pixel in blocchi 4x4 codificati e può essere bloccato solo su limiti 4x4.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



