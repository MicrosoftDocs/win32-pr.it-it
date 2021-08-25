---
title: Dispositivi (grafica Direct3D 11)
description: Questa sezione descrive gli oggetti dispositivo e contesto di dispositivo Direct3D 11.
ms.assetid: 61d1ea92-e657-4931-8475-74a3123c72f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e77cfd255c43cc902f2583fe22575bef2567609f43b6f893984e99dec713532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851121"
---
# <a name="devices-direct3d-11-graphics"></a>Dispositivi (grafica Direct3D 11)

Un dispositivo Direct3D alloca ed elimina gli oggetti, esegue il rendering delle primitive e comunica con un driver di grafica e l'hardware. In Direct3D 11 un dispositivo viene separato in un oggetto dispositivo per la creazione di risorse e in un oggetto contesto di dispositivo, che esegue il rendering. Questa sezione descrive gli oggetti dispositivo e contesto di dispositivo Direct3D 11.

Gli oggetti creati da un dispositivo non possono essere usati direttamente con altri dispositivi. Usare una risorsa condivisa per condividere i dati tra più dispositivi, con il vincolo che un oggetto condiviso può essere usato solo dal dispositivo che lo ha creato.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                                                         | Descrizione                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introduzione a un dispositivo in Direct3D 11](overviews-direct3d-11-devices-intro.md)<br/>                                                                 | Il modello a oggetti Direct3D 11 separa la funzionalità di creazione e rendering delle risorse in un dispositivo e in uno o più contesti. questa separazione è progettata per facilitare il multithreading.<br/>                                                  |
| [Livelli software](overviews-direct3d-11-devices-layers.md)<br/>                                                                                        | Il runtime Direct3D 11 viene costruito con livelli, a partire dalla funzionalità di base nel core e creando funzionalità facoltative e di supporto per gli sviluppatori nei livelli esterni. Questa sezione descrive le funzionalità di ogni livello.<br/> |
| [Limitazioni relative alla creazione di dispositivi WARP e di riferimento](overviews-direct3d-11-devices-limitations.md)<br/>                                                   | Esistono alcune limitazioni per la creazione di dispositivi WARP e Di riferimento in Direct3D 10.1 e Direct3D 11.0. In questo argomento vengono illustrate queste limitazioni.<br/>                                                                                              |
| [Direct3D 11 su hardware di livello inferiore](overviews-direct3d-11-devices-downlevel.md)<br/>                                                                   | Questa sezione illustra come Direct3D 11 è progettato per supportare hardware nuovo ed esistente, da DirectX 9 a DirectX 11.<br/>                                                                                                             |
| [Uso dei dati delle funzionalità Direct3D 11 per integrare i livelli di funzionalità Direct3D](using-direct3d-optional-features-to-supplement-direct3d-feature-levels.md)<br/> | Informazioni su come controllare il supporto dei dispositivi per le funzionalità facoltative, incluse le funzionalità aggiunte nelle versioni recenti di Windows.<br/>                                                                                                           |



 

## <a name="how-to-topics-about-devices"></a>Argomenti relativi alle procedure sui dispositivi



| Argomento                                                                                                                                                                                                                                                                                                    | Descrizione                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="How_To__Create_a_Reference_Device"></span><span id="how_to__create_a_reference_device"></span><span id="HOW_TO__CREATE_A_REFERENCE_DEVICE"></span>[Procedura: Creare un dispositivo di riferimento](overviews-direct3d-11-devices-create-ref.md)<br/>                                                 | Descrive come creare un dispositivo di riferimento.<br/>                            |
| <span id="How_To__Create_a_WARP_Device"></span><span id="how_to__create_a_warp_device"></span><span id="HOW_TO__CREATE_A_WARP_DEVICE"></span>[Procedura: Creare un dispositivo WARP](overviews-direct3d-11-devices-create-warp.md)<br/>                                                                    | Descrive come creare un dispositivo WARP.<br/>                                 |
| <span id="How_To__Create_a_Swap_Chain"></span><span id="how_to__create_a_swap_chain"></span><span id="HOW_TO__CREATE_A_SWAP_CHAIN"></span>[Procedura: Creare una catena di scambio](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                                                  | Viene descritto come creare una catena di scambio.<br/>                                  |
| <span id="How_To__Enumerate_Adapters"></span><span id="how_to__enumerate_adapters"></span><span id="HOW_TO__ENUMERATE_ADAPTERS"></span>[Procedura: Enumerare gli adattatori](overviews-direct3d-11-devices-enum.md)<br/>                                                                                   | Viene descritto come enumerare le schede di visualizzazione fisiche.<br/>              |
| <span id="How_To__Get_Adapter_Display_Modes"></span><span id="how_to__get_adapter_display_modes"></span><span id="HOW_TO__GET_ADAPTER_DISPLAY_MODES"></span>[Procedura: Ottenere le modalità di visualizzazione dell'adapter](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                                           | Viene descritto come ottenere le funzionalità di visualizzazione supportate di un adattatore.<br/> |
| <span id="How_To__Create_a_Device_and_Immediate_Context"></span><span id="how_to__create_a_device_and_immediate_context"></span><span id="HOW_TO__CREATE_A_DEVICE_AND_IMMEDIATE_CONTEXT"></span>[Procedura: Creare un dispositivo e un contesto immediato](overviews-direct3d-11-devices-initialize.md)<br/> | Descrive come inizializzare un dispositivo.<br/>                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

 





