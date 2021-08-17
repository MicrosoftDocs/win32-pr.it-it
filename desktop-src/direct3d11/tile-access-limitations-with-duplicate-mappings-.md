---
title: Limitazioni di accesso ai riquadri con mapping duplicati
description: Questa sezione descrive le limitazioni di accesso ai riquadri con mapping duplicati.
ms.assetid: 7A498E0D-9151-4A89-B7C3-C4F476457D17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ea4839b8115ccffe1993d767bc19d2d7c3db0c230aff65f8dd0fd9f74d3cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124119"
---
# <a name="tile-access-limitations-with-duplicate-mappings"></a>Limitazioni di accesso ai riquadri con mapping duplicati

Questa sezione descrive le limitazioni di accesso ai riquadri con mapping duplicati.

## <a name="copying-tiled-resources-with-overlapping-source-and-destination"></a>Copia di risorse affiancate con origine e destinazione sovrapposte

Se nell'area di origine e di destinazione di un'operazione di copia sono presenti mapping duplicati nell'area di copia che si sarebbero sovrapposti anche se entrambe le risorse non fossero risorse affiancate e l'operazione di copia supporti copie sovrapposte, l'operazione di copia si comporterà come se l'origine fosse copiata in un percorso temporaneo prima di andare \* \* alla \* destinazione. Se tuttavia la sovrapposizione non è ovvia (ad esempio le risorse di origine e di destinazione sono diverse, ma i mapping di condivisione o i mapping vengono duplicati su una determinata superficie), i risultati dell'operazione di copia nei riquadri condivisi non sono definiti.

## <a name="copying-to-tiled-resource-with-duplicated-tiles-in-destination-area"></a>Copia nella risorsa affiancata con riquadri duplicati nell'area di destinazione

La copia in una risorsa affiancata con riquadri duplicati nell'area di destinazione produce risultati non definiti in questi riquadri, a meno che i dati stessi non siano identici. riquadri diversi possono scrivere i riquadri in ordini diversi.

## <a name="uav-accesses-to-duplicate-tiles-mappings"></a>Accessi UAV ai mapping di riquadri duplicati

Si supponga che una visualizzazione di accesso non ordinato (UAV) in una risorsa affiancata abbia mapping di riquadri duplicati nella relativa area o con altre risorse associate alla pipeline. L'ordinamento degli accessi a questi riquadri duplicati non è definito se eseguito da thread diversi, così come qualsiasi ordinamento dell'accesso alla memoria agli UAV in generale non è ordinato.

## <a name="rendering-after-tile-mapping-changes-or-content-updates-from-outside-mappings"></a>Rendering dopo modifiche al mapping dei riquadri o aggiornamenti del contenuto da mapping esterni

Se i mapping dei riquadri di una risorsa affiancata sono stati modificati o il contenuto nei riquadri del pool affiancato mappato è stato modificato tramite i mapping di un'altra risorsa affiancata e il rendering della risorsa affiancata verrà eseguito tramite la visualizzazione di destinazione di rendering o la visualizzazione depth stencil, l'applicazione deve cancellare (usando la funzione fissa Clear APIs) o copiare completamente usando le API Copia/Aggiorna i riquadri modificati all'interno dell'area di cui viene eseguito il rendering (mappato o \* \* meno). In caso di errore di cancellazione o copia di un'applicazione in questi casi, le strutture di ottimizzazione hardware per la vista di destinazione di rendering o la vista depth stencil specificata non sono più stanti e comportano risultati di garbage rendering su alcuni componenti hardware e incoerenza tra hardware diverso. Queste strutture di dati di ottimizzazione nascoste usate dall'hardware potrebbero essere locali a singoli mapping e non visibili ad altri mapping alla stessa memoria.

[**L'operazione ID3D11DeviceContext1::ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview) supporta la cancellazione delle visualizzazioni di destinazione di rendering con rettangoli. Per l'hardware che supporta le risorse affiancate, **ClearView** deve supportare anche la cancellazione delle visualizzazioni depth stencil con rettangoli, solo per superfici di profondità (senza stencil). Questa operazione consente alle applicazioni di cancellare solo l'area necessaria di una superficie.

Se un'applicazione deve mantenere il contenuto di memoria esistente delle aree in una risorsa affiancata in cui i mapping sono stati modificati, tale applicazione deve risolvere il requisito chiaro. L'applicazione può eseguire questa operazione salvando prima il contenuto in cui sono stati modificati i mapping dei riquadri (copiandoli in una superficie temporanea, ad esempio usando [**ID3D11DeviceContext2::CopyTiles),**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)emettendo il comando clear richiesto e quindi copiando nuovamente il contenuto. Anche se questa operazione consente di mantenere il contenuto della superficie per il rendering incrementale, lo svantaggio è che le prestazioni di rendering successive sulla superficie potrebbero risultare erre perché le ottimizzazioni del rendering potrebbero essere perse.

Se un riquadro viene mappato in più risorse affiancate contemporaneamente e il contenuto del riquadro viene modificato in qualsiasi modo (rendering, copia e così via) tramite una delle risorse affiancate, se il rendering dello stesso riquadro deve essere eseguito tramite qualsiasi altra risorsa affiancata, il riquadro deve essere cancellato prima come descritto in precedenza.

## <a name="rendering-to-tiles-shared-outside-render-area"></a>Rendering in riquadri condivisi all'esterno dell'area di rendering

Si supponga che venga eseguito il rendering di un'area in una risorsa affiancata e che venga eseguito il mapping anche dei riquadri del pool di riquadri a cui fa riferimento l'area di rendering dall'esterno dell'area di rendering (incluso tramite altre risorse affiancate, contemporaneamente o meno). Non è garantito che i dati sottoposti a rendering in questi riquadri vengano visualizzati correttamente quando vengono visualizzati tramite gli altri mapping, anche se il layout della memoria sottostante è compatibile. Ciò è dovuto alle strutture dei dati di ottimizzazione che possono essere usate dall'hardware che possono essere locali ai singoli mapping per le superfici di cui è possibile eseguire il rendering e non sono visibili ad altri mapping nella stessa posizione di memoria. È possibile aggirare questa restrizione copiando dal mapping di cui è stato eseguito il rendering a tutti gli altri mapping alla stessa memoria a cui è possibile accedere o cancellando tale memoria o copiando altri dati se il contenuto precedente non è più necessario. Anche se questa operazione sembra ridondante, tutti gli altri mapping alla stessa memoria comprendono correttamente come accedere al contenuto e almeno il risparmio di memoria di avere un solo backup di memoria fisica rimane intatto. Inoltre, quando si passa dall'uso di diverse risorse affiancate che condividono mapping (a meno che non si eseere solo la lettura), è necessario chiamare l'API [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) tra le opzioni.

## <a name="rendering-to-tiles-shared-within-render-area"></a>Rendering in riquadri condivisi all'interno dell'area di rendering

Se viene eseguito il rendering di un'area in una risorsa affiancata verso e all'interno dell'area di rendering più riquadri vengono mappati alla stessa posizione del pool di riquadri, i risultati del rendering non sono definiti in tali riquadri.

## <a name="data-compatibility-across-tiled-resources-sharing-tiles"></a>Compatibilità dei dati tra le risorse affiancate che condividono riquadri

Si supponga che più risorse affiancate presentino mapping agli stessi percorsi del pool di riquadri e che ogni risorsa sia usata per accedere agli stessi dati. Questo scenario è valido solo se vengono evitate le altre regole per evitare problemi con le strutture di ottimizzazione hardware, vengono effettuate chiamate appropriate a [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) e le risorse affiancate sono compatibili tra loro. Quest'ultimo viene descritto qui in termini di significato per le risorse affiancate che condividono riquadri come incompatibili. Le condizioni di incompatibilità di accesso agli stessi dati tra mapping di riquadri duplicati sono l'uso di dimensioni di superficie o formato diversi o differenze nella presenza di flag di associazione di destinazione di rendering o depth stencil sulle risorse. La scrittura in memoria con un tipo di mapping produce risultati non definiti se successivamente si legge o si esegue il rendering tramite un mapping da una risorsa incompatibile. Se gli altri mapping di condivisione delle risorse vengono inizializzati per la prima volta con nuovi dati (riciclo della memoria per uno scopo diverso), l'operazione di lettura o rendering successiva va bene perché i dati non vengono travasati da interpretazioni incompatibili. Tuttavia, è necessario chiamare l'API **TiledResourceBarrier** quando si passa da un accesso a mapping incompatibili come questo.

Se la destinazione di rendering o depth stencil di binding non è impostata su nessuna delle risorse che condividono i mapping tra loro, esistono molte meno restrizioni. Purché il formato e i tipi di superficie (ad esempio Texture2D) siano gli stessi, è possibile condividere i riquadri. I diversi formati compatibili sono casi come le superfici BC e le dimensioni equivalenti non compresse a \* 32 bit o a 16 bit per formato componente, ad esempio BC6H e R32G32B32A32. Molti formati a 32 bit per elemento possono essere associati anche a R32 \_ \* (R10G10B10A2, \_ \* R8G8B8A8, \_ \* B8G8R8A8 \_ \* ,B8G8R8X8X8,R16G16 \_ \* \_ \* ); questa operazione è sempre stata consentita per le risorse non affiancate.

La condivisione tra riquadri imballati e non imballati è buona se i formati sono compatibili e i riquadri sono riempiti con un colore a tinta unita.

Infine, se non sono comuni le risorse che condividono i mapping dei riquadri, ad eccezione del fatto che nessuno ha flag di associazione di destinazione di rendering o depth stencil, solo la memoria riempita con 0 può essere condivisa in modo sicuro. il mapping verrà visualizzato come qualsiasi decodifica 0 per la definizione del formato di risorsa specificato (in genere solo 0).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso della pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




