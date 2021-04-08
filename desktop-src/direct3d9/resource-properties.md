---
description: Tutte le risorse condividono le seguenti proprietà.
ms.assetid: 6ef6ce68-44fa-4964-8b61-2a37382eda1c
title: Proprietà delle risorse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7b53a23e489b5f53495c5d2626da1e2633c9cf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747167"
---
# <a name="resource-properties-direct3d-9"></a>Proprietà delle risorse (Direct3D 9)

Tutte le risorse condividono le seguenti proprietà.

-   Utilizzo. Modalità di utilizzo di una risorsa, ad esempio, come una trama o una destinazione di rendering.
-   Formattare. Il formato dei dati, ad esempio il formato pixel di una superficie 2D.
-   Piscina. Tipo di memoria in cui viene allocata la risorsa.
-   Digitare  Tipo di risorsa, ad esempio un buffer di vertici o una destinazione di rendering.

Gli utilizzi delle risorse vengono applicati. Un'applicazione che utilizzerà una risorsa in una determinata operazione deve specificare tale operazione in fase di creazione delle risorse. Per un elenco delle costanti di utilizzo definite per le risorse, vedere [**D3DUSAGE**](d3dusage.md).

Le \_ costanti D3DUSAGE RTPATCHES, D3DUSAGE \_ NPATCHES e D3DUSAGE \_ Points indicano al driver che è probabile che i dati presenti in questi buffer vengano usati per le patch triangolari o griglia, le N-patch o gli sprite di punti, rispettivamente. Questi flag vengono forniti se l'hardware non è in grado di eseguire queste operazioni senza elaborazione host. Pertanto, il driver desidera allocare tali superfici nella memoria di sistema in modo che la CPU possa accedervi. Se il driver è in grado di eseguire queste operazioni interamente nell'hardware, può allocare tali superfici nella memoria video o AGP per evitare la copia di un host e migliorare le prestazioni almeno duplici. Si noti che le informazioni fornite da questi flag non sono assolutamente necessarie. Un driver è in grado di rilevare che tali operazioni vengono eseguite sui dati e sposterà nuovamente il buffer nella memoria di sistema per i frame successivi.

Per informazioni dettagliate sui flag di utilizzo e sulla relativa correlazione con risorse specifiche, vedere le pagine di riferimento sui singoli metodi di creazione delle risorse.

Per informazioni sul formato di superficie delle risorse, vedere il tipo enumerato [D3DFORMAT](d3dformat.md) .

La classe di memoria che include i buffer di una risorsa è denominata pool. I valori del pool sono definiti dal tipo enumerato [**D3DPOOL**](./d3dpool.md) . Non è possibile combinare un pool per oggetti diversi contenuti in una singola risorsa, ovvero i livelli MIP in una mipmap e, quando si sceglie un pool per una risorsa, il pool non può essere modificato.

I tipi di risorse vengono impostati in modo implicito in fase di esecuzione quando l'applicazione chiama un metodo di creazione di risorse, ad esempio [**IDirect3DDevice9:: CreateCubeTexture**](/windows/desktop/api). I tipi di risorsa sono definiti dal tipo enumerato [**D3DRESOURCETYPE**](./d3dresourcetype.md) . Le applicazioni possono eseguire query su questi tipi in fase di esecuzione. si prevede tuttavia che la maggior parte degli scenari non richieda il controllo dei tipi in fase di esecuzione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
