---
description: Le schede Multihead sono quelle con un acceleratore e un acceleratore di frame, indipendenti da Digital a analogico (DAC), e monitorano gli output.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multihead (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4617666ca623795d33bf1dafcaafeabe73323253
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481300"
---
# <a name="multihead-direct3d-9"></a>Multihead (Direct3D 9)

Le schede Multihead sono quelle con un acceleratore e un acceleratore di frame, indipendenti da Digital a analogico (DAC), e monitorano gli output. Tali dispositivi possono offrire un supporto più usabile per più monitor rispetto a un numero simile di schede di visualizzazione eterogenee.

Le schede Multihead sono esposte nell'API come un singolo dispositivo a livello di API che può guidare diverse catene di scambio a schermo intero. Di conseguenza, tutte le risorse vengono condivise con tutte le intestazioni e ogni Head ha esattamente le stesse funzionalità. Ogni intestazione può essere impostata su modalità di visualizzazione indipendente. È possibile usare chiamate separate a [**IDirect3DSwapChain9::P inviato nuovamente**](/windows/desktop/api) per aggiornare ogni Head. È anche possibile usare una sola chiamata a [**IDirect3DDevice9::P inviato nuovamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) per aggiornare ogni Head in modo sequenziale.

> [!Note]  
> L'aggiornamento di ogni Head non si verifica contemporaneamente con una singola chiamata a [**IDirect3DDevice9::P inviato nuovamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Le statistiche presenti in Direct3D 9Ex possono utilizzare la struttura [**D3DPRESENTSTATS**](d3dpresentstats.md) per limitare gli aggiornamenti a ogni capo vicino per limitare gli effetti di strappo tra più intestazioni degli adapter. Per informazioni sulla sincronizzazione dei frame delle applicazioni Direct3D 9Ex flip model, vedere la pagina relativa ai [miglioramenti di Direct3D 9Ex](../direct3darticles/direct3d-9ex-improvements.md).

 

Ogni catena di scambio per un dispositivo Multihead deve essere a schermo intero. Quando un dispositivo è entrato in modalità multihead, deve rimanere a schermo intero. La transizione alla modalità finestra richiede l'eliminazione del dispositivo (ad eccezione della normale operazione ALT + TAB-to-minimizza).

Il metodo precedente per suddividere la memoria video tra le teste e considerare ogni capo come un acceleratore completamente indipendente sarà comunque uno scenario di utilizzo comune. Questa proposta non sostituisce questo meccanismo, a meno che l'applicazione non sia stata codificata in modo specifico per funzionare in modalità Multihead Direct3D 9.

Ai driver viene assegnata una conoscenza adeguata per passare tra le due modalità operative.

Una testa verrà chiamata intestazione master e tutte le altre teste sulla stessa scheda verranno denominate intestazioni subordinate. Se in un sistema è presente più di un adattatore multihead, il database master e i relativi subordinati di un adattatore Multihead vengono chiamati gruppi. I gruppi sono identificati dall'ordinale dell'adapter della testa master.

La struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) è stata aggiornata per esporre i nuovi tappi hardware seguenti.


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   NumberOfAdaptersInGroup è 1 per gli adapter convenzionali e maggiore di 1 per l'adattatore Master di una scheda Multihead. Il valore sarà 0 per un adapter subordinato di una scheda Multihead. Ogni scheda può avere al massimo un master, ma potrebbe avere molti subordinati.
-   MasterAdapterOrdinal indica quale dispositivo è il master per questo subordinato.
-   AdapterOrdinalInGroup indica l'ordine in cui le intestazioni fanno riferimento all'API. L'adapter Master ha sempre AdapterOrdinalInGroup 0. Questi valori non corrispondono ai numeri ordinali degli adapter passati ai metodi IDirect3D9, ma si applicano solo alle intestazioni all'interno di un gruppo.

Questa definizione consente alle schede Multihead di continuare a presentare più schede come se fossero schede indipendenti, proprio come in DirectX 8.

Per creare un dispositivo multihead, specificare il flag di comportamento D3DCREATE \_ ADAPTERGROUP \_ Device in [**IDirect3D9:: CreateDevice**](/windows/desktop/api). I parametri di presentazione, ovvero una matrice di [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md), devono contenere elementi NumberOfAdaptersInGroup. Il runtime assegnerà ogni elemento a ogni Head in ordine numerico AdapterOrdinalInGroup. Quando \_ \_ viene impostato il dispositivo D3DCREATE ADAPTERGROUP, ogni parametro Presentation deve avere:

-   Il membro a finestra è impostato su **false** (in altre parole, deve essere a schermo intero).
-   Lo stesso valore per il membro EnableAutoDepthStencil dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md).

Inoltre, se EnableAutoDepthStencil è **true**, ognuno dei campi seguenti deve avere lo stesso valore per ogni [**\_ parametro D3DPRESENT**](d3dpresent-parameters.md):

-   AutoDepthStencilFormat
-   BackBufferWidth
-   BackBufferHeight
-   BackBufferFormat

Se è impostata l'applicazione livello dati, le chiamate aggiuntive a [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) non sono valide.

Se il dispositivo è stato creato con l'applicazione livello dati, [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) prevede una matrice di [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md).

Ogni struttura di [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) passata a [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) deve essere a schermo intero. Per tornare alla modalità finestra, l'applicazione deve eliminare definitivamente il dispositivo e ricreare un dispositivo non multiparte in modalità finestra.

Di seguito è riportato uno scenario di utilizzo di base:


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



Per ulteriori informazioni, vedere [**IDirect3D9:: CreateDevice**](/windows/desktop/api) e [**IDirect3DDevice9:: GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 
