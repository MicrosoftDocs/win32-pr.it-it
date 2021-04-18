---
description: L'applicazione Direct3D può assegnare coordinate di trama a qualsiasi vertice di qualsiasi primitiva.
ms.assetid: 2e23bcb3-9eba-49d9-93ce-0a4fbb15f746
title: Modalità di indirizzamento delle trame (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ebad5fdb141c41c43c651a2188640d7a6b764e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304373"
---
# <a name="texture-addressing-modes-direct3d-9"></a>Modalità di indirizzamento delle trame (Direct3D 9)

L'applicazione Direct3D può assegnare coordinate di trama a qualsiasi vertice di qualsiasi primitiva. Per informazioni dettagliate, vedere [coordinate di trama (Direct3D 9)](texture-coordinates.md). In genere, le coordinate di trama u-e v assegnate a un vertice sono comprese nell'intervallo tra 0,0 e 1,0 inclusi. Tuttavia, se si assegnano coordinate di trama esterne a tale intervallo, è possibile creare alcuni effetti speciali di texturing.

È possibile controllare le operazioni di Direct3D con le coordinate di trama che non rientrano nell' \[ intervallo 0,0, 1,0 impostando \] la modalità di indirizzamento della trama. Ad esempio, è possibile impostare l'applicazione sulla modalità di indirizzamento della trama in modo che una trama venga affiancata in una primitiva.

Direct3D consente alle applicazioni di eseguire il wrapping della trama. È importante notare che l'impostazione della modalità di indirizzamento della trama su D3DTADDRESS \_ Wrap non corrisponde all'esecuzione del wrapping della trama. L'impostazione della modalità di indirizzamento della trama su D3DTADDRESS \_ Wrap comporta l'applicazione di più copie della trama di origine alla primitiva corrente e l'abilitazione del wrapping della trama per modificare il modo in cui il sistema Rasterizza i poligoni con trama. Per informazioni dettagliate, vedere [wrapping della trama (Direct3D 9)](texture-wrapping.md).

L'abilitazione del wrapping della trama rende efficaci le coordinate di trama al di fuori dell' \[ intervallo 0,0, 1,0 \] e il comportamento per la rasterizzazione di tali coordinate di trama delinquente non è definito in questo caso. Quando il wrapping della trama è abilitato, le modalità di indirizzamento delle trame non vengono usate. Assicurarsi che l'applicazione non specifichi coordinate di trama inferiori a 0,0 o superiori a 1,0 quando il wrapping della trama è abilitato.

## <a name="setting-the-addressing-mode"></a>Impostazione della modalità di indirizzamento

È possibile impostare le modalità di indirizzamento delle trame per singole fasi di trama chiamando il metodo [**IDirect3DDevice9:: SetSamplerState**](/windows/desktop/api) . Specificare l'identificatore della fase di trama desiderato nel parametro *Sampler* . Impostare il parametro di *tipo* sui \_ valori D3DSAMP, D3DSAMP \_ ADDRESSV o D3DSAMP \_ ADDRESSW per aggiornare singolarmente le modalità di indirizzamento u-, v-o w. Il parametro *value* determina la modalità da impostare. Può trattarsi di qualsiasi membro del tipo enumerato [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) . Per recuperare la modalità di indirizzamento della trama corrente per una fase di trama, chiamare [**IDirect3DDevice9:: GetSamplerState**](/windows/desktop/api), usando i \_ membri D3DSAMP Address, D3DSAMP \_ ADDRESSV o D3DSAMP \_ ADDRESSW dell'enumerazione [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) per identificare la modalità di indirizzo su cui si desidera ottenere informazioni.

## <a name="device-limitations"></a>Limitazioni del dispositivo

Sebbene il sistema consenta in genere le coordinate di trama non comprese nell'intervallo tra 0,0 e 1,0, incluse le limitazioni hardware spesso influiscono sulla distanza delle coordinate di trama degli intervalli. Un dispositivo di rendering comunica questo limite nel membro **MaxTextureRepeat** della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) quando si recuperano le funzionalità del dispositivo. Il valore in questo membro descrive l'intervallo completo di coordinate di trama consentite dal dispositivo. Ad esempio, se questo valore è 128, le coordinate di trama di input devono essere mantenute nell'intervallo compreso tra-128,0 e + 128,0. Il passaggio di vertici con coordinate di trama esterne a questo intervallo non è valido. La stessa restrizione si applica alle coordinate di trama generate come risultato della generazione automatica delle coordinate di trama e delle trasformazioni di coordinate di trama.

L'interpretazione di **MaxTextureRepeat** è influenzata anche dal \_ bit della funzionalità TEXREPEATNOTSCALEDBYSIZE D3DPTEXTURECAPS. Quando questo bit è impostato, il valore nel membro **MaxTextureRepeat** viene utilizzato esattamente come descritto. Tuttavia, quando D3DPTEXTURECAPS \_ TEXREPEATNOTSCALEDBYSIZE non è impostato, le limitazioni di trama ripetute dipendono dalle dimensioni della trama indicizzate dalle coordinate di trama. In questo caso, **MaxTextureRepeat** deve essere ridimensionato in base alle dimensioni di trama correnti al livello di dettaglio più grande per calcolare l'intervallo di coordinate di trama valido. Ad esempio, data una dimensione di trama di 32 e **MaxTextureRepeat** di 512, l'intervallo di coordinate di trama valido effettivo è 512/32 = 16, quindi le coordinate di trama per questo dispositivo devono essere comprese nell'intervallo da-16,0 a + 16,0.

Altre informazioni sulle modalità di indirizzamento delle trame sono contenute negli argomenti seguenti.

-   [Modalità di indirizzamento della trama a capo (Direct3D 9)](wrap-texture-address-mode.md)
-   [Modalità address texture mirror (Direct3D 9)](mirror-texture-address-mode.md)
-   [Modalità di indirizzamento della trama del morsetto (Direct3D 9)](clamp-texture-address-mode.md)
-   [Modalità di indirizzo della trama colore del bordo (Direct3D 9)](border-color-texture-address-mode.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla texturing](basic-texturing-concepts.md)
</dt> </dl>

 

 
