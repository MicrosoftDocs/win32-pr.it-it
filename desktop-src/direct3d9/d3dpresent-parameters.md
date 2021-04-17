---
description: Descrive i parametri di presentazione.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: Struttura D3DPRESENT_PARAMETERS (D3D9Types. h)
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
ms.openlocfilehash: f83ab03773356a01c8c6ac490bb099c6e7508be2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355059"
---
# <a name="d3dpresent_parameters-structure"></a>\_Struttura dei parametri D3DPRESENT

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

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Larghezza dei buffer indietro della nuova catena di scambio, in pixel. Se la **finestra** è **impostata su false** (la presentazione è a schermo intero), questo valore deve essere uguale alla larghezza di una delle modalità di visualizzazione enumerate trovate tramite [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Se la **finestra** è **true** e **BackBufferWidth** o **BackBufferHeight** è zero, viene acquisita la dimensione corrispondente dell'area client di **hDeviceWindow** (o la finestra di stato attivo, se **hDeviceWindow** è **null**).

</dd> <dt>

**BackBufferHeight**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altezza dei buffer indietro della nuova catena di scambio, in pixel. Se la **finestra** è **impostata su false** (la presentazione è a schermo intero), questo valore deve corrispondere all'altezza di una delle modalità di visualizzazione enumerate individuate tramite [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes). Se la **finestra** è **true** e **BackBufferWidth** o **BackBufferHeight** è zero, viene acquisita la dimensione corrispondente dell'area client di **hDeviceWindow** (o la finestra di stato attivo, se **hDeviceWindow** è **null**).

</dd> <dt>

**BackBufferFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Il formato del buffer nascosto. Per ulteriori informazioni sui formati, vedere [D3DFORMAT](d3dformat.md). Questo valore deve essere uno dei formati di destinazione di rendering convalidato da [**CheckDeviceType**](/windows/desktop/api). È possibile usare [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) per ottenere il formato corrente.

In realtà, \_ è possibile specificare D3DFMT Unknown per **BackBufferFormat** in modalità Window. In questo modo si indica al runtime di usare il formato di visualizzazione corrente e si elimina la necessità di chiamare [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).

Per le applicazioni a finestra, il formato del buffer nascosto non deve più corrispondere al formato della modalità di visualizzazione, perché la conversione dei colori può ora essere eseguita dall'hardware (se l'hardware supporta la conversione dei colori). Il set di possibili formati di buffer indietro è vincolato, ma il runtime consentirà di presentare qualsiasi formato di buffer nascosto valido da presentare a qualsiasi formato desktop. È necessario che il dispositivo sia utilizzabile sul desktop. i dispositivi in genere non funzionano in modalità a 8 bit per pixel.

Le applicazioni a schermo intero non possono eseguire la conversione di colori.

</dd> <dt>

**BackBufferCount**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Questo valore può essere compreso tra 0 e [D3DPRESENT \_ back \_ buffers \_ Max](d3dpresent-back-buffers.md) (o [D3DPRESENT \_ buffer back \_ \_ Max \_ ex](d3dpresent-back-buffers.md) quando si usa Direct3D 9Ex). I valori 0 vengono considerati come 1. Se non è possibile creare il numero di buffer indietro, il runtime non riuscirà a eseguire la chiamata al metodo e a riempire questo valore con il numero di buffer back che è possibile creare. Di conseguenza, un'applicazione può chiamare il metodo due volte con la stessa \_ struttura di parametri D3DPRESENT e prevedere che funzioni la seconda volta.

Il metodo ha esito negativo se non è possibile creare un buffer nascosto. Il valore di **BackBufferCount** influenza il set di effetti di scambio consentito. In particolare, qualsiasi \_ effetto di scambio di copia di D3DSWAPEFFECT richiede che esista esattamente un buffer nascosto.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Tipo: **[ **D3DMULTISAMPLE \_**](./d3dmultisample-type.md)**

</dd> <dd>

Membro del tipo enumerato di [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) . Il valore deve essere D3DMULTISAMPLE \_ None, a meno che **SwapEffect** non sia stato impostato su D3DSWAPEFFECT \_ Ignora. Il campionamento multiplo è supportato solo se l'effetto di scambio è D3DSWAPEFFECT \_ scarto.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Livello di qualità. L'intervallo valido è compreso tra zero e uno minore del livello restituito da pQualityLevels usato da [**CheckDeviceMultiSampleType**](/windows/desktop/api). Se si passa un valore maggiore, viene restituito l'errore D3DERR \_ INVALIDCALL. I valori abbinati delle destinazioni di rendering o delle superfici di depth stencil e del [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) devono corrispondere.

</dd> <dt>

**SwapEffect**
</dt> <dd>

Tipo: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**

</dd> <dd>

Membro del tipo enumerato [**D3DSWAPEFFECT**](./d3dswapeffect.md) . Il runtime garantirà la semantica implicita sul comportamento di scambio del buffer; Se, pertanto, la **finestra** è **true** e **SwapEffect** è impostato su D3DSWAPEFFECT \_ Flip, il runtime creerà un ulteriore buffer indietro e copierà a seconda di quale diventa il buffer anteriore al momento della presentazione.

\_Per la copia di D3DSWAPEFFECT è necessario che **BackBufferCount** sia impostato su 1.

D3DSWAPEFFECT \_ scarto verrà applicato nel runtime di debug riempiendo qualsiasi buffer con rumore dopo la presentazione.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D9 e Direct3D9Ex<br/> In Direct3D9Ex, D3DSWAPEFFECT \_ FLIPEX viene aggiunto per indicare quando un'applicazione sta adottando la modalità Flip. Ovvero, whan il frame di un'applicazione viene passato in modalità della finestra (anziché copiato) al Gestione finestre desktop (DWM) per la composizione. La modalità Flip garantisce una larghezza di banda di memoria più efficiente e consente a un'applicazione di sfruttare le statistiche presenti a schermo intero. Non modifica il comportamento a schermo intero. Il comportamento della modalità Flip è disponibile a partire da Windows 7.<br/> |



 

</dd> <dt>

**hDeviceWindow**
</dt> <dd>

Tipo: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

La finestra del dispositivo determina la posizione e le dimensioni del buffer nascosto sullo schermo. Viene usato da Direct3D quando il contenuto del buffer nascosto viene copiato nel buffer anteriore durante il [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

-   Per un'applicazione a schermo intero, si tratta di un handle per la finestra superiore (ovvero la finestra di stato attivo).

    Per le applicazioni che usano più dispositivi a schermo intero, ad esempio un sistema a più monitor, un solo dispositivo può usare la finestra di stato attivo come finestra del dispositivo. Tutti gli altri dispositivi devono avere finestre del dispositivo univoche.

-   Per un'applicazione in modalità finestra, questo handle sarà la finestra di destinazione predefinita per il [**presente**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Se questo handle è **null**, verrà eseguita la finestra messa a fuoco.

Si noti che non viene eseguito alcun tentativo da parte del runtime di riflettere le modifiche dell'utente nelle dimensioni della finestra. Il buffer nascosto non viene reimpostato in modo implicito quando viene reimpostata questa finestra. Tuttavia, il metodo [**attuale**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) rileva automaticamente le modifiche alla posizione della finestra.

</dd> <dt>

**Finestra**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

**True** se l'applicazione viene eseguita con finestra; **False** se l'applicazione viene eseguita a schermo intero.

</dd> <dt>

**EnableAutoDepthStencil**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Se questo valore è **true**, Direct3D gestirà i buffer di profondità per l'applicazione. Il dispositivo creerà un buffer di stencil Depth quando viene creato. Il buffer di stencil Depth verrà impostato automaticamente come destinazione di rendering del dispositivo. Quando il dispositivo viene reimpostato, il buffer di stencil Depth verrà automaticamente eliminato e ricreato con le nuove dimensioni.

Se EnableAutoDepthStencil è **true**, AutoDepthStencilFormat deve essere un formato di stencil Depth valido.

</dd> <dt>

**AutoDepthStencilFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro del tipo enumerato [D3DFORMAT](d3dformat.md) . Formato della superficie di stencil di profondità automatica che il dispositivo creerà. Questo membro viene ignorato a meno che **EnableAutoDepthStencil** non sia **true**.

</dd> <dt>

**Flag**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Una delle costanti [D3DPRESENTFLAG](d3dpresentflag.md) .

</dd> <dt>

**RefreshRateInHz a schermo intero \_**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Velocità con cui l'adattatore di visualizzazione aggiorna lo schermo. Il valore dipende dalla modalità in cui l'applicazione è in esecuzione:

-   Per la modalità finestra, la frequenza di aggiornamento deve essere 0.
-   Per la modalità schermo intero, la frequenza di aggiornamento è una delle frequenze di aggiornamento restituite da [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).

</dd> <dt>

**PresentationInterval**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Frequenza massima con cui i buffer indietro della catena di scambio possono essere presentati al buffer anteriore. Per una spiegazione dettagliata delle modalità e degli intervalli supportati, vedere [D3DPRESENT](d3dpresent.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



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

 

 
