---
description: Descrive i parametri di presentazione.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: D3DPRESENT_PARAMETERS struttura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 543b6b40d3fe24f902eb999a9377b8dbf60e1baa31efb70febbd2c0261d47305
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857441"
---
# <a name="d3dpresent_parameters-structure"></a>Struttura PARAMETERS \_ D3DPRESENT

Descrive i parametri di presentazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a>Members

<dl> <dt>

**BackBufferWidth**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza in pixel dei buffer indietro della nuova catena di scambio. Se **Windowed** è **FALSE** (la presentazione è a schermo intero), questo valore deve corrispondere alla larghezza di una delle modalità di visualizzazione enumerate trovate tramite [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Se **Windowed** è **TRUE** e **BackBufferWidth** o **BackBufferHeight** è zero, viene presa la dimensione corrispondente dell'area client di **hDeviceWindow** (o della finestra di stato attivo, se **hDeviceWindow** è **NULL).**

</dd> <dt>

**BackBufferHeight**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza in pixel dei buffer indietro della nuova catena di scambio. Se **Windowed** è **FALSE** (la presentazione è a schermo intero), questo valore deve corrispondere all'altezza di una delle modalità di visualizzazione enumerate trovate tramite [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Se **Windowed** è **TRUE** e **BackBufferWidth** o **BackBufferHeight** è zero, viene presa la dimensione corrispondente dell'area client di **hDeviceWindow** (o della finestra di stato attivo, se **hDeviceWindow** è **NULL).**

</dd> <dt>

**BackBufferFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Formato del buffer nascosto. Per altre informazioni sui formati, vedere [D3DFORMAT](d3dformat.md). Questo valore deve essere uno dei formati di destinazione di rendering convalidati da [**CheckDeviceType.**](/windows/desktop/api) È possibile usare [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) per ottenere il formato corrente.

In realtà, È possibile specificare D3DFMT \_ UNKNOWN per **BackBufferFormat** in modalità finestra. Ciò indica al runtime di usare il formato corrente della modalità di visualizzazione ed elimina la necessità di chiamare [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).

Per le applicazioni con finestra, il formato del buffer nascosto non deve più corrispondere al formato della modalità di visualizzazione perché la conversione dei colori può ora essere eseguita dall'hardware (se l'hardware supporta la conversione dei colori). Il set di possibili formati di buffer nascosto è vincolato, ma il runtime consentirà di presentare qualsiasi formato di buffer nascosto valido in qualsiasi formato desktop. Esiste il requisito aggiuntivo che il dispositivo sia operabile nel desktop. I dispositivi in genere non funzionano in modalità a 8 bit per pixel.

Le applicazioni a schermo intero non possono eseguire la conversione dei colori.

</dd> <dt>

**BackBufferCount**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Questo valore può essere compreso tra 0 e [D3DPRESENT \_ BACK \_ BUFFERS \_ MAX](d3dpresent-back-buffers.md) (o [D3DPRESENT \_ BACK \_ BUFFERS MAX \_ \_ EX](d3dpresent-back-buffers.md) quando si usa Direct3D 9Ex). I valori 0 vengono considerati come 1. Se non è possibile creare il numero di buffer nascosto, il runtime avrà esito negativo nella chiamata al metodo e riempirà questo valore con il numero di buffer che è possibile creare. Di conseguenza, un'applicazione può chiamare il metodo due volte con la stessa struttura PARAMETERS D3DPRESENT e prevede che \_ funzioni la seconda volta.

Il metodo ha esito negativo se non è possibile creare un buffer nascosto. Il valore di **BackBufferCount** influisce sul set di effetti di scambio consentiti. In particolare, qualsiasi effetto di scambio COPY D3DSWAPEFFECT richiede che sia \_ presente esattamente un buffer nascosto.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Tipo: **[ **D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DMULTISAMPLE \_ TYPE.**](./d3dmultisample-type.md) Il valore deve essere D3DMULTISAMPLE NONE a meno che SwapEffect non sia stato \_ impostato su  D3DSWAPEFFECT \_ DISCARD. Il multicampionamento è supportato solo se l'effetto di scambio è D3DSWAPEFFECT \_ DISCARD.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Livello di qualità. L'intervallo valido è compreso tra zero e uno minore del livello restituito da pQualityLevels usato da [**CheckDeviceMultiSampleType.**](/windows/desktop/api) Il passaggio di un valore più grande restituisce l'errore D3DERR \_ INVALIDCALL. I valori associati delle destinazioni di rendering o depth stencil superfici e [**D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md) devono corrispondere.

</dd> <dt>

**SwapEffect**
</dt> <dd>

Tipo: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**

</dd> <dd>

Membro del [**tipo enumerato D3DSWAPEFFECT.**](./d3dswapeffect.md) Il runtime garantirà la semantica implicita relativa al comportamento di scambio del buffer. Pertanto, se **Windowed** è **TRUE** e **SwapEffect** è impostato su D3DSWAPEFFECT FLIP, il runtime creerà un buffer nascosto aggiuntivo e copierà quello che diventa il front buffer in fase di \_ presentazione.

D3DSWAPEFFECT \_ COPY richiede che **BackBufferCount** sia impostato su 1.

D3DSWAPEFFECT DISCARD verrà applicato nel runtime di debug riempiendo qualsiasi buffer con \_ rumore dopo la presentazione.

Differenze tra Direct3D9 e Direct3D9Ex:

- In Direct3D9Ex, D3DSWAPEFFECT FLIPEX viene aggiunto per designare quando un'applicazione \_ adotta la modalità flip. Ovvero, il frame di un'applicazione viene passato in modalità finestra (anziché copiato) al Gestione finestre desktop(DWM) per la composizione. La modalità flip offre una larghezza di banda di memoria più efficiente e consente a un'applicazione di sfruttare le statistiche presenti a schermo intero. Non modifica il comportamento a schermo intero. Il comportamento della modalità capovolgimento è disponibile a partire Windows 7.



 

</dd> <dt>

**hDeviceWindow**
</dt> <dd>

Tipo: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

La finestra del dispositivo determina la posizione e le dimensioni del buffer nascosto sullo schermo. Viene usato da Direct3D quando il contenuto del buffer nascosto viene copiato nel front buffer durante [**present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

-   Per un'applicazione a schermo intero, si tratta di un handle per la finestra superiore ,ovvero la finestra attiva.

    Per le applicazioni che usano più dispositivi a schermo intero ,ad esempio un sistema multimonitoraggio, esattamente un dispositivo può usare la finestra dello stato attivo come finestra del dispositivo. Tutti gli altri dispositivi devono avere finestre del dispositivo univoche.

-   Per un'applicazione in modalità finestra, questo handle sarà la finestra di destinazione predefinita per [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Se questo handle è **NULL,** verrà utilizzata la finestra di stato attivo.

Si noti che il runtime non tenta di riflettere le modifiche apportate dall'utente alle dimensioni della finestra. Il buffer nascosto non viene reimpostato in modo implicito quando questa finestra viene reimpostata. Tuttavia, il [**metodo Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) tiene traccia automaticamente delle modifiche alla posizione della finestra.

</dd> <dt>

**Finestra**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

**TRUE** se l'applicazione viene eseguita in finestra; **FALSE** se l'applicazione viene eseguita a schermo intero.

</dd> <dt>

**EnableAutoDepthStencil**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Se questo valore è **TRUE,** Direct3D gestirà i buffer di profondità per l'applicazione. Il dispositivo creerà un buffer depth-stencil al momento della creazione. Il buffer depth-stencil verrà impostato automaticamente come destinazione di rendering del dispositivo. Quando il dispositivo viene reimpostato, il buffer depth-stencil verrà automaticamente eliminato e ricreato con le nuove dimensioni.

Se EnableAutoDepthStencil è **TRUE,** AutoDepthStencilFormat deve essere un formato depth-stencil valido.

</dd> <dt>

**AutoDepthStencilFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro del [tipo enumerato D3DFORMAT.](d3dformat.md) Formato della superficie depth-stencil automatica che verrà creata dal dispositivo. Questo membro viene ignorato a meno **che EnableAutoDepthStencil non** sia **TRUE.**

</dd> <dt>

**Flag**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Una delle [costanti D3DPRESENTFLAG.](d3dpresentflag.md)

</dd> <dt>

**\_RefreshRateInHz a schermo intero**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Frequenza con cui la scheda di visualizzazione aggiorna lo schermo. Il valore dipende dalla modalità di esecuzione dell'applicazione:

-   Per la modalità finestra, la frequenza di aggiornamento deve essere 0.
-   Per la modalità schermo intero, la frequenza di aggiornamento è una delle frequenze di aggiornamento restituite da [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).

</dd> <dt>

**PresentationInterval**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Velocità massima con cui i buffer back della catena di scambio possono essere presentati al front buffer. Per una spiegazione dettagliata delle modalità e degli intervalli supportati, vedere [D3DPRESENT](d3dpresent.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[**Presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
