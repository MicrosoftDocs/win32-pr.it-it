---
title: Creazione di risorse affiancate
description: Le risorse affiancate vengono create specificando il flag D3D11 \_ RESOURCE \_ MISC \_ TILED quando si crea una risorsa.
ms.assetid: DED2B70C-1E95-4A85-A818-FD32165FBF6C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657fc2cca4d5c1d8fce9efba2013d3cd04291efc7f40d44b4ed325e40f843358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752581"
---
# <a name="creating-tiled-resources"></a>Creazione di risorse affiancate

Le risorse affiancate vengono create specificando il flag [**D3D11 \_ RESOURCE \_ MISC \_ TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) quando si crea una risorsa.

Le restrizioni relative all'uso di [**D3D11 \_ RESOURCE \_ MISC \_ TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) per creare una risorsa sono descritte in [Parametri di creazione di risorse affiancate](tiled-resource-creation-parameters.md).

L'archiviazione di una risorsa non affiancata viene allocata nel sistema grafico quando viene creata la risorsa. Ad esempio, quando si chiama [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) per creare una matrice di trame 2D, il sistema grafico alloca spazio di archiviazione per tali trame 2D. Quando viene creata una risorsa affiancata, il sistema grafico non alloca lo spazio di archiviazione per il contenuto della risorsa. Quando invece un'applicazione crea una risorsa affiancata, il sistema grafico effettua una prenotazione dello spazio indirizzi solo per l'area della superficie affiancata e quindi consente il mapping dei riquadri da controllare dall'applicazione. Il "mapping" di un riquadro è semplicemente la posizione fisica in memoria a cui punta un riquadro logico in una risorsa (o **NULL** per un riquadro non mappato). Non confondere questo concetto con il concetto di mapping di una risorsa Direct3D per l'accesso alla CPU, che nonostante l'uso dello stesso nome sia completamente indipendente. Sarà possibile definire e modificare il mapping di ogni riquadro singolarmente in base alle esigenze, sapendo che non è necessario eseguire il mapping di tutti i riquadri per una superficie alla volta, rendendo così efficace l'uso della quantità di memoria disponibile.

Questa sezione fornisce altre informazioni su come creare risorse affiancate.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mapping inclusi in un pool di riquadri](mappings-are-into-a-tile-pool.md)<br/>                                     | Quando viene creata una risorsa con il flag [**D3D11 \_ RESOURCE \_ MISC \_ TILED,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) i riquadri che costituiscono la risorsa provengono da punti alle posizioni in un pool di riquadri. Un pool di riquadri è un pool di memoria (supportato da una o più allocazioni in background, nonvisibile dall'applicazione). <br/> |
| [Parametri di creazione di risorse affiancate](tiled-resource-creation-parameters.md)<br/>                           | Esistono alcuni vincoli sul tipo di risorse Direct3D che è possibile creare con il flag [**D3D11 \_ RESOURCE \_ MISC \_ TILED.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Questa sezione fornisce i parametri validi per la creazione di risorse affiancate.<br/>                                                |
| [Spazio indirizzi disponibile per le risorse affiancate](address-space-available-for-tiled-resources.md)<br/>         | Questa sezione specifica lo spazio degli indirizzi virtuali disponibile per le risorse affiancate. <br/>                                                                                                                                                                                                                           |
| [Parametri di creazione dei pool di riquadri](tile-pool-creation-parameters.md)<br/>                                     | Usare i parametri in questa sezione per definire pool di riquadri tramite l'API [**ID3D11Device::CreateBuffer.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) <br/>                                                                                                                                                                              |
| [Condivisione tra processi e dispositivi di risorse affiancate](tiled-resource-cross-process-and-device-sharing.md)<br/> | I pool di riquadri possono essere condivisi con altri processi, proprio come le risorse tradizionali. Le risorse affiancate che fanno riferimento ai pool di riquadri non possono essere condivise tra dispositivi e processi. Tuttavia, processi separati possono creare le proprie risorse affiancate mappate a pool di riquadri condivisi tra tali risorse affiancate. <br/>          |
| [Operazioni disponibili nelle risorse affiancate](operations-available-on-tiled-resources.md)<br/>                 | Questa sezione elenca le operazioni che è possibile eseguire sulle risorse affiancate.<br/>                                                                                                                                                                                                                                             |
| [Operazioni disponibili nei pool di riquadri](operations-available-on-tile-pools.md)<br/>                           | Questa sezione elenca le operazioni che è possibile eseguire nei pool di riquadri.<br/>                                                                                                                                                                                                                                                  |
| [Come viene affiancata l'area di una risorsa affiancata](how-a-tiled-resource-s-area-is-tiled.md)<br/>                       | Quando si crea una risorsa affiancata, le dimensioni, le dimensioni dell'elemento di formato e il numero di mipmap e/o sezioni di matrice (se applicabile) determinano il numero di riquadri necessari per eseguire il backup dell'intera superficie di attacco. <br/>                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse affiancate](tiled-resources.md)
</dt> </dl>

 

 





