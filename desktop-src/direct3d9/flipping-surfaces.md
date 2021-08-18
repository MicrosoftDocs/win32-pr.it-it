---
description: Un'applicazione Direct3D visualizza in genere una sequenza animata generando i fotogrammi dell'animazione nei buffer nascosto e presentandoli in sequenza.
ms.assetid: 4ca9a845-f433-4d4a-939e-4b9ab2983927
title: Capovolgimento delle superfici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c14aa7df63c3956d4974282033b44a7129853940d475b23115f9bca344ca4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988037"
---
# <a name="flipping-surfaces-direct3d-9"></a>Capovolgimento delle superfici (Direct3D 9)

Un'applicazione Direct3D visualizza in genere una sequenza animata generando i fotogrammi dell'animazione nei buffer nascosto e presentandoli in sequenza. I buffer back sono organizzati in catene di scambio. Una catena di scambio è una serie di buffer che vengono "capovolti" sullo schermo uno dopo l'altro. Può essere usato per eseguire il rendering di una scena in memoria e quindi per capovolgere la scena sullo schermo al termine del rendering. In questo modo si evita il fenomeno noto come la rimozione e si consente un'animazione più uniforme.

Ogni dispositivo creato in Direct3D ha almeno una catena di scambio. Quando si inizializza il primo dispositivo Direct3D, si imposta il membro BackBufferCount di [**D3DPRESENT \_ PARAMETERS,**](d3dpresent-parameters.md)che indica a Direct3D il numero di buffer nascosto che saranno presenti nella catena di scambio. La chiamata a [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crea quindi il dispositivo Direct3D e la catena di scambio corrispondente.

Quando si usa [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) per richiedere un'operazione di capovolgimento della superficie, i puntatori alla memoria surface per il front buffer e i buffer back vengono scambiati. Il capovolgimento viene eseguito scambiando i puntatori utilizzati dal dispositivo di visualizzazione per fare riferimento alla memoria, non copiando la memoria della superficie. Quando una catena di capovolgimento contiene un buffer anteriore e più buffer nascosto, i puntatori vengono commutati in un modello circolare, come illustrato nel diagramma seguente.

![diagramma di una catena di capovolgimento con un buffer anteriore e due buffer back](images/trplflip.png)

È possibile creare catene di scambio di addizione per un dispositivo chiamando [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/desktop/api). Un'applicazione può creare una catena di scambio per ogni visualizzazione e associare ogni catena di scambio a una determinata finestra. L'applicazione esegue il rendering delle immagini nei buffer back di ogni catena di scambio e quindi le presenta singolarmente. I due parametri accettati **da IDirect3DDevice9::CreateAdditionalSwapChain** sono un puntatore a una struttura [**PARAMETERS D3DPRESENT \_**](d3dpresent-parameters.md) e l'indirizzo di un puntatore a un'interfaccia [**IDirect3DSwapChain9.**](/windows/desktop/api) È quindi possibile usare [**IDirect3DSwapChain9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) per visualizzare il contenuto del buffer nascosto successivo nel front buffer. Si noti che un dispositivo può avere una sola catena di scambio a schermo intero.

È possibile accedere a un buffer nascosto specifico chiamando i metodi [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) o [**IDirect3DSwapChain9::GetBackBuffer,**](/windows/desktop/api) che restituiscono un puntatore a un'interfaccia [**IDirect3DSurface9**](/windows/desktop/api) che rappresenta la superficie del buffer nascosto restituita. Si noti che la chiamata a questo metodo aumenta il conteggio dei riferimenti interni [**nell'interfaccia IDirect3DDevice9,**](/windows/desktop/api) quindi assicurarsi di chiamare [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) al termine dell'uso di questa superficie o si verifica una perdita di memoria.

Tenere presente che Direct3D capovolge le superfici scambiando i puntatori di memoria della superficie all'interno della catena di scambio, non scambiando le superfici stesse. Ciò significa che verrà sempre eseguito il rendering nel buffer nascosto che verrà visualizzato successivamente.

È importante notare la distinzione tra un'operazione di capovolgimento, eseguita da un driver della scheda video, e un'operazione "Present" applicata a una catena di scambio creata con D3DSWAPEFFECT \_ FLIP.

Il termine "capovolgimento" indica convenzionalmente un'operazione che modifica l'intervallo di indirizzi di memoria video che una scheda video usa per generare il segnale di output, causando così la visualizzazione del contenuto di un buffer nascosto in precedenza. In Direct3D 9 il termine viene spesso usato più in generale per descrivere la presentazione di un buffer nascosto in qualsiasi catena di scambio creata con l'effetto flip FLIP D3DSWAPEFFECT. \_

Anche se queste operazioni "Presenti" vengono implementate quasi invariabilmente dalle operazioni di capovolgimento quando la catena di scambio è a schermo intero, vengono necessariamente implementate dalle operazioni di copia quando la catena di scambio è in finestra. Inoltre, un driver di scheda video può usare il capovolgimento per implementare le operazioni Present su catene di scambio a schermo intero basate su D3DSWAPEFFECT DISCARD e \_ D3DSWAPEFFECT \_ COPY.

La discussione precedente si applica al caso comunemente usato di una catena di scambio a schermo intero creata con D3DSWAPEFFECT \_ FLIP.

Per una descrizione più generale dei diversi effetti di scambio sia per le catene di scambio finestra che per le catene di scambio a schermo intero, vedere [**D3DSWAPEFFECT.**](./d3dswapeffect.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
