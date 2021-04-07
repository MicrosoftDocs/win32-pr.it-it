---
description: In un'applicazione Direct3D viene in genere visualizzata una sequenza animata generando i frame dell'animazione nei buffer indietro e mostrandoli in sequenza.
ms.assetid: 4ca9a845-f433-4d4a-939e-4b9ab2983927
title: Capovolgimento di superfici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dafd263de0f907b33ff6f20ffcbb2cce69943da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746866"
---
# <a name="flipping-surfaces-direct3d-9"></a>Capovolgimento di superfici (Direct3D 9)

In un'applicazione Direct3D viene in genere visualizzata una sequenza animata generando i frame dell'animazione nei buffer indietro e mostrandoli in sequenza. I buffer indietro sono organizzati in catene di scambio. Una catena di scambio è una serie di buffer che "Capovolgere" sullo schermo uno dopo l'altro. Questa operazione può essere utilizzata per eseguire il rendering di una scena in memoria e quindi capovolgerla sullo schermo quando il rendering viene completato. In questo modo si evita il fenomeno noto come strappo e si consente un'animazione più uniforme.

Ogni dispositivo creato in Direct3D ha almeno una catena di scambio. Quando si inizializza il primo dispositivo Direct3D, si imposta il membro BackBufferCount di [**D3DPRESENT \_ parametri**](d3dpresent-parameters.md), che indica a Direct3D il numero di buffer back che saranno presenti nella catena di scambio. La chiamata a [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crea quindi il dispositivo Direct3D e la catena di scambio corrispondente.

Quando si usa [**IDirect3DDevice9::P inviato nuovamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) per richiedere un'operazione di apertura della superficie, i puntatori alla memoria di superficie per il buffer anteriore e i buffer indietro vengono scambiati. Il capovolgimento viene eseguito cambiando i puntatori usati dal dispositivo di visualizzazione per fare riferimento alla memoria, non copiando la memoria della superficie. Quando una catena di capovolgimento contiene un buffer anteriore e più di un buffer nascosto, i puntatori vengono scambiati in un modello circolare, come illustrato nel diagramma seguente.

![diagramma di una catena di capovolgimento con un buffer anteriore e due buffer indietro](images/trplflip.png)

È possibile creare catene di scambio aggiuntive per un dispositivo chiamando [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/desktop/api). Un'applicazione può creare una catena di scambio per ogni visualizzazione e associare ogni catena di scambio a una particolare finestra. L'applicazione esegue il rendering delle immagini nei buffer indietro di ogni catena di scambio e quindi le presenta singolarmente. I due parametri accettati da **IDirect3DDevice9:: CreateAdditionalSwapChain** sono un puntatore a una struttura di [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) e l'indirizzo di un puntatore a un'interfaccia [**IDirect3DSwapChain9**](/windows/desktop/api) . È quindi possibile usare [**IDirect3DSwapChain9::P inviato nuovamente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) per visualizzare il contenuto del buffer nascosto successivo nel buffer anteriore. Si noti che un dispositivo può avere una sola catena di scambio a schermo intero.

È possibile ottenere l'accesso a un buffer nascosto specifico chiamando i metodi [**IDirect3DDevice9:: GetBackBuffer**](/windows/desktop/api) o [**IDirect3DSwapChain9:: GetBackBuffer**](/windows/desktop/api) , che restituiscono un puntatore a un'interfaccia [**IDirect3DSurface9**](/windows/desktop/api) che rappresenta la superficie del buffer indietro restituita. Si noti che la chiamata a questo metodo aumenta il conteggio dei riferimenti interni nell'interfaccia [**IDirect3DDevice9**](/windows/desktop/api) , quindi assicurarsi di chiamare [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) al termine dell'operazione oppure si disporrà di una perdita di memoria.

Tenere presente che Direct3D capovolge le superfici scambiando i puntatori della memoria di superficie all'interno della catena di scambio, non scambiando le superfici stesse. Ciò significa che verrà sempre eseguito il rendering nel buffer nascosto che verrà visualizzato successivamente.

È importante notare la distinzione tra una "operazione di capovolgimento", come eseguita da un driver della scheda video e un'operazione "presente" applicata a una catena di scambio creata con D3DSWAPEFFECT \_ flip.

Il termine "Capovolgi" indica convenzionalmente un'operazione che modifica l'intervallo di indirizzi di memoria video utilizzati da un adattatore di visualizzazione per generare il segnale di output, causando in tal modo la visualizzazione del contenuto di un buffer nascosto precedentemente nascosto. In Direct3D 9 il termine viene spesso usato più in generale per descrivere la presentazione di un buffer nascosto in qualsiasi catena di scambio creata con l' \_ effetto di D3DSWAPEFFECT Flip swap.

Sebbene le operazioni "presenti" siano quasi invariabilmente implementate dalle operazioni di capovolgimento quando la catena di scambio è a schermo intero, vengono necessariamente implementate dalle operazioni di copia quando la catena di scambio è a finestra. Inoltre, è possibile che un driver della scheda di visualizzazione usi il capovolgimento per implementare le operazioni presenti sulle catene di scambio a schermo intero in base alla copia D3DSWAPEFFECT di \_ scarto e D3DSWAPEFFECT \_ .

La discussione precedente si applica al caso di uso comune di una catena di scambio a schermo intero creata con D3DSWAPEFFECT \_ flip.

Per una descrizione più generale dei diversi effetti di swapping per le catene di scambio a schermo intero e a schermo intero, vedere [**D3DSWAPEFFECT**](./d3dswapeffect.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
