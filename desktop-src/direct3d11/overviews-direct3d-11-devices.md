---
title: Dispositivi (grafica Direct3D 11)
description: Questa sezione descrive gli oggetti del dispositivo e del contesto del dispositivo Direct3D 11.
ms.assetid: 61d1ea92-e657-4931-8475-74a3123c72f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dda010b3801952e90514fac6307556f8f6fbaff
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104993677"
---
# <a name="devices-direct3d-11-graphics"></a>Dispositivi (grafica Direct3D 11)

Un dispositivo Direct3D alloca ed Elimina definitivamente gli oggetti, esegue il rendering delle primitive e comunica con un driver di grafica e l'hardware. In Direct3D 11 un dispositivo viene separato in un oggetto dispositivo per la creazione di risorse e un oggetto del contesto di dispositivo che esegue il rendering. Questa sezione descrive gli oggetti del dispositivo e del contesto del dispositivo Direct3D 11.

Gli oggetti creati da un dispositivo non possono essere usati direttamente con altri dispositivi. Usare una risorsa condivisa per condividere i dati tra più dispositivi, con il vincolo che un oggetto condiviso può essere usato solo dal dispositivo che lo ha creato.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                                                         | Descrizione                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introduzione a un dispositivo in Direct3D 11](overviews-direct3d-11-devices-intro.md)<br/>                                                                 | Il modello a oggetti Direct3D 11 separa la creazione e la funzionalità di rendering delle risorse in un dispositivo e uno o più contesti; Questa separazione è progettata per semplificare il multithreading.<br/>                                                  |
| [Livelli software](overviews-direct3d-11-devices-layers.md)<br/>                                                                                        | Il runtime di Direct3D 11 viene costruito con i livelli, a partire dalle funzionalità di base e la creazione di funzionalità facoltative e di supporto per gli sviluppatori nei livelli esterni. In questa sezione vengono descritte le funzionalità di ogni livello.<br/> |
| [Limitazioni della creazione di dispositivi WARP e Reference](overviews-direct3d-11-devices-limitations.md)<br/>                                                   | Esistono alcune limitazioni per la creazione di dispositivi WARP e Reference in Direct3D 10,1 e Direct3D 11,0. In questo argomento vengono illustrate tali limitazioni.<br/>                                                                                              |
| [Direct3D 11 su hardware di livello inferiore](overviews-direct3d-11-devices-downlevel.md)<br/>                                                                   | Questa sezione illustra il modo in cui Direct3D 11 è progettato per supportare hardware nuovi ed esistenti, da DirectX 9 a DirectX 11.<br/>                                                                                                             |
| [Utilizzo dei dati della funzionalità Direct3D 11 per integrare i livelli di funzionalità Direct3D](using-direct3d-optional-features-to-supplement-direct3d-feature-levels.md)<br/> | Informazioni su come controllare il supporto dei dispositivi per le funzionalità facoltative, incluse le funzionalità aggiunte nelle versioni recenti di Windows.<br/>                                                                                                           |



 

## <a name="how-to-topics-about-devices"></a>Procedure per i dispositivi



| Argomento                                                                                                                                                                                                                                                                                                    | Descrizione                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="How_To__Create_a_Reference_Device"></span><span id="how_to__create_a_reference_device"></span><span id="HOW_TO__CREATE_A_REFERENCE_DEVICE"></span>[Procedura: creare un dispositivo di riferimento](overviews-direct3d-11-devices-create-ref.md)<br/>                                                 | Viene descritto come creare un dispositivo di riferimento.<br/>                            |
| <span id="How_To__Create_a_WARP_Device"></span><span id="how_to__create_a_warp_device"></span><span id="HOW_TO__CREATE_A_WARP_DEVICE"></span>[Procedura: creare un dispositivo WARP](overviews-direct3d-11-devices-create-warp.md)<br/>                                                                    | Viene descritto come creare un dispositivo WARP.<br/>                                 |
| <span id="How_To__Create_a_Swap_Chain"></span><span id="how_to__create_a_swap_chain"></span><span id="HOW_TO__CREATE_A_SWAP_CHAIN"></span>[Procedura: creare una catena di scambio](overviews-direct3d-11-devices-create-swap-chain.md)<br/>                                                                  | Viene descritto come creare una catena di scambio.<br/>                                  |
| <span id="How_To__Enumerate_Adapters"></span><span id="how_to__enumerate_adapters"></span><span id="HOW_TO__ENUMERATE_ADAPTERS"></span>[Procedura: enumerare gli adapter](overviews-direct3d-11-devices-enum.md)<br/>                                                                                   | Viene descritto come enumerare le schede di visualizzazione fisiche.<br/>              |
| <span id="How_To__Get_Adapter_Display_Modes"></span><span id="how_to__get_adapter_display_modes"></span><span id="HOW_TO__GET_ADAPTER_DISPLAY_MODES"></span>[Procedura: ottenere le modalità di visualizzazione dell'adapter](overviews-direct3d-11-devices-get-adapter-info.md)<br/>                                           | Viene descritto come ottenere le funzionalità di visualizzazione supportate di un adapter.<br/> |
| <span id="How_To__Create_a_Device_and_Immediate_Context"></span><span id="how_to__create_a_device_and_immediate_context"></span><span id="HOW_TO__CREATE_A_DEVICE_AND_IMMEDIATE_CONTEXT"></span>[Procedura: creare un dispositivo e un contesto immediato](overviews-direct3d-11-devices-initialize.md)<br/> | Viene descritto come inizializzare un dispositivo.<br/>                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione per Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

 





