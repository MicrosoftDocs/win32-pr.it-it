---
title: Funzionalità di campionamento della trama delle risorse affiancate
description: Questa sezione descrive le funzionalità di campionamento delle trame di risorse affiancate.
ms.assetid: E56737CE-C468-4D3C-84EE-E8EB2AB6F505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd46c96219e54aea6990e91de8e340fdca5e32b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728727"
---
# <a name="tiled-resources-texture-sampling-features"></a>Funzionalità di campionamento della trama delle risorse affiancate

Questa sezione descrive le funzionalità di campionamento delle trame di risorse affiancate.

## <a name="requirements-of-tiled-resources-texture-sampling-features"></a>Requisiti delle funzionalità di campionamento della trama delle risorse affiancate

Le funzionalità di campionamento di trama descritte di seguito richiedono il livello [2](tier-2.md) del supporto delle risorse affiancate.

## <a name="shader-feedback-about-mapped-areas"></a>Feedback dello shader sulle aree mappate

Qualsiasi istruzione shader che legge e/o scrive in una risorsa affiancata causa la registrazione delle informazioni sullo stato. Questo stato viene esposto come valore restituito aggiuntivo facoltativo per ogni istruzione di accesso alle risorse che entra in un registro temporaneo a 32 bit. Il contenuto del valore restituito è opaco. Ovvero la lettura diretta dal programma shader non è consentita. È tuttavia possibile usare la funzione [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) per estrarre le informazioni sullo stato.

## <a name="fully-mapped-check"></a>Controllo con mapping completo

La funzione [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) interpreta lo stato restituito da un accesso alla memoria e indica se è stato eseguito il mapping di tutti i dati a cui è stato eseguito il mapping nella risorsa. **CheckAccessFullyMapped** restituisce true (0xFFFFFFFF) se i dati sono stati mappati o false (0x00000000) se non è stato eseguito il mapping dei dati.

Durante le operazioni di filtro, a volte il peso di un determinato Texel è 0,0. Un esempio è un esempio lineare con coordinate di trama che rientrano direttamente in un centro Texel: 3 altri Texel (quelli che possono variare in base all'hardware) contribuiscono al filtro, ma con 0 peso. I Texel in peso 0 non contribuiscono al risultato del filtro, pertanto se si verificano riquadri **null** , non vengono conteggiati come accessi non mappati. Si noti che la stessa garanzia si applica ai filtri di trama che includono più livelli MIP; Se i Texel in uno dei mipmap non sono mappati, ma il peso su tali Texel è 0, questi Texel non vengono conteggiati come accesso non mappato.

Quando si esegue il campionamento da un formato con meno di 4 componenti (ad esempio DXGI \_ Format \_ R8 \_ UNORM), i Texel che rientrino nei riquadri **null** comportano l'accesso con mapping **null** , indipendentemente dai componenti che lo shader esamina effettivamente nel risultato. Se ad esempio si esegue la lettura da R8 \_ UNORM e si maschera il risultato della lettura nello shader con. GBA/. yzw, non dovrebbe essere necessario leggere la trama. Tuttavia, se l'indirizzo Texel è un riquadro mappato **null** , l'operazione viene comunque conteggiata come un accesso con mapping **null** .

Lo shader può controllare lo stato e intraprendere qualsiasi corso di azione desiderato in caso di errore. Una linea di azione, ad esempio, può essere la registrazione dei "mancati" (ad esempio tramite la scrittura di UAV) e/o l'emissione di un'altra lettura clampata a un LOD più grossolano noto per il mapping. Un'applicazione potrebbe voler tenere traccia degli accessi riusciti, in modo da ottenere un'idea della parte del set di riquadri mappato a cui è stato effettuato l'accesso.

Una complicazione per la registrazione non esiste alcun meccanismo per segnalare il set esatto di riquadri a cui sarebbe stato effettuato l'accesso. L'applicazione può prendere ipotesi conservative basate sulla conoscenza delle coordinate usate per l'accesso, nonché sull'uso dell'istruzione LOD (ad esempio, [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)) che restituisce il calcolo dell'hardware LOD.

Un'altra complicazione consiste nel fatto che molti accessi saranno agli stessi riquadri, pertanto si verificherà una grande quantità di registrazione ridondante e probabilmente la contesa sulla memoria. Potrebbe essere utile se l'hardware potesse avere la possibilità di non dover segnalare gli accessi ai riquadri se sono stati segnalati altrove. Probabilmente lo stato di tale traccia può essere reimpostato dall'API (probabilmente in corrispondenza dei limiti del frame).

## <a name="per-sample-minlod-clamp"></a>MinLOD Clamp per campione

Per consentire agli shader di evitare aree in mipmap le risorse affiancate note come non mappate, la maggior parte delle istruzioni dello shader che comportano l'uso di un campionatore (filtro) hanno una nuova modalità che consente allo shader di passare un parametro di Clamp float32 MinLOD aggiuntivo all'esempio di trama. Questo valore si trova nello spazio dei numeri mipmap della vista, in contrapposizione alla risorsa sottostante.

L'hardware esegue il valore [**Max**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-max)(FShaderMinLODClamp, fComputedLOD) nella stessa posizione del calcolo di LOD in cui si verifica il morsetto MinLOD per risorsa, che è anche un valore **Max**().

Se il risultato dell'applicazione del clamp per singolo campione e di tutti gli altri morsetti LOD definiti nel campionatore è un set vuoto, il risultato è lo stesso risultato dell'accesso al di fuori limite come minLOD Clamp per risorsa: 0 per i componenti nel formato di superficie e i valori predefiniti per i componenti mancanti.

L'istruzione LOD (ad esempio, [**tex2Dlod**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-tex2dlod)), che precede il morsetto minLOD per campione descritto in questo argomento, restituisce un valore di LOD bloccato e non bloccato. Il valore di LOD bloccato restituito da questa istruzione LOD riflette tutti i bloccaggi, incluso il morsetto per risorsa, ma non un morsetto per campione. Il morsetto per campione è comunque controllato e noto dallo shader, quindi l'autore dello shader può applicare manualmente tale morsetto al valore restituito dell'istruzione LOD, se lo si desidera.

## <a name="minmax-reduction-filtering"></a>Filtro riduzione min/max

Le applicazioni possono scegliere di gestire le proprie strutture di dati che informano l'aspetto dei mapping per una risorsa affiancata. Un esempio potrebbe essere una superficie che contiene un Texel per contenere informazioni per ogni riquadro in una risorsa affiancata. È possibile archiviare il primo elemento LOD mappato in una posizione del riquadro specificata. Con un attento campionamento di questa struttura di dati in modo analogo alla risorsa affiancata, è possibile individuare il valore minimo di LOD di cui è stato eseguito il mapping completo per un footprint di filtro di trama intero. Per semplificare questo processo, Direct3D 11,2 introduce una nuova modalità di campionamento per utilizzo generico, ovvero un filtro minimo/massimo.

L'utilità di filtro min/max per il rilevamento di LOD può essere utile per altri scopi, ad esempio, forse il filtro delle superfici di profondità.

Il filtro di riduzione min/max è una modalità nei sampler che recupera lo stesso set di Texel che un normale filtro di trama recupererà. Tuttavia, anziché fondere i valori per produrre una risposta, restituisce il valore min () o Max () dei Texel recuperati, in base ai singoli componenti, ad esempio il numero minimo di tutti i valori R, separatamente dal minimo di tutti i valori G e così via.

Le operazioni min/max seguono le regole di precisione aritmetica Direct3D. L'ordine dei confronti non è rilevante.

Durante le operazioni di filtro che non sono min/max, a volte il peso di un determinato Texel è 0,0. Un esempio è un esempio lineare con coordinate di trama che rientrano direttamente in un centro Texel-3 altri Texel (quelli che possono variare in base all'hardware) contribuiscono al filtro, ma con 0 peso. Per uno di questi Texel che sarebbe 0 peso su un filtro non min/max, se il filtro è min/max, questi Texel non contribuiscono ancora al risultato (e i pesi non influiscono sull'operazione di filtro min/max).

L'elenco completo delle modalità di filtro viene visualizzato nell'enumerazione del [**\_ filtro d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter) con i valori minimo e massimo nei valori di enumerazione.

Il supporto per questa funzionalità dipende dal supporto di [livello 2](tier-2.md) per le risorse affiancate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alla pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 