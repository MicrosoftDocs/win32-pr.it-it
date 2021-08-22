---
description: Le schede a più teste sono quelle che hanno un buffer di frame e un acceleratore comuni, convertitori indipendenti da digitale ad analogico (DAC) e output di monitoraggio.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multihead (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a74f51cea282618c9471eb9a63eedf8eef73c38b4d961209064261a93c4d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563517"
---
# <a name="multihead-direct3d-9"></a>Multihead (Direct3D 9)

Le schede a più teste sono quelle che hanno un buffer di frame e un acceleratore comuni, convertitori indipendenti da digitale ad analogico (DAC) e output di monitoraggio. Tali dispositivi possono offrire un supporto di monitor multipli molto più utilizzabile rispetto a un numero simile di schede video eterogenee.

Le schede a più teste vengono esposte nell'API come un singolo dispositivo a livello di API che può guidare diverse catene di scambio a schermo intero. Di conseguenza, tutte le risorse vengono condivise con tutte le teste e ogni testa ha esattamente le stesse funzionalità. Ogni testina può essere impostata su modalità di visualizzazione indipendenti. È possibile usare chiamate separate a [**IDirect3DSwapChain9::P resent**](/windows/desktop/api) per aggiornare ogni head. È anche possibile usare una chiamata a [**IDirect3DDevice9::P per**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) aggiornare ogni head in sequenza.

> [!Note]  
> L'aggiornamento di ogni head non viene eseguito contemporaneamente con una singola chiamata a [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Le statistiche presenti in Direct3D 9Ex possono usare la struttura [**D3DPRESENTSTATS**](d3dpresentstats.md) per mantenere gli aggiornamenti a ogni testina vicini l'uno all'altro per limitare gli effetti di tearing tra più testine di adattatori. Per informazioni sulla sincronizzazione dei fotogrammi delle applicazioni direct3D 9Ex flip model, vedere Miglioramenti di [Direct3D 9Ex.](../direct3darticles/direct3d-9ex-improvements.md)

 

Ogni catena di scambio per un dispositivo a più teste deve essere a schermo intero. Quando un dispositivo è in modalità a più teste, deve rimanere a schermo intero. La transizione alla modalità finestra richiede l'eliminazione del dispositivo (ad eccezione della normale operazione ALT+TAB per ridurre a icona).

Il vecchio metodo di divisione della memoria video tra le testine e il trattamento di ogni testina come acceleratore completamente indipendente sarà comunque uno scenario di utilizzo comune. Questa proposta non sostituisce tale meccanismo a meno che l'applicazione non sia stata specificatamente codificata per funzionare in modalità a più teste Direct3D 9.

Ai driver viene data una conoscenza adeguata per passare da una modalità di funzionamento all'altra.

Una testa sarà denominata testa master e tutte le altre teste nella stessa scheda saranno chiamate teste subordinate. Se in un sistema sono presenti più schede a più teste, il master e i relativi subordinati di un adattatore multihead vengono chiamati gruppo. I gruppi sono denotata dal numero ordinale dell'adapter della testa master.

La [**struttura D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) è stata aggiornata per esporre i nuovi limiti hardware seguenti.


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   NumberOfAdaptersInGroup è 1 per gli adapter convenzionali e maggiore di 1 per l'adattatore master di una scheda a più teste. Il valore sarà 0 per un adattatore subordinato di una scheda a più teste. Ogni scheda può avere al massimo un master, ma può avere molti subordinati.
-   MasterAdapterOrdinal indica quale dispositivo è il master per questo oggetto subordinato.
-   AdapterOrdinalInGroup indica l'ordine in cui l'API fa riferimento alle testine. L'adapter master ha sempre AdapterOrdinalInGroup 0. Questi valori non corrispondono agli ordinali dell'adapter passati ai metodi IDirect3D9, ma si applicano solo alle testine all'interno di un gruppo.

Questa definizione consente alle schede multihead di continuare a presentare più schede come se fossero schede indipendenti, proprio come in DirectX 8.

Per creare un dispositivo multihead, specificare il flag di comportamento D3DCREATE \_ ADAPTERGROUP \_ DEVICE in [**IDirect3D9::CreateDevice**](/windows/desktop/api). I parametri di presentazione (una matrice [**di parametri D3DPRESENT \_**](d3dpresent-parameters.md)) devono contenere elementi NumberOfAdaptersInGroup. Il runtime assegna ogni elemento a ogni head nell'ordine numerico AdapterOrdinalInGroup. Quando È impostato D3DCREATE \_ ADAPTERGROUP \_ DEVICE, ogni parametro di presentazione deve avere:

-   Il membro Windowed impostato su **FALSE** (in altre parole, a schermo intero).
-   Stesso valore per il membro EnableAutoDepthStencil di [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md).

Inoltre, se EnableAutoDepthStencil è **TRUE,** ognuno dei campi seguenti deve avere lo stesso valore per ogni [**parametro D3DPRESENT \_**](d3dpresent-parameters.md):

-   AutoDepthStencilFormat
-   BackBufferWidth
-   BackBufferHeight
-   BackBufferFormat

Se l'applicazione livello dati è impostata, le chiamate aggiuntive a [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) non sono validi.

Se il dispositivo è stato creato con l'applicazione livello dati, [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) prevede una matrice [**di PARAMETRI D3DPRESENT \_**](d3dpresent-parameters.md).

Ogni [**struttura D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md) passata a [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) deve essere a schermo intero. Per tornare alla modalità finestra, l'applicazione deve eliminare il dispositivo e creare di nuovo un dispositivo non multihead in modalità a finestre.

Ecco uno scenario di utilizzo di base:


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



Per altre informazioni, vedere [**IDirect3D9::CreateDevice**](/windows/desktop/api) e [**IDirect3DDevice9::GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmazione Suggerimenti](programming-tips.md)
</dt> </dl>

 

 
