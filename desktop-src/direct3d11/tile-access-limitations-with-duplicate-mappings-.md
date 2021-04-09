---
title: Limitazioni di accesso ai riquadri con mapping duplicati
description: Questa sezione descrive le limitazioni di accesso ai riquadri con mapping duplicati.
ms.assetid: 7A498E0D-9151-4A89-B7C3-C4F476457D17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0909b0d10e286e5f774f6893b692abdeb19d3ef7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044236"
---
# <a name="tile-access-limitations-with-duplicate-mappings"></a>Limitazioni di accesso ai riquadri con mapping duplicati

Questa sezione descrive le limitazioni di accesso ai riquadri con mapping duplicati.

## <a name="copying-tiled-resources-with-overlapping-source-and-destination"></a>Copia di risorse affiancate con origine e destinazione sovrapposte

Se i riquadri nell'area di origine e di destinazione di un'operazione di copia \* hanno mapping duplicati nell'area di copia che verrebbero sovrapposti anche se entrambe le risorse non erano risorse affiancate e l'operazione di copia \* supporta le copie sovrapposte, l'operazione di copia \* si comporterà correttamente (come se l'origine venisse copiata in un percorso temporaneo prima di passare alla destinazione). Tuttavia, se la sovrapposizione non è ovvia (ad esempio, le risorse di origine e di destinazione sono diverse ma i mapping di condivisione o i mapping vengono duplicati su una determinata superficie), i risultati dell'operazione di copia sui riquadri condivisi non sono definiti.

## <a name="copying-to-tiled-resource-with-duplicated-tiles-in-destination-area"></a>Copia in una risorsa affiancata con riquadri duplicati nell'area di destinazione

La copia in una risorsa affiancata con riquadri duplicati nell'area di destinazione produce risultati non definiti in questi riquadri, a meno che i dati stessi non siano identici. riquadri diversi possono scrivere i riquadri in ordini diversi.

## <a name="uav-accesses-to-duplicate-tiles-mappings"></a>Accessi UAV ai mapping dei riquadri duplicati

Si supponga che una visualizzazione di accesso non ordinato (UAV) su una risorsa affiancata includa mapping dei riquadri duplicati nell'area o con altre risorse associate alla pipeline. L'ordinamento degli accessi a questi riquadri duplicati non è definito se eseguito da thread diversi, così come qualsiasi ordine di accesso alla memoria per UAV in generale non è ordinato.

## <a name="rendering-after-tile-mapping-changes-or-content-updates-from-outside-mappings"></a>Rendering dopo modifiche al mapping dei riquadri o aggiornamenti del contenuto da mapping esterni

Se i mapping dei riquadri di una risorsa affiancata sono stati modificati o il contenuto nei riquadri del pool affiancati è stato modificato tramite i mapping di un'altra risorsa affiancata, e la risorsa affiancata verrà sottoposta a rendering tramite la visualizzazione della destinazione di rendering o la visualizzazione depth stencil, l'applicazione deve cancellare (usando le API di cancellazione della funzione fissa) o copiare completamente usando \* \* le API Copy/Update i riquadri modificati nell'area di cui viene eseguito il rendering (mappata o meno). Se un'applicazione non è stata cancellata o copiata in questi casi, le strutture di ottimizzazione hardware per la visualizzazione della destinazione di rendering specificata o la visualizzazione depth stencil risultano obsolete e i risultati del rendering del Garbage Collector comportano l'hardware e l'incoerenza in componenti hardware diversi. Queste strutture di dati di ottimizzazione nascoste utilizzate dall'hardware potrebbero essere locali a singoli mapping e non visibili ad altri mapping alla stessa memoria.

L'operazione [**ID3D11DeviceContext1:: ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview) supporta la cancellazione delle visualizzazioni di destinazione di rendering con rettangoli. Per l'hardware che supporta le risorse affiancate, **ClearView** deve supportare anche la cancellazione di viste depth stencil con rettangoli, solo per le superfici di profondità (senza stencil). Questa operazione consente alle applicazioni di cancellare solo l'area necessaria di una superficie.

Se un'applicazione deve mantenere il contenuto della memoria esistente delle aree di una risorsa affiancata in cui sono stati modificati i mapping, l'applicazione deve aggirare il requisito chiaro. L'applicazione può eseguire questa operazione salvando prima il contenuto in cui i mapping dei riquadri sono stati modificati (copiando questi elementi in una superficie temporanea, ad esempio usando [**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)), eseguendo il comando Clear necessario e quindi copiando il contenuto. Sebbene questa operazione consenta di mantenere il contenuto della superficie per il rendering incrementale, il lato negativo è che le prestazioni di rendering successive sulla superficie potrebbero subire problemi perché le ottimizzazioni del rendering potrebbero andare perse.

Se un riquadro viene mappato a più risorse affiancate allo stesso tempo e il contenuto del riquadro viene modificato in qualsiasi modo (rendering, copia e così via) tramite una delle risorse affiancate, se è necessario eseguire il rendering dello stesso riquadro tramite qualsiasi altra risorsa affiancata, il riquadro deve essere cancellato per primo come descritto in precedenza.

## <a name="rendering-to-tiles-shared-outside-render-area"></a>Rendering nei riquadri condivisi all'esterno dell'area di rendering

Si supponga che venga eseguito il rendering di un'area in una risorsa affiancata in e che ai riquadri del pool di sezioni a cui fa riferimento l'area di rendering venga anche eseguito il mapping a dall'esterno dell'area di rendering (anche tramite altre risorse affiancate, allo stesso tempo o meno). I dati di cui viene eseguito il rendering in questi riquadri non vengono visualizzati correttamente quando vengono visualizzati tramite gli altri mapping, anche se il layout di memoria sottostante è compatibile. Questo fatto è dovuto a strutture di dati di ottimizzazione che possono essere usate da un hardware locale a mapping singoli per le superfici di rendering e non visibili ad altri mapping alla stessa posizione di memoria. È possibile ovviare a questa restrizione copiando dal mapping di cui è stato eseguito il rendering in tutti gli altri mapping alla stessa memoria a cui è possibile accedere oppure deselezionando tale memoria o copiando altri dati nel caso in cui il contenuto precedente non sia più necessario. Anche se questa soluzione ovvia sembra ridondante, tutti gli altri mapping alla stessa memoria comunicano correttamente come accedere al contenuto e almeno il risparmio di memoria dovuto alla presenza di un singolo supporto di memoria fisica rimane intatto. Inoltre, quando si passa dall'uso di risorse affiancate diverse che condividono i mapping (a meno che non solo la lettura), è necessario chiamare l'API [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) tra le opzioni.

## <a name="rendering-to-tiles-shared-within-render-area"></a>Rendering nei riquadri condivisi all'interno dell'area di rendering

Se viene eseguito il rendering di un'area in una risorsa affiancata in e all'interno dell'area di rendering, viene eseguito il mapping di più riquadri alla stessa posizione del pool di sezioni. i risultati del rendering non sono definiti in tali riquadri

## <a name="data-compatibility-across-tiled-resources-sharing-tiles"></a>Compatibilità dei dati tra le risorse affiancate condivisione di riquadri

Si supponga che più risorse affiancate dispongano di mapping per gli stessi percorsi del pool di sezioni e che ogni risorsa venga utilizzata per accedere agli stessi dati. Questo scenario è valido solo se le altre regole per evitare problemi con le strutture di ottimizzazione hardware vengono evitate, le chiamate appropriate a [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) vengono effettuate e le risorse affiancate sono compatibili tra loro. Quest'ultimo viene descritto in termini di cosa significa che le risorse affiancate condividono i riquadri in modo che siano incompatibili. Le condizioni di incompatibilità per l'accesso agli stessi dati nei mapping dei riquadri duplicati sono l'uso di dimensioni o formati di superficie diversi oppure le differenze nella presenza della destinazione di rendering o dei flag di binding depth stencil sulle risorse. La scrittura nella memoria con un tipo di mapping produce risultati non definiti se successivamente si esegue la lettura o il rendering tramite un mapping da una risorsa incompatibile. Se gli altri mapping di condivisione delle risorse vengono inizializzati per la prima volta con nuovi dati (riciclo della memoria per uno scopo diverso), l'operazione di lettura o di rendering successiva è corretta perché i dati non vengono sottoposto a emorragia in interpretazioni incompatibili. Tuttavia, è necessario chiamare l'API **TiledResourceBarrier** quando si passa dall'accesso a mapping incompatibili come questo.

Se la destinazione di rendering o il flag di binding depth stencil non è impostato su una delle risorse che condividono i mapping tra loro, le restrizioni sono molto inferiori. Se il formato e i tipi di superficie, ad esempio Texture2D, sono uguali, i riquadri possono essere condivisi. Formati diversi che sono compatibili sono casi come \* le aree BC e il formato di 32 bit o 16 bit non compresso di dimensioni equivalenti, ad esempio BC6H e R32G32B32A32. Molti formati a 32 bit per elemento possono essere associati a un alias con R32 \_ \* (R10G10B10A2 \_ \* , R8G8B8A8 \_ \* , B8G8R8A8 \_ \* , B8G8R8X8 \_ \* , R16G16 \_ \* ). questa operazione è sempre consentita per le risorse non affiancate.

La condivisione tra riquadri compressi e non compressi è un'ammenda se i formati sono compatibili e i riquadri sono riempiti con colore a tinta unita.

Infine, se non è presente alcuna informazione comune sulle risorse che condividono i mapping dei riquadri, tranne per il fatto che nessuno ha una destinazione di rendering o depth stencil flag di binding, è possibile condividere in modo sicuro solo la memoria con 0. il mapping verrà visualizzato come qualsiasi altro 0 decodificato in per la definizione del formato di risorsa specificato (in genere solo 0).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alla pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




