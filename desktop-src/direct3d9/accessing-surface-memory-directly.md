---
description: 'È possibile accedere direttamente alla memoria della superficie usando il metodo IDirect3DSurface9:: LockRect.'
ms.assetid: ad669c22-6163-4fbb-bad0-160ced5bc558
title: Accesso diretto alla memoria di Surface (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ed9a65265671e6509172eccd9a1b66ea91507f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342221"
---
# <a name="accessing-surface-memory-directly-direct3d-9"></a>Accesso diretto alla memoria di Surface (Direct3D 9)

È possibile accedere direttamente alla memoria della superficie usando il metodo [**IDirect3DSurface9:: LockRect**](/windows/desktop/api) . Quando si chiama questo metodo, il parametro pRect è un puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che descrive il rettangolo sulla superficie a cui accedere direttamente. Per richiedere che l'intera superficie venga bloccata, impostare pRect su **null**. Inoltre, è possibile specificare un oggetto **Rect** che copre solo una parte della superficie. A condizione che non si sovrappongano due rettangoli, due thread o processi possono bloccare simultaneamente più rettangoli in una superficie. Si noti che non è possibile bloccare un buffer nascosto multicampione.

Il metodo [**IDirect3DSurface9:: LockRect**](/windows/desktop/api) inserisce una struttura [**D3DLOCKED \_ Rect**](d3dlocked-rect.md) con tutte le informazioni per accedere correttamente alla memoria della superficie. La struttura include informazioni sul passo e un puntatore ai bit bloccati. Al termine dell'accesso alla memoria della superficie, chiamare il metodo [**IDirect3DSurface9:: UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) per sbloccarlo.

Quando si dispone di una superficie bloccata, è possibile modificare direttamente il contenuto. Nell'elenco seguente vengono descritti alcuni suggerimenti per evitare problemi comuni con il rendering diretto della memoria della superficie.

-   Non presupporre mai un passo di visualizzazione costante. Esaminare sempre le informazioni sul pitch restituite dal metodo [**IDirect3DSurface9:: LockRect**](/windows/desktop/api) . Questo pitch può variare per diversi motivi, tra cui la posizione della memoria della superficie, il tipo di scheda di visualizzazione o anche la versione del driver Direct3D. Per altre informazioni, vedere [Width vs. Pitch (Direct3D 9)](width-vs--pitch.md).
-   Assicurarsi di copiare in superfici sbloccate. I metodi di copia Direct3D avranno esito negativo se vengono chiamati su una superficie bloccata.
-   Limitare l'attività dell'applicazione mentre è bloccata una superficie.
-   Copiare sempre i dati allineati per visualizzare la memoria. Windows 98 utilizza un gestore di errori di pagina, Vflatd. 386, per implementare un buffer di fotogrammi virtuali per le schede di visualizzazione con memoria a commutazione di banca. Il gestore consente a questi dispositivi di visualizzare di presentare un buffer di frame lineare a Direct3D. La copia dei dati non allineati alla memoria di visualizzazione può causare la sospensione delle operazioni da parte del sistema se la copia si estende in banchi di memoria.
-   Una superficie potrebbe non essere bloccata se appartiene a una risorsa assegnata al pool di memoria predefinito D3DPOOL, a meno che non si tratti di una \_ trama dinamica o di una superficie creata con [**IDirect3DDevice9:: CreateOffscreenPlainSurface**](/windows/desktop/api). Le superfici del buffer nascosto, a cui è possibile accedere tramite i metodi [**IDirect3DDevice9:: GetBackBuffer**](/windows/desktop/api) e [**IDirect3DSwapChain9:: GetBackBuffer**](/windows/desktop/api) , possono essere bloccate solo se la catena di scambio è stata creata con il membro Flags dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) per includere il \_ backBuffer bloccabile D3DPRESENTFLAG \_ .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Superfici Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
