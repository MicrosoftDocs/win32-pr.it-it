---
title: Come verificare il supporto dei driver
description: In questo argomento viene illustrato come determinare se le funzionalità di multithreading, inclusi gli elenchi di comandi e la creazione di risorse, sono supportate per l'accelerazione hardware.
ms.assetid: f577357c-c2e5-4e58-9870-2e995bdc6782
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae42bbb3eedb76d049479839d497a79db81b5697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992776"
---
# <a name="how-to-check-for-driver-support"></a>Procedura: verificare il supporto dei driver

In questo argomento viene illustrato come determinare se le funzionalità di multithreading, inclusi gli [elenchi di comandi](overviews-direct3d-11-render-multi-thread-command-list.md)e la creazione di [risorse](overviews-direct3d-11-render-multi-thread-intro.md) , sono supportate per l'accelerazione hardware.

È consigliabile per le applicazioni verificare il supporto hardware della grafica del multithreading. Se il driver e l'hardware grafico non supportano la creazione di oggetti multithread, le prestazioni possono essere limitate nei modi seguenti:

-   La creazione di più oggetti (anche di tipi diversi) allo stesso tempo può essere limitata.
-   La creazione di un oggetto durante il rendering dei comandi grafici tramite un [contesto immediato](overviews-direct3d-11-render-multi-thread-render.md) potrebbe essere limitata. Se, ad esempio, l'hardware non supporta il multithreading, un'applicazione deve evitare di creare in un thread in background un oggetto che richiede un tempo molto lungo per la creazione. Un'operazione di creazione che richiede molto tempo può bloccare il rendering del contesto immediato e aumentare il rischio di una balbuzie della frequenza dei fotogrammi visivi.

Il runtime supporta il multithreading e gli elenchi di comandi indipendentemente dal supporto hardware e driver; Se non è disponibile alcun supporto per driver e hardware per gli elenchi multithread o di comando, la funzionalità verrà emulata dal runtime. Per altre informazioni sul multithreading, vedere [Introduzione al multithreading in Direct3D 11](overviews-direct3d-11-render-multi-thread-intro.md).

**Per verificare il supporto dei driver per il multithreading:**

1.  Inizializzare un oggetto interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) . Per impostazione predefinita, il multithreading è abilitato.
2.  Chiamare [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport). Passare il valore di **\_ \_ threading della funzionalità d3d11** al parametro *feature* , passare la struttura di [**\_ \_ \_ Threading dei dati**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) della funzionalità d3d11 al parametro *pFeatureSupportData* e passare le dimensioni della struttura di **\_ \_ \_ Threading dei dati della funzionalità d3d11** al parametro *FeatureSupportDataSize* .
3.  Se il metodo [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) ha esito positivo, la struttura di [**\_ \_ \_ Threading dei dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) passata nel passaggio precedente verrà inizializzata con informazioni sul supporto del multithreading.
    -   Se **DriverConcurrentCreates** è **true**, un driver può creare più di una risorsa contemporaneamente (simultaneamente) su thread diversi.

        Se **DriverCommandLists** è **true**, il driver supporta gli elenchi di comandi. Ovvero, i comandi di rendering eseguiti da un contesto immediato possono essere simultanei con la creazione di oggetti su thread distinti con basso rischio di una balbuzie della frequenza dei fotogrammi.

    -   Se **DriverConcurrentCreates** è **false**, un driver non supporta la creazione simultanea, il che significa che la quantità di concorrenza possibile è estremamente limitata. L'hardware grafico non è in grado di creare oggetti di tipi diversi in thread diversi simultanueously. Inoltre, l'hardware grafico non può usare un contesto immediato per emettere comandi di rendering mentre l'hardware grafico tenta di creare una risorsa in un altro thread.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




