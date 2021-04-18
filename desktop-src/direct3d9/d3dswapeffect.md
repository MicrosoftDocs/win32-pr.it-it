---
description: Definisce gli effetti di swapping.
ms.assetid: 522a5f71-3ad9-4cfc-a899-e25b9b721b1b
title: Enumerazione D3DSWAPEFFECT (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSWAPEFFECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41327dc66f676c6f498ad0cefb23202bedc13112
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322453"
---
# <a name="d3dswapeffect-enumeration"></a>Enumerazione D3DSWAPEFFECT

Definisce gli effetti di swapping.

## <a name="syntax"></a>Sintassi

```cpp
typedef enum D3DSWAPEFFECT { 
  D3DSWAPEFFECT_DISCARD      = 1,
  D3DSWAPEFFECT_FLIP         = 2,
  D3DSWAPEFFECT_COPY         = 3,
  D3DSWAPEFFECT_OVERLAY      = 4,
  D3DSWAPEFFECT_FLIPEX       = 5,
  D3DSWAPEFFECT_FORCE_DWORD  = 0xFFFFFFFF
} D3DSWAPEFFECT, *LPD3DSWAPEFFECT;
```

## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**Eliminazione di D3DSWAPEFFECT \_**
</dt> <dd>

Quando viene creata una catena di scambio con un effetto di scambio di D3DSWAPEFFECT \_ Flip o D3DSWAPEFFECT \_ Copy, il runtime garantisce che un'operazione di [**IDirect3DDevice9::P**](/windows/desktop/api) reinviata non influirà sul contenuto di uno dei buffer back. Sfortunatamente, la riunione di questa garanzia può comportare un sovraccarico significativo della memoria video o dell'elaborazione, soprattutto quando si implementa la semantica di capovolgimento per una catena di scambio a finestra o una semantica di copia per una catena di scambio a schermo intero. Un'applicazione può usare l' \_ effetto di scarto D3DSWAPEFFECT per evitare questi sovraccarichi e consentire al driver di visualizzazione di selezionare la tecnica di presentazione più efficiente per la catena di scambio. Questo è anche l'unico effetto di swapping che può essere usato quando si specifica un valore diverso da D3DMULTISAMPLE \_ None per il membro MultiSampleType dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md).

Analogamente a una catena di scambio che usa D3DSWAPEFFECT \_ Flip, una catena di scambio che usa D3DSWAPEFFECT \_ scarto potrebbe includere più di un buffer nascosto, a cui è possibile accedere con [**IDirect3DDevice9:: GetBackBuffer**](/windows/desktop/api) o [**IDirect3DSwapChain9:: GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer). La catena di scambio è preferibile come una coda in cui 0 indicizza sempre il buffer nascosto che verrà visualizzato dalla successiva operazione presente e da cui i buffer vengono eliminati quando vengono visualizzati.

Un'applicazione che usa questo effetto di scambio non può fare supposizioni sul contenuto di un buffer nascosto rimosso e pertanto deve aggiornare un intero buffer nascosto prima di richiamare un'operazione presente che la visualizzerà. Sebbene non venga applicato, la versione di debug del runtime sovrascriverà il contenuto dei buffer indietro rimossi con dati casuali per consentire agli sviluppatori di verificare che le applicazioni stiano aggiornando correttamente l'intero buffer nascosto.

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT \_ Flip**
</dt> <dd>

La catena di scambio potrebbe includere più buffer back ed è preferibile come una coda circolare che include il buffer anteriore. All'interno di questa coda, i buffer indietro sono sempre numerati in sequenza da 0 a (n-1), dove n è il numero di buffer indietro, in modo che 0 indica il buffer presentato meno di recente. Quando present viene richiamato, la coda viene "ruotata" in modo che il buffer anteriore diventi indietro nel buffer (n-1), mentre il buffer indietro 0 diventa il nuovo buffer anteriore.

</dd> <dt>

<span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**Copia di D3DSWAPEFFECT \_**
</dt> <dd>

Questo effetto di scambio può essere specificato solo per una catena di scambio che comprende un singolo buffer nascosto. Se la catena di scambio è a finestra o a schermo intero, il runtime garantirà la semantica implicita da un'operazione presente basata sulla copia, ovvero che l'operazione lascia invariato il contenuto del buffer nascosto, anziché sostituirlo con il contenuto del buffer anteriore come operazione presente basata su capovolgimento.

Per una catena di scambio a schermo intero, il runtime usa una combinazione di operazioni di capovolgimento e operazioni di copia, supportata se necessario dai buffer nascosti, per eseguire l'operazione corrente. Di conseguenza, la presentazione viene sincronizzata con la ritraccia verticale della scheda di visualizzazione e la relativa frequenza è vincolata dall'intervallo di presentazione scelto. Una catena di scambio specificata con il \_ \_ flag immediato intervallo D3DPRESENT è l'unica eccezione. (Fare riferimento alla descrizione del membro **PresentationIntervals** della struttura dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) ). In questo caso, un'operazione presente copia il contenuto del buffer nascosto direttamente nel buffer anteriore senza attendere la ritraccia verticale.

</dd> <dt>

<span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**\_Sovrapposizione D3DSWAPEFFECT**
</dt> <dd>

Usare un'area dedicata di memoria video che può essere sovrapposta all'area primaria. Non viene eseguita alcuna copia quando viene visualizzata la sovrimpressione. L'operazione di sovrapposizione viene eseguita in hardware, senza modificare i dati nell'area primaria.

|                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> D3DSWAPEFFECT \_ overlay è disponibile solo in Direct3D9Ex in esecuzione su Windows 7 (o più sistemi operativi correnti).<br/> |

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**\_FLIPEX D3DSWAPEFFECT**
</dt> <dd>

Designa quando un'applicazione sta adottando la modalità Flip, durante il quale viene passato il frame di un'applicazione anziché copiato nella Gestione finestre desktop (DWM) per la composizione quando l'applicazione presenta la modalità finestra. La modalità Flip consente a un'applicazione di utilizzare la larghezza di banda della memoria in modo più efficiente, oltre a consentire a un'applicazione di sfruttare le statistiche presenti a schermo intero. La modalità Flip non influisce sul comportamento a schermo intero.

> [!Note]  
> Se si crea una catena di scambio con D3DSWAPEFFECT \_ FLIPEX, non è possibile eseguire l'override del membro **hDeviceWindow** della struttura dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) quando si presenta un nuovo frame per la visualizzazione. Ovvero, è necessario passare **null** al parametro *hDestWindowOverride* di [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) per indicare al runtime di usare il membro **hDeviceWindow** dei **\_ parametri D3DPRESENT** per la presentazione.

|                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> D3DSWAPEFFECT \_ FLIPEX è disponibile solo in Direct3D9Ex in esecuzione su Windows 7 (o più sistemi operativi correnti).<br/> |

</dd> <dt>

<span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Lo stato del buffer nascosto dopo una chiamata a present è ben definito da ognuno di questi effetti di swap e indica se il dispositivo Direct3D è stato creato con una catena di scambio a schermo intero o una catena di scambio a finestra non ha alcun effetto su questo stato. In particolare, l' \_ effetto di D3DSWAPEFFECT Flip swap funziona allo stesso modo, sia a finestra che a schermo intero, e il runtime Direct3D garantisce questo problema creando buffer aggiuntivi. Di conseguenza, è consigliabile che le applicazioni usino D3DSWAPEFFECT \_ scarti, quando possibile, per evitare tali sanzioni. Questo è dovuto al fatto che questo effetto di scambio sarà sempre il più efficiente in termini di utilizzo della memoria e delle prestazioni.

Le applicazioni che usano D3DSWAPEFFECT \_ Flip o D3DSWAPEFFECT \_ scarta non dovrebbero prevedere il funzionamento di Alpha di destinazione a schermo intero. Ciò significa che lo \_ stato di rendering DESTBLEND di D3DRS non funzionerà come previsto perché le catene di scambio a schermo intero con questi effetti di scambio non hanno un formato pixel esplicito dal punto di vista del driver. Il driver deduce che devono assumere il formato di visualizzazione, che non ha un canale alfa. Per ovviare a questo problema, seguire questa procedura:

-   Usare la \_ copia di D3DSWAPEFFECT.
-   Controllare il \_ flag D3DCAPS3 Alpha \_ FullScreen \_ Flip \_ o \_ scarto nel membro Caps3 della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) . Questo flag indica se il driver è in grado di eseguire la fusione alfa quando \_ si usa D3DSWAPEFFECT Flip o D3DSWAPEFFECT \_ scarto.
-   Le applicazioni che usano l'effetto di swap della modalità Flip (D3DSWAPEFFECT \_ FLIPEX) devono chiamare [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) dopo la modifica di un ridimensionamento o di un'area della finestra per garantire che il contenuto visualizzato venga aggiornato.

Una finestra invisibile non può ricevere eventi in modalità utente; Inoltre, una finestra a schermo intero invisibile interferirà con la presentazione di un'altra finestra in modalità finestra di un'altra applicazione. Pertanto, ogni applicazione deve garantire che una finestra del dispositivo sia visibile quando un presentazione catena viene presentato in modalità a schermo intero.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)

[**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
