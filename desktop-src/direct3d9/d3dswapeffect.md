---
description: Definisce gli effetti di scambio.
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
ms.openlocfilehash: 58354e35ca8456f6fde57d2f2567a6b6a202f6d7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343036"
---
# <a name="d3dswapeffect-enumeration"></a>Enumerazione D3DSWAPEFFECT

Definisce gli effetti di scambio.

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

<span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT \_ DISCARD**
</dt> <dd>

Quando viene creata una catena di scambio con un effetto swap di D3DSWAPEFFECT FLIP o D3DSWAPEFFECT COPY, il runtime garantisce che \_ un'operazione \_ [**IDirect3DDevice9::P resente**](/windows/desktop/api) non influirà sul contenuto di alcun buffer nascosto. Sfortunatamente, soddisfare questa garanzia può comportare notevoli sovraccarici di elaborazione o memoria video, soprattutto quando si implementa la semantica di capovolgimento per una catena di scambio a finestre o la semantica di copia per una catena di scambio a schermo intero. Un'applicazione può usare l'effetto swap DISCARD D3DSWAPEFFECT per evitare questi sovraccarici e consentire al driver di visualizzazione di selezionare la tecnica di presentazione più efficiente \_ per la catena di scambio. Questo è anche l'unico effetto di scambio che può essere usato quando si specifica un valore diverso da D3DMULTISAMPLE NONE per il membro \_ MultiSampleType [**di D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md).

Analogamente a una catena di scambio che usa D3DSWAPEFFECT FLIP, una catena di scambio che usa D3DSWAPEFFECT DISCARD può includere più buffer nascosto, a cui è possibile accedere usando \_ \_ [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) o [**IDirect3DSwapChain9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer). La catena di scambio è meglio definita come una coda in cui 0 indicizza sempre il buffer nascosto che verrà visualizzato dalla successiva operazione Present e da cui i buffer vengono eliminati quando sono stati visualizzati.

Un'applicazione che usa questo effetto di scambio non può fare supposizioni sul contenuto di un buffer nascosto eliminato e pertanto deve aggiornare un intero buffer nascosto prima di richiamare un'operazione Present che lo visualizza. Anche se questa operazione non viene applicata, la versione di debug del runtime sovrascriverà il contenuto dei buffer nascosto eliminati con dati casuali per consentire agli sviluppatori di verificare che le applicazioni aggiornino correttamente l'intera superficie del buffer nascosto.

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**CAPOVOLGIMENTO D3DSWAPEFFECT \_**
</dt> <dd>

La catena di scambio può includere più buffer back ed è più adatta come coda circolare che include il front buffer. All'interno di questa coda, i buffer nascosto sono sempre numerati in sequenza da 0 a (n - 1), dove n è il numero di buffer inversi, in modo che 0 denoti il buffer presentato meno di recente. Quando viene richiamato Present, la coda viene "ruotata" in modo che il buffer anteriore diventi buffer nascosto (n - 1), mentre il buffer nascosto 0 diventa il nuovo front buffer.

</dd> <dt>

<span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**COPIA D3DSWAPEFFECT \_**
</dt> <dd>

Questo effetto di scambio può essere specificato solo per una catena di scambio che comprende un singolo buffer nascosto. Indipendentemente dal fatto che la catena di scambio sia in modalità finestra o a schermo intero, il runtime garantisce la semantica implicita in un'operazione Present basata sulla copia, in modo che il contenuto del buffer nascosto non sia modificato, anziché sostituirlo con il contenuto del front buffer come farebbe un'operazione Present basata su capovolgimento.

Per una catena di scambio a schermo intero, il runtime usa una combinazione di operazioni di capovolgimento e di copia, supportate se necessario dai buffer nascosto, per eseguire l'operazione Present. Di conseguenza, la presentazione viene sincronizzata con il retrace verticale della scheda video e la frequenza è vincolata dall'intervallo di presentazione scelto. Una catena di scambio specificata con il flag D3DPRESENT \_ INTERVAL \_ IMMEDIATE è l'unica eccezione. Vedere la descrizione del **membro PresentationIntervals** della [**struttura D3DPRESENT \_ PARAMETERS.**](d3dpresent-parameters.md) In questo caso, un'operazione Present copia il contenuto del buffer nascosto direttamente nel front buffer senza attendere il retrace verticale.

</dd> <dt>

<span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**SOVRIMPRESSIONE D3DSWAPEFFECT \_**
</dt> <dd>

Usare un'area dedicata di memoria video che può essere sovrimpressa sulla superficie primaria. Non viene eseguita alcuna copia quando viene visualizzata la sovrimpressione. L'operazione di sovrapposizione viene eseguita nell'hardware, senza modificare i dati nella superficie primaria.

Differenze tra Direct3D 9 e Direct3D 9Ex:

- D3DSWAPEFFECT \_ OVERLAY è disponibile solo in Direct3D9Ex in esecuzione in Windows 7 (o nel sistema operativo corrente).

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ FLIPEX**
</dt> <dd>

Specifica quando un'applicazione adotta la modalità flip, durante il quale viene passato il frame di un'applicazione anziché copiarlo nel Gestione finestre desktop (DWM) per la composizione quando l'applicazione viene visualizzata in modalità a finestre. La modalità flip consente a un'applicazione di usare in modo più efficiente la larghezza di banda della memoria, nonché di consentire a un'applicazione di sfruttare le statistiche presenti a schermo intero. La modalità di capovolgimento non influisce sul comportamento a schermo intero.

> [!Note]  
> Se si crea una catena di scambio con D3DSWAPEFFECT FLIPEX, non è possibile eseguire l'override del membro \_ **hDeviceWindow** della struttura [**PARAMETERS D3DPRESENT \_**](d3dpresent-parameters.md) quando si presenta un nuovo frame per la visualizzazione. In altre informazioni, è necessario passare **NULL** al parametro *hDestWindowOverride* [**di IDirect3DDevice9Ex::P resentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) per indicare al runtime di usare il membro **hDeviceWindow** di **D3DPRESENT \_ PARAMETERS** per la presentazione.

Differenze tra Direct3D 9 e Direct3D 9Ex:

- D3DSWAPEFFECT FLIPEX è disponibile solo \_ in Direct3D9Ex in esecuzione in Windows 7 (o nel sistema operativo corrente).

</dd> <dt>

<span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Lo stato del buffer nascosto dopo una chiamata a Present è ben definito da ognuno di questi effetti di scambio e se il dispositivo Direct3D è stato creato con una catena di scambio a schermo intero o una catena di scambio finestra non ha alcun effetto su questo stato. In particolare, l'effetto flip FLIP D3DSWAPEFFECT funziona allo stesso modo sia a finestra che a schermo intero e il runtime Direct3D garantisce questo effetto creando \_ buffer aggiuntivi. Di conseguenza, è consigliabile che le applicazioni usino D3DSWAPEFFECT DISCARD quando possibile per \_ evitare tali sanzioni. Questo è dovuto al fatto che questo effetto di scambio sarà sempre il più efficiente in termini di utilizzo e prestazioni della memoria.

Le applicazioni che usano D3DSWAPEFFECT FLIP o \_ D3DSWAPEFFECT DISCARD non devono prevedere il funzionamento del valore alfa di \_ destinazione a schermo intero. Ciò significa che lo stato di rendering D3DRS DESTBLEND non funzionerà come previsto perché le catene di scambio a schermo intero con questi effetti di scambio non hanno un formato pixel esplicito dal punto di vista del \_ driver. Il driver deduce che deve assumere il formato di visualizzazione, che non ha un canale alfa. Per risolvere il problema, seguire questa procedura:

-   Usare D3DSWAPEFFECT \_ COPY.
-   Controllare il flag ALPHA FULLSCREEN FLIP OR DISCARD di D3DCAPS3 nel membro \_ \_ \_ \_ \_ Caps3 della [**struttura D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) Questo flag indica se il driver può eseguire la fusione alfa quando si usa D3DSWAPEFFECT FLIP o \_ D3DSWAPEFFECT \_ DISCARD.
-   Le applicazioni che usano l'effetto swap in modalità capovolgimento (D3DSWAPEFFECT FLIPEX) devono chiamare PresentEx dopo il ridimensionamento di una finestra o la modifica dell'area per garantire che il contenuto visualizzato \_ venga aggiornato. [](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)

Una finestra invisibile non può ricevere eventi in modalità utente. inoltre, una finestra invisibile a schermo intero interferirà con la presentazione della finestra in modalità finestra di un'altra applicazione. Pertanto, ogni applicazione deve garantire che una finestra del dispositivo sia visibile quando un swapchain viene presentato in modalità schermo intero.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |

## <a name="see-also"></a>Vedi anche

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)

[**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
