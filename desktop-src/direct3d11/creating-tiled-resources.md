---
title: Creazione di risorse affiancate
description: '\_ \_ \_ Quando si crea una risorsa, le risorse affiancate vengono create specificando il flag di varie risorse di d3d11.'
ms.assetid: DED2B70C-1E95-4A85-A818-FD32165FBF6C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e2c0e457bfd8534d3a42c6f658095b3349572
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/13/2019
ms.locfileid: "104398183"
---
# <a name="creating-tiled-resources"></a>Creazione di risorse affiancate

Quando si crea una risorsa, le risorse affiancate vengono create specificando il flag di [**\_ \_ varie \_ risorse di d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .

Limitazioni relative al momento in cui è possibile usare le [**\_ risorse d3d11 \_ \_ affiancate**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) per creare una risorsa sono descritte in [parametri di creazione di risorse affiancati](tiled-resource-creation-parameters.md).

Una risorsa di archiviazione non affiancata viene allocata nel sistema grafico quando viene creata la risorsa. Ad esempio, quando si chiama [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) per creare una matrice di trame 2D, il sistema grafico alloca spazio di archiviazione per tali trame 2D. Quando viene creata una risorsa affiancata, il sistema grafico non alloca lo spazio di archiviazione per il contenuto della risorsa. Al contrario, quando un'applicazione crea una risorsa affiancata, il sistema grafico esegue una prenotazione dello spazio degli indirizzi solo per l'area della superficie affiancata e quindi consente il controllo del mapping dei riquadri da parte dell'applicazione. Il "mapping" di un riquadro è semplicemente la posizione fisica in memoria a cui fa riferimento un riquadro logico in una risorsa (o **null** per un riquadro non mappato). Non confondere questo concetto con la nozione di mapping di una risorsa Direct3D per l'accesso alla CPU, che nonostante l'uso dello stesso nome sia completamente indipendente. Sarà possibile definire e modificare il mapping di ogni riquadro singolarmente, in base alle esigenze, sapendo che non è necessario eseguire il mapping di tutti i riquadri per una superficie alla volta, in modo da usare in modo efficace la quantità di memoria disponibile.

In questa sezione vengono fornite ulteriori informazioni su come creare risorse affiancate.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mapping inclusi in un pool di riquadri](mappings-are-into-a-tile-pool.md)<br/>                                     | Quando viene creata una risorsa con il flag di [**\_ \_ varie \_ sezioni della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) , i riquadri che compongono la risorsa provengono da punti in un pool di sezioni. Un pool di sezioni è un pool di memoria (supportato da una o più allocazioni dietro le quinte, non visibili dall'applicazione). <br/> |
| [Parametri per la creazione di risorse affiancate](tiled-resource-creation-parameters.md)<br/>                           | Esistono alcuni vincoli sul tipo di risorse Direct3D che è possibile creare con il flag di [**\_ \_ varie \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) risorse di d3d11. In questa sezione vengono forniti i parametri validi per la creazione di risorse affiancate.<br/>                                                |
| [Spazio degli indirizzi disponibile per le risorse affiancate](address-space-available-for-tiled-resources.md)<br/>         | In questa sezione viene specificato lo spazio degli indirizzi virtuale disponibile per le risorse affiancate. <br/>                                                                                                                                                                                                                           |
| [Parametri di creazione dei pool di riquadri](tile-pool-creation-parameters.md)<br/>                                     | Usare i parametri in questa sezione per definire i pool di sezioni tramite l'API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) . <br/>                                                                                                                                                                              |
| [Condivisione tra processi e dispositivi affiancati per le risorse](tiled-resource-cross-process-and-device-sharing.md)<br/> | I pool di sezioni possono essere condivisi con altri processi proprio come le risorse tradizionali. Le risorse affiancate che fanno riferimento a pool di sezioni non possono essere condivise tra dispositivi e processi. Tuttavia, i processi distinti possono creare le proprie risorse affiancate che eseguono il mapping ai pool di sezioni condivisi tra le risorse affiancate. <br/>          |
| [Operazioni disponibili sulle risorse affiancate](operations-available-on-tiled-resources.md)<br/>                 | In questa sezione sono elencate le operazioni che è possibile eseguire sulle risorse affiancate.<br/>                                                                                                                                                                                                                                             |
| [Operazioni disponibili nei pool di riquadri](operations-available-on-tile-pools.md)<br/>                           | Questa sezione elenca le operazioni che è possibile eseguire nei pool di sezioni.<br/>                                                                                                                                                                                                                                                  |
| [Come affiancare l'area di una risorsa affiancata](how-a-tiled-resource-s-area-is-tiled.md)<br/>                       | Quando si crea una risorsa affiancata, le dimensioni, le dimensioni degli elementi di formato e il numero di sezioni mipmap e/o matrici (se applicabile) determinano il numero di riquadri necessari per eseguire il backup dell'intera superficie di attacco. <br/>                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse affiancate](tiled-resources.md)
</dt> </dl>

 

 





