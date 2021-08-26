---
title: Funzionalità di campionamento delle trame delle risorse affiancate
description: Questa sezione descrive le funzionalità di campionamento delle trame delle risorse affiancate.
ms.assetid: E56737CE-C468-4D3C-84EE-E8EB2AB6F505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1356b274b5e101a730e3de92a6cdf98b1f293515228fb420a77642f4603757c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119477"
---
# <a name="tiled-resources-texture-sampling-features"></a>Funzionalità di campionamento delle trame delle risorse affiancate

Questa sezione descrive le funzionalità di campionamento delle trame delle risorse affiancate.

## <a name="requirements-of-tiled-resources-texture-sampling-features"></a>Requisiti delle funzionalità di campionamento delle trame delle risorse affiancate

Le funzionalità di campionamento trame descritte di seguito richiedono il livello [2](tier-2.md) di supporto delle risorse affiancate.

## <a name="shader-feedback-about-mapped-areas"></a>Commenti e suggerimenti sugli shader sulle aree mappate

Qualsiasi istruzione shader che legge e/o scrive in una risorsa affiancata causa la registrazione delle informazioni sullo stato. Questo stato viene esposto come valore restituito aggiuntivo facoltativo in ogni istruzione di accesso alle risorse che entra in un registro temporaneo a 32 bit. Il contenuto del valore restituito è opaco. Ciò significa che la lettura diretta da parte del programma shader non è consentita. È tuttavia possibile usare la [**funzione CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) per estrarre le informazioni sullo stato.

## <a name="fully-mapped-check"></a>Controllo con mapping completo

La [**funzione CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta lo stato restituito da un accesso alla memoria e indica se è stato eseguito il mapping di tutti i dati a cui si accede nella risorsa. **CheckAccessFullyMapped** restituisce true (0xFFFFFFFF) se è stato eseguito il mapping dei dati o false (0x00000000) se i dati sono stati non mappati.

Durante le operazioni di filtro, a volte il peso di un determinato texel finisce per essere 0,0. Un esempio è un campione lineare con coordinate di trama che rientrano direttamente in un centro texel: altri 3 texel (che possono variare in base all'hardware) contribuiscono al filtro, ma con peso 0. Questi texel di peso 0 non contribuiscono affatto al risultato del filtro, quindi se rientrano in riquadri **NULL,** non vengono conteggiati come accessi non mappati. Si noti che la stessa garanzia vale per i filtri di trama che includono più livelli mip; Se i texel in una delle mipmap non sono mappati, ma il peso su tali texel è 0, questi texel non vengono conteggiati come accesso non mappato.

Quando si esegue il campionamento da un formato che include meno di 4 componenti (ad esempio DXGI FORMAT R8 UNORM), tutti i \_ \_ \_ texel   che rientrano nei riquadri NULL comportano la visualizzazione di un accesso con mapping NULL indipendentemente dai componenti effettivamente a cui lo shader esamina il risultato. Ad esempio, la lettura da R8 UNORM e la maschera del risultato della lettura nello shader con .gba/.yzw non sembrano dover leggere affatto la \_ trama. Tuttavia, se l'indirizzo texel è un **riquadro mappato NULL,** l'operazione viene comunque conteggiata come accesso alla mappa **NULL.**

Lo shader può controllare lo stato e intraprendere qualsiasi corso di azione desiderato in caso di errore. Ad esempio, un corso di azione può essere la registrazione di "mancati" (ad esempio tramite la scrittura UAV) e/o l'emissione di un'altra lettura con un loD grossolano noto per essere mappato. Un'applicazione potrebbe voler tenere traccia anche degli accessi riusciti per avere un'idea della parte del set mappato di riquadri a cui è stato eseguito l'accesso.

Una complicazione per la registrazione è che non esiste alcun meccanismo per segnalare l'esatto set di riquadri a cui sarebbe stato eseguito l'accesso. L'applicazione può fare ipotesi conservativa in base alla conoscenza delle coordinate usate per l'accesso, nonché usando l'istruzione LOD (ad [**esempio, tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)), che restituisce il calcolo loD hardware.

Un'altra complicazione è che molti accessi saranno agli stessi riquadri, quindi si verificherà una grande quantità di registrazione ridondante ed eventualmente una situazione di conflitti nella memoria. Potrebbe essere utile se all'hardware fosse possibile non preoccuparsi di segnalare gli accessi ai riquadri se sono stati segnalati in precedenza in un'altra posizione. È possibile che lo stato di tale rilevamento possa essere reimpostato dall'API (probabilmente in corrispondenza dei limiti del frame).

## <a name="per-sample-minlod-clamp"></a>Chiusura MinLOD per campione

Per evitare che gli shader evitino le aree nelle risorse affiancate con mipmapped che sono note come non mappate, la maggior parte delle istruzioni di shader che comportano l'uso di un campionatore (filtro) ha una nuova modalità che consente allo shader di passare un parametro di chiusura MinLOD minLOD float32 aggiuntivo al campione di trama. Questo valore si trova nello spazio dei numeri mipmap della vista, a differenza della risorsa sottostante.

L'hardware esegue [**max**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-max)(fShaderMinLODClamp,fComputedLOD) nella stessa posizione nel calcolo LOD in cui si verifica il blocco MinLOD per risorsa, che è anche un **valore massimo**().

Se il risultato dell'applicazione del gruppo LOD per campione e di qualsiasi altro gruppo LOD definito nel campionatore è un set vuoto, il risultato è lo stesso risultato di accesso fuori dai limiti del dispositivo minLOD per risorsa: 0 per i componenti nel formato di superficie e i valori predefiniti per i componenti mancanti.

L'istruzione LOD (ad [**esempio, tex2Dlod),**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)che precede il blocco minLOD per campione descritto qui, restituisce sia un LOD con e senza chiusura. Il lod di lod di chiusura restituito da questa istruzione LOD riflette tutte le soglie, incluso il blocco per risorsa, ma non un blocco per campione. Il blocco per campione è comunque controllato e noto dallo shader, quindi l'autore dello shader può applicarlo manualmente al valore restituito dell'istruzione LOD, se necessario.

## <a name="minmax-reduction-filtering"></a>Filtro di riduzione minimo/massimo

Le applicazioni possono scegliere di gestire le proprie strutture di dati che le informano dell'aspetto dei mapping per una risorsa affiancata. Un esempio potrebbe essere una superficie che contiene un texel per contenere le informazioni per ogni riquadro in una risorsa affiancata. È possibile archiviare il primo loD mappato in una determinata posizione del riquadro. Con un campionamento accurato di questa struttura di dati in modo simile a quello previsto per il campionamento della risorsa affiancata, è possibile individuare il valore loD minimo di cui è stato eseguito il mapping completo per l'intero footprint del filtro della trama. Per semplificare questo processo, Direct3D 11.2 introduce una nuova modalità di campionamento per utilizzo generico, filtro min/max.

L'utilità del filtro min/max per il rilevamento dei valori LOD può essere utile per altri scopi, ad esempio per filtrare le superfici di profondità.

Il filtro di riduzione minimo/massimo è una modalità per i campionatori che recupera lo stesso set di texel che verrebbe recuperato da un filtro di trama normale. Ma invece di unire i valori per produrre una risposta, restituisce il valore min() o max() dei texel recuperati, in base al componente (ad esempio, il numero minimo di tutti i valori R, separatamente dal minimo di tutti i valori G e così via).

Le operazioni min/max seguono le regole di precisione aritmetica Direct3D. L'ordine dei confronti non è importante.

Durante le operazioni di filtro che non sono min/max, a volte il peso di un determinato texel finisce per essere 0,0. Un esempio è un campione lineare con coordinate di trama che rientrano direttamente in un centro texel. Altri 3 texel (che possono variare in base all'hardware) contribuiscono al filtro, ma con peso 0. Per uno di questi texel con peso 0 per un filtro non minimo/massimo, se il filtro è min/max, questi texel non contribuiscono ancora al risultato (e i pesi non influiscono altrimenti sull'operazione di filtro min/max).

L'elenco completo delle modalità di filtro viene visualizzato [**nell'enumerazione FILTER D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter) con MINIMUM e MAXIMUM nei valori di enumerazione.

Il supporto per questa funzionalità dipende dal [supporto di livello 2](tier-2.md) per le risorse affiancate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso della pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 