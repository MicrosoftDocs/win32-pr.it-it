---
description: Gli Stati di rendering definiscono gli Stati di configurazione per tutti i tipi di elaborazione dei vertici e dei pixel.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Enumerazione D3DRENDERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2386762eaa45f1eefbccac97723c3ad71c3a76fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322309"
---
# <a name="d3drenderstatetype-enumeration"></a>Enumerazione D3DRENDERSTATETYPE

Gli Stati di rendering definiscono gli Stati di configurazione per tutti i tipi di elaborazione dei vertici e dei pixel. Alcuni Stati di rendering configurano l'elaborazione dei vertici e alcuni configurano l'elaborazione dei pixel (vedere [gli Stati di rendering (Direct3D 9)](render-states.md)). Gli Stati di rendering possono essere salvati e ripristinati usando stateblocks (vedere lo stato [di salvataggio e ripristino del blocco di stato (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**\_ZENABLE D3DRS**
</dt> <dd>

Stato del buffer di profondità come un membro del tipo enumerato [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) . Impostare questo stato su D3DZB \_ true per abilitare il buffering z, D3DZB \_ USEW per abilitare il buffering w o D3DZB \_ false per disabilitare il buffering di profondità.

Il valore predefinito per questo stato di rendering è D3DZB \_ true se è stato creato un depth stencil insieme alla catena di scambio impostando il membro EnableAutoDepthStencil della struttura dei [**\_ parametri D3DPRESENT**](d3dpresent-parameters.md) su **true** e D3DZB \_ false in caso contrario.

</dd> <dt>

<span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**\_FillMode D3DRS**
</dt> <dd>

Uno o più membri del tipo enumerato [**D3DFILLMODE**](./d3dfillmode.md) . Il valore predefinito è D3DFILL \_ Solid.

</dd> <dt>

<span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**\_MODOOMBRA D3DRS**
</dt> <dd>

Uno o più membri del tipo enumerato [**D3DSHADEMODE**](./d3dshademode.md) . Il valore predefinito è D3DSHADE \_ Gouraud.

</dd> <dt>

<span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**\_ZWRITEENABLE D3DRS**
</dt> <dd>

**True** per consentire all'applicazione di scrivere nel buffer di profondità. Il valore predefinito è **true**. Questo membro consente a un'applicazione di impedire al sistema di aggiornare il buffer di profondità con nuovi valori di profondità. Se **false**, i confronti di profondità vengono ancora eseguiti in base allo stato di rendering D3DRS \_ ZFUNC, presupponendo che venga eseguita la memorizzazione nel buffer di profondità, ma i valori di profondità non vengono scritti nel buffer.

</dd> <dt>

<span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**\_ALPHATESTENABLE D3DRS**
</dt> <dd>

**True** per abilitare il test alfa per pixel. Se il test viene superato, il pixel viene elaborato dal buffer del frame. In caso contrario, l'elaborazione del buffer di frame viene ignorata per il pixel.

Il test viene eseguito confrontando il valore alfa in ingresso con il valore alfa di riferimento, usando la funzione di confronto fornita dallo \_ stato di rendering ALPHAFUNC di D3DRS. Il valore alfa di riferimento è determinato dal valore impostato per D3DRS \_ ALPHAREF. Per altre informazioni, vedere [stato di test Alfa (Direct3D 9)](alpha-testing-state.md).

Il valore predefinito di questo parametro è **false**.

</dd> <dt>

<span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**\_LASTPIXEL D3DRS**
</dt> <dd>

Il valore predefinito è **true**, che consente di disegnare l'ultimo pixel in una riga. Per impedire il disegno dell'ultimo pixel, impostare questo valore su **false**. Per altre informazioni, vedere [stato di contorno e riempimento (Direct3D 9)](outline-and-fill-state.md).

</dd> <dt>

<span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**\_SRCBLEND D3DRS**
</dt> <dd>

Un membro del tipo enumerato [**D3DBLEND**](./d3dblend.md) . Il valore predefinito è D3DBLEND \_ One.

</dd> <dt>

<span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**\_DESTBLEND D3DRS**
</dt> <dd>

Un membro del tipo enumerato [**D3DBLEND**](./d3dblend.md) . Il valore predefinito è D3DBLEND \_ zero.

</dd> <dt>

<span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**\_CULLMODE D3DRS**
</dt> <dd>

Specifica il modo in cui i triangoli rivolti al back-end vengono abbattuti, se presenti. Questo può essere impostato su un membro del tipo enumerato [**D3DCULL**](./d3dcull.md) . Il valore predefinito è D3DCULL \_ CCW.

</dd> <dt>

<span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**\_ZFUNC D3DRS**
</dt> <dd>

Un membro del tipo enumerato [**D3DCMPFUNC**](./d3dcmpfunc.md) . Il valore predefinito è D3DCMP \_ LESSEQUAL. Questo membro consente a un'applicazione di accettare o rifiutare un pixel, in base alla distanza dalla fotocamera.

Il valore di profondità del pixel viene confrontato con il valore del buffer di profondità. Se il valore di profondità del pixel supera la funzione di confronto, viene scritto il pixel.

Il valore di profondità viene scritto nel buffer di profondità solo se lo stato di rendering è **true**.

I rasterizzatori software e molti acceleratori hardware funzionano più velocemente se il test di profondità ha esito negativo, perché non è necessario filtrare e modulare la trama se non viene eseguito il rendering del pixel.

</dd> <dt>

<span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**\_ALPHAREF D3DRS**
</dt> <dd>

Valore che specifica un valore alfa di riferimento rispetto al quale vengono testati i pixel quando è abilitato il test alfa. Si tratta di un valore a 8 bit inserito negli 8 bit bassi del valore di stato di rendering DWORD. I valori possono variare da 0x00000000 a 0x000000FF. Il valore predefinito è 0.

</dd> <dt>

<span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**\_ALPHAFUNC D3DRS**
</dt> <dd>

Un membro del tipo enumerato [**D3DCMPFUNC**](./d3dcmpfunc.md) . Il valore predefinito è D3DCMP \_ Always. Questo membro consente a un'applicazione di accettare o rifiutare un pixel, in base al relativo valore alfa.

</dd> <dt>

<span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**\_DITHERENABLE D3DRS**
</dt> <dd>

**True** per abilitare la dithering. Il valore predefinito è **false**.

</dd> <dt>

<span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**\_ALPHABLENDENABLE D3DRS**
</dt> <dd>

**True** per abilitare la trasparenza con Blend alfa. Il valore predefinito è **false**.

Il tipo di fusione alfa è determinato dagli \_ Stati di rendering D3DRS SRCBLEND e \_ D3DRS DESTBLEND.

</dd> <dt>

<span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**\_FOGENABLE D3DRS**
</dt> <dd>

**True** per abilitare la fusione di nebbia. Il valore predefinito è **false**. Per ulteriori informazioni sull'utilizzo della combinazione di nebbia, vedere [Fog](fog.md).

</dd> <dt>

<span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**\_SPECULARENABLE D3DRS**
</dt> <dd>

**True** per abilitare le evidenziazioni speculari. Il valore predefinito è **false**.

Le evidenziazioni speculari vengono calcolate come se ogni vertice nell'oggetto da illuminare è in corrispondenza dell'origine dell'oggetto. Ciò consente di ottenere i risultati previsti finché l'oggetto viene modellato intorno all'origine e la distanza tra la luce e l'oggetto è relativamente grande. In altri casi, i risultati non sono definiti.

Quando questo membro è impostato su **true**, il colore speculare viene aggiunto al colore di base dopo la propagazione della trama ma prima della fusione alfa.

</dd> <dt>

<span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**\_FogColor D3DRS**
</dt> <dd>

Valore il cui tipo è [**D3DCOLOR**](d3dcolor.md). Il valore predefinito è 0. Per altre informazioni sul colore di nebbia, vedere [nebbia color (Direct3D 9)](fog-color.md).

</dd> <dt>

<span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**\_FOGTABLEMODE D3DRS**
</dt> <dd>

Formula di nebbia da usare per la nebbia dei pixel. Impostare su uno dei membri del tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) . Il valore predefinito è D3DFOG \_ None. Per ulteriori informazioni sulla nebbia dei pixel, vedere [pixel Fog (Direct3D 9)](pixel-fog.md).

</dd> <dt>

<span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**\_FOGSTART D3DRS**
</dt> <dd>

Profondità con cui gli effetti di nebbia pixel o vertice iniziano per la modalità di nebbia lineare. Il valore predefinito è 0,0 f. La profondità viene specificata nello spazio globale per la nebbia dei vertici e nello spazio del dispositivo \[ 0,0, 1,0 \] o nello spazio globale per la nebbia dei pixel. Per la nebbia dei pixel, questi valori si trovano nello spazio del dispositivo quando il sistema usa la z per i calcoli di nebbia e lo spazio globale quando il sistema usa la nebbia relativa agli occhi (w-Fog). Per ulteriori informazioni, vedere la pagina relativa ai [parametri di nebbia (Direct3D 9)](fog-parameters.md) e alla [profondità basata sull'occhio](pixel-fog.md)rispetto alla Z.

I valori per questo stato di rendering sono valori a virgola mobile. Poiché il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**\_FOGEND D3DRS**
</dt> <dd>

Profondità con cui terminano gli effetti della nebbia del pixel o del vertice per la modalità di nebbia lineare. Il valore predefinito è 1.0 f. La profondità viene specificata nello spazio globale per la nebbia dei vertici e nello spazio del dispositivo \[ 0,0, 1,0 \] o nello spazio globale per la nebbia dei pixel. Per la nebbia dei pixel, questi valori si trovano nello spazio del dispositivo quando il sistema usa z per i calcoli di nebbia e nello spazio globale quando il sistema usa la nebbia relativa agli occhi (w-Fog). Per ulteriori informazioni, vedere la pagina relativa ai [parametri di nebbia (Direct3D 9)](fog-parameters.md) e alla [profondità basata sull'occhio](pixel-fog.md)rispetto alla Z.

I valori per questo stato di rendering sono valori a virgola mobile. Poiché il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**\_FOGDENSITY D3DRS**
</dt> <dd>

Densità di nebbia per la nebbia dei pixel o dei vertici usata nelle modalità di nebbia esponenziale (D3DFOG \_ exp e D3DFOG \_ exp2). I valori di densità validi sono compresi tra 0,0 e 1,0. Il valore predefinito è 1,0. Per altre informazioni, vedere [parametri di nebbia (Direct3D 9)](fog-parameters.md).

I valori per questo stato di rendering sono valori a virgola mobile. Poiché il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**\_RANGEFOGENABLE D3DRS**
</dt> <dd>

**True** per abilitare la nebbia del vertice basata sull'intervallo. Il valore predefinito è **false**, nel qual caso il sistema usa la nebbia basata sulla profondità. Nella nebbia basata sull'intervallo, la distanza di un oggetto dal visualizzatore viene utilizzata per calcolare gli effetti di nebbia, non la profondità dell'oggetto, ovvero la coordinata z, nella scena. Nella nebbia basata sull'intervallo, tutti i metodi Fog funzionano come di consueto, ad eccezione del fatto che usano l'intervallo anziché la profondità nei calcoli.

L'intervallo è il fattore corretto da usare per i calcoli di nebbia, ma viene comunemente usata la profondità perché l'intervallo richiede molto tempo per il calcolo e la profondità è in genere già disponibile. L'uso della profondità per calcolare la nebbia ha l'effetto indesiderato che la fogginess di oggetti periferici cambia quando lo spostamento degli occhi del visualizzatore, in questo caso la profondità cambia e l'intervallo rimane costante.

Poiché nessun hardware supporta attualmente la nebbia basata sull'intervallo per pixel, la correzione dell'intervallo viene offerta solo per la nebbia dei vertici.

Per altre informazioni, vedere [Vertex Fog (Direct3D 9)](vertex-fog.md).

</dd> <dt>

<span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**\_STENCILENABLE D3DRS**
</dt> <dd>

**True** per abilitare gli stencil oppure **false** per disabilitare lo stencil. Il valore predefinito è **false**. Per altre informazioni, vedere [tecniche di buffer di stencil (Direct3D 9)](stencil-buffer-techniques.md).

</dd> <dt>

<span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**\_STENCILFAIL D3DRS**
</dt> <dd>

Operazione dello stencil da eseguire se il test dello stencil ha esito negativo. I valori sono dal tipo enumerato [**D3DSTENCILOP**](./d3dstencilop.md) . Il valore predefinito è D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**\_STENCILZFAIL D3DRS**
</dt> <dd>

Operazione dello stencil da eseguire se il test di stencil viene superato e il test di profondità (z-test) ha esito negativo. I valori sono dal tipo enumerato [**D3DSTENCILOP**](./d3dstencilop.md) . Il valore predefinito è D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**\_STENCILPASS D3DRS**
</dt> <dd>

Operazione dello stencil da eseguire se vengono superati sia lo stencil che i test di profondità (z). I valori sono dal tipo enumerato [**D3DSTENCILOP**](./d3dstencilop.md) . Il valore predefinito è D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**\_STENCILFUNC D3DRS**
</dt> <dd>

Funzione di confronto per il test di stencil. I valori sono dal tipo enumerato [**D3DCMPFUNC**](./d3dcmpfunc.md) . Il valore predefinito è D3DCMP \_ Always.

La funzione di confronto viene utilizzata per confrontare il valore di riferimento con una voce del buffer di stencil. Questo confronto si applica solo ai bit del valore di riferimento e alla voce del buffer dello stencil impostati nella maschera dello stencil (impostata dallo \_ stato di rendering STENCILMASK di D3DRS). Se **true**, il test dello stencil viene superato.

</dd> <dt>

<span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**\_STENCILREF D3DRS**
</dt> <dd>

Valore di riferimento int per il test di stencil. Il valore predefinito è 0.

</dd> <dt>

<span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**\_STENCILMASK D3DRS**
</dt> <dd>

Maschera applicata al valore di riferimento e a ogni voce del buffer di stencil per determinare i bit significativi per il test di stencil. La maschera predefinita è 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**\_STENCILWRITEMASK D3DRS**
</dt> <dd>

Maschera di scrittura applicata ai valori scritti nel buffer dello stencil. La maschera predefinita è 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**\_TEXTUREFACTOR D3DRS**
</dt> <dd>

Colore usato per la fusione a più trame con l' \_ argomento D3DTA TFACTOR texture-blending o l' \_ operazione di combinazione di trame D3DTOP BLENDFACTORALPHA. Il valore associato è una variabile [**D3DCOLOR**](d3dcolor.md) . Il valore predefinito è opaco bianco (0xFFFFFFFF).

</dd> <dt>

<span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**\_WRAP0 D3DRS**
</dt> <dd>

Comportamento di wrapping della trama per più set di coordinate di trama. I valori validi per questo stato di rendering possono essere qualsiasi combinazione di D3DWRAPCOORD \_ 0 (o D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (o D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (o D3DWRAP \_ W) e D3DWRAPCOORD \_ 3 flag. In questo modo il sistema esegue il wrapping nella direzione della prima, della seconda, della terza e della quarta dimensione, a volte definita le direzioni s, t, r e q, per una determinata trama. Il valore predefinito per questo stato di rendering è 0 (wrapping disabilitato in tutte le direzioni).

</dd> <dt>

<span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**\_WRAP1 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**\_WRAP2 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**\_WRAP3 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**\_WRAP4 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**\_WRAP5 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**\_WRAP6 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**\_WRAP7 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**Ritaglio D3DRS \_**
</dt> <dd>

**True** per abilitare il ritaglio primitivo da Direct3D o **false** per disabilitarlo. Il valore predefinito è **true**.

</dd> <dt>

<span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**\_Illuminazione D3DRS**
</dt> <dd>

**True** per abilitare l'illuminazione Direct3D oppure **false** per disabilitarlo. Il valore predefinito è **true**. Solo i vertici che includono un vertice normale sono illuminati correttamente; i vertici che non contengono un normale impiegano un prodotto a virgola pari a 0 in tutti i calcoli di illuminazione.

</dd> <dt>

<span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**\_Ambiente D3DRS**
</dt> <dd>

Colore chiaro ambiente. Questo valore è di tipo [**D3DCOLOR**](d3dcolor.md). Il valore predefinito è 0.

</dd> <dt>

<span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**\_FOGVERTEXMODE D3DRS**
</dt> <dd>

Formula di nebbia da usare per la nebbia del vertice. Impostare su un membro del tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) . Il valore predefinito è D3DFOG \_ None.

</dd> <dt>

<span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**\_COLORVERTEX D3DRS**
</dt> <dd>

**True** per abilitare il colore per vertice o **false** per disabilitarlo. Il valore predefinito è **true**. L'abilitazione del colore per vertice consente al sistema di includere il colore definito per i singoli vertici nei calcoli di illuminazione.

Per ulteriori informazioni, vedere gli Stati di rendering seguenti:

-   \_DIFFUSEMATERIALSOURCE D3DRS
-   \_SPECULARMATERIALSOURCE D3DRS
-   \_AMBIENTMATERIALSOURCE D3DRS
-   \_EMISSIVEMATERIALSOURCE D3DRS

</dd> <dt>

<span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**\_LOCALVIEWER D3DRS**
</dt> <dd>

**True** per abilitare le evidenziazioni speculari relative alla fotocamera o **false** per usare le evidenziazioni speculari ortogonali. Il valore predefinito è **true**. Le applicazioni che usano la proiezione ortogonale devono specificare **false**.

</dd> <dt>

<span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**\_NORMALIZENORMALS D3DRS**
</dt> <dd>

**True** per abilitare la normalizzazione automatica delle normali dei vertici oppure **false** per disabilitarla. Il valore predefinito è **false**. L'abilitazione di questa funzionalità consente al sistema di normalizzare le normali dei vertici per i vertici dopo averli trasformati nello spazio della fotocamera, operazione che può richiedere molto tempo.

</dd> <dt>

<span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**\_DIFFUSEMATERIALSOURCE D3DRS**
</dt> <dd>

Origine dei colori diffusa per i calcoli di illuminazione. I valori validi sono membri del tipo enumerato [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . Il valore predefinito è D3DMCS \_ COLOR1. Il valore di questo stato di rendering viene utilizzato solo se lo \_ stato di rendering COLORVERTEX di D3DRS è impostato su **true**.

</dd> <dt>

<span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**\_SPECULARMATERIALSOURCE D3DRS**
</dt> <dd>

Origine colore speculare per i calcoli di illuminazione. I valori validi sono membri del tipo enumerato [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . Il valore predefinito è D3DMCS \_ color2.

</dd> <dt>

<span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**\_AMBIENTMATERIALSOURCE D3DRS**
</dt> <dd>

Origine del colore di ambiente per i calcoli di illuminazione. I valori validi sono membri del tipo enumerato [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . Il valore predefinito è \_ Material D3DMCS.

</dd> <dt>

<span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**\_EMISSIVEMATERIALSOURCE D3DRS**
</dt> <dd>

Origine colore emissivo per i calcoli di illuminazione. I valori validi sono membri del tipo enumerato [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . Il valore predefinito è \_ Material D3DMCS.

</dd> <dt>

<span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**\_VERTEXBLEND D3DRS**
</dt> <dd>

Numero di matrici da usare per eseguire la fusione di geometria, se disponibile. I valori validi sono membri del tipo enumerato [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Il valore predefinito è D3DVBF \_ Disable.

</dd> <dt>

<span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**\_CLIPPLANEENABLE D3DRS**
</dt> <dd>

Abilita o Disabilita i piani di ritaglio definiti dall'utente. I valori validi sono qualsiasi valore DWORD in cui lo stato di ogni bit (set o not set) consente di attivare/disabilitare lo stato di attivazione di un piano di ritaglio definito dall'utente corrispondente. Il bit meno significativo (bit 0) controlla il primo piano di ritaglio in corrispondenza dell'indice 0 e i bit successivi controllano l'attivazione dei piani di ritaglio con indici più elevati. Se è impostato un bit, il sistema applica il piano di ritaglio appropriato durante il rendering della scena. Il valore predefinito è 0.

Le macro [**D3DCLIPPLANEn**](d3dclipplanen.md) sono definite per fornire un modo pratico per abilitare i piani di ritaglio.

</dd> <dt>

<span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**\_POINTSIZE D3DRS**
</dt> <dd>

Valore float che specifica le dimensioni da utilizzare per il calcolo delle dimensioni del punto nei casi in cui non viene specificata la dimensione del punto per ogni vertice. Questo valore non viene usato quando il vertice contiene le dimensioni dei punti. Questo valore si trova in unità dello spazio dello schermo se D3DRS \_ POINTSCALEENABLE è **false**; in caso contrario, questo valore è in unità di spazio globale. Il valore predefinito è il valore restituito da un driver. Se un driver restituisce 0 o 1, il valore predefinito è 64, che consente l'emulazione delle dimensioni del punto software. Poiché il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ POINTSIZE \_ min**
</dt> <dd>

Valore float che specifica le dimensioni minime delle primitive di punti. Le primitive di punti vengono fissate a queste dimensioni durante il rendering. Se si imposta questa opzione su valori inferiori a 1,0, i punti vengono eliminati quando il punto non copre un pixel Center e l'anti-aliasing è disabilitato o viene sottoposto a rendering con intensità ridotta quando è abilitato l'anti-aliasing. Il valore predefinito è 1.0 f. L'intervallo per questo valore è maggiore o uguale a 0,0 f. Poiché il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**\_POINTSPRITEENABLE D3DRS**
</dt> <dd>

valore bool. Se è **true**, le coordinate di trama delle primitive di punti vengono impostate in modo da eseguire il mapping delle trame complete in ogni punto. Se è **false**, le coordinate di trama dei vertici vengono utilizzate per l'intero punto. Il valore predefinito è **false**. È possibile ottenere i punti a pixel singolo dello stile DirectX 7 impostando D3DRS \_ POINTSCALEENABLE su **false** e D3DRS \_ POINTSIZE su 1,0, che corrispondono ai valori predefiniti.

</dd> <dt>

<span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**\_POINTSCALEENABLE D3DRS**
</dt> <dd>

valore bool che controlla il calcolo delle dimensioni per le primitive puntiformi. Se è **true**, la dimensione del punto viene interpretata come valore di spazio della fotocamera e viene ridimensionata dalla funzione Distance e da tronco a viewport per il ridimensionamento dell'asse y per calcolare la dimensione finale dello spazio dello schermo. Se è **false**, le dimensioni del punto vengono interpretate come spazi dello schermo e utilizzate direttamente. Il valore predefinito è **false**.

</dd> <dt>

<span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_ A**
</dt> <dd>

Valore float che controlla l'attenuazione delle dimensioni basate sulla distanza per le primitive di punti. Attivo solo quando D3DRS \_ POINTSCALEENABLE è **true**. Il valore predefinito è 1.0 f. L'intervallo per questo valore è maggiore o uguale a 0,0 f. Poiché il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**
</dt> <dd>

Valore float che controlla l'attenuazione delle dimensioni basate sulla distanza per le primitive di punti. Attivo solo quando D3DRS \_ POINTSCALEENABLE è **true**. Il valore predefinito è 0,0 f. L'intervallo per questo valore è maggiore o uguale a 0,0 f. Poiché il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**
</dt> <dd>

Valore float che controlla l'attenuazione delle dimensioni basate sulla distanza per le primitive di punti. Attivo solo quando D3DRS \_ POINTSCALEENABLE è **true**. Il valore predefinito è 0,0 f. L'intervallo per questo valore è maggiore o uguale a 0,0 f. Poiché il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**\_MULTISAMPLEANTIALIAS D3DRS**
</dt> <dd>

valore bool che determina il modo in cui vengono calcolati i singoli campioni quando si usa un buffer di destinazione di rendering multicampionamento. Se è impostato su **true**, vengono calcolati i diversi esempi in modo che l'anti-aliasing delle scene complete venga eseguito tramite il campionamento in posizioni di campionamento diverse per ogni campione multiplo. Se è impostato su **false**, gli esempi multipli vengono scritti con lo stesso valore di esempio, campionati in corrispondenza del pixel Center, che consente il rendering senza alias in un buffer multicampione. Questo stato di rendering non ha alcun effetto durante il rendering in un singolo buffer di esempio. Il valore predefinito è **true**.

</dd> <dt>

<span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**\_MULTISAMPLEMASK D3DRS**
</dt> <dd>

Ogni bit in questa maschera, iniziando dal bit meno significativo (LSB), controlla la modifica di uno degli esempi in una destinazione di rendering multicampionamento. Pertanto, per una destinazione di rendering di 8 campioni, il byte minimo contiene le otto abilitazioni di scrittura per ognuno degli otto esempi. Questo stato di rendering non ha alcun effetto durante il rendering in un singolo buffer di esempio. Il valore predefinito è 0xFFFFFFFF.

Questo stato di rendering consente l'uso di un buffer multisample come buffer di accumulo, eseguendo il rendering multipass della geometria in cui ogni passaggio Aggiorna un subset di esempi.

Se sono presenti n campioni multisamples e k Enabled, l'intensità risultante dell'immagine di cui è stato eseguito il rendering dovrebbe essere k/n. Ogni componente RGB di ogni pixel è fattorizzato da k/n.

</dd> <dt>

<span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**\_PATCHEDGESTYLE D3DRS**
</dt> <dd>

Imposta se i bordi della patch utilizzeranno lo schema a mosaico di tipo float. I valori possibili sono definiti dal tipo enumerato [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) . Il valore predefinito è D3DPATCHEDGE \_ discrete.

</dd> <dt>

<span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**\_DEBUGMONITORTOKEN D3DRS**
</dt> <dd>

Impostare solo per il debug del monitoraggio. I valori possibili sono definiti dal tipo enumerato [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) . Si noti che se \_ è impostato D3DRS DEBUGMONITORTOKEN, la chiamata viene considerata come passaggio di un token al monitor di debug. Ad esempio, se-dopo il passaggio di D3DDMT \_ Enable o D3DDMT \_ Disable a D3DRS \_ DEBUGMONITORTOKEN. gli altri valori di token vengono passati, lo stato (abilitato o disabilitato) del monitoraggio del debug continuerà a essere persistente.

Questo stato è utile solo per le compilazioni di debug. Per impostazione predefinita, il monitoraggio del debug viene abilitato per D3DDMT \_ .

</dd> <dt>

<span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ POINTSIZE \_ Max**
</dt> <dd>

Valore float che specifica la dimensione massima a cui verranno bloccati gli sprite del punto. Il valore deve essere minore o uguale al membro MaxPointSize di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) e maggiore o uguale a D3DRS \_ POINTSIZE \_ min. Il valore predefinito è 64,0. Poiché il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**\_INDEXEDVERTEXBLENDENABLE D3DRS**
</dt> <dd>

valore bool che Abilita o Disabilita la fusione di vertici indicizzati. Il valore predefinito è **false**. Se impostato su **true**, la fusione di vertici indicizzati è abilitata. Se impostato su **false**, la fusione di vertici indicizzati è disabilitata. Se questo stato di rendering è abilitato, l'utente deve passare gli indici di matrice come DWORDwith compresso ogni vertice. Quando lo stato di rendering è disabilitato e la fusione dei vertici viene abilitata tramite lo \_ stato VERTEXBLEND di D3DRS, equivale a avere gli indici di matrice 0, 1, 2, 3 in ogni vertice.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**\_COLORWRITEENABLE D3DRS**
</dt> <dd>

Valore UINT che consente la scrittura per canale per il buffer dei colori della destinazione di rendering. Un bit impostato comporta l'aggiornamento del canale colori durante il rendering 3D. Un bit chiaro restituisce il canale di colore ininteressato. Questa funzionalità è disponibile se il \_ bit D3DPMISCCAPS COLORWRITEENABLE capabilities è impostato nel membro PrimitiveMiscCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo. Questo stato di rendering non influisce sull'operazione di cancellazione. Il valore predefinito è 0x0000000F.

I valori validi per questo stato di rendering possono essere qualsiasi combinazione dei \_ flag D3DCOLORWRITEENABLE alfa, D3DCOLORWRITEENABLE \_ blu, D3DCOLORWRITEENABLE \_ verde o D3DCOLORWRITEENABLE \_ .

</dd> <dt>

<span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**\_TWEENFACTOR D3DRS**
</dt> <dd>

Valore float che controlla il fattore di interpolazione. Il valore predefinito è 0,0 f. Poiché il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**\_BLENDOP D3DRS**
</dt> <dd>

Valore utilizzato per selezionare l'operazione aritmetica applicata quando lo stato di rendering della fusione alfa, D3DRS \_ ALPHABLENDENABLE, è impostato su **true**. I valori validi sono definiti dal tipo enumerato [**D3DBLENDOP**](./d3dblendop.md) . Il valore predefinito è D3DBLENDOP \_ Add.

Se la \_ funzionalità del dispositivo BLENDOP di D3DPMISCCAPS non è supportata, \_ viene eseguito D3DBLENDOP Add.

</dd> <dt>

<span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**\_POSITIONDEGREE D3DRS**
</dt> <dd>

N: grado di interpolazione posizione patch. I valori possono essere D3DDEGREE \_ cubici (impostazione predefinita) o D3DDEGREE \_ lineari. Per ulteriori informazioni, vedere [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**\_NORMALDEGREE D3DRS**
</dt> <dd>

N-patch del livello di interpolazione normale. I valori possono essere D3DDEGREE \_ lineari (impostazione predefinita) o D3DDEGREE \_ quadratici. Per ulteriori informazioni, vedere [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**\_SCISSORTESTENABLE D3DRS**
</dt> <dd>

**True** per abilitare il test di Scissor e **false** per disabilitarlo. Il valore predefinito è **false**.

</dd> <dt>

<span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**\_SLOPESCALEDEPTHBIAS D3DRS**
</dt> <dd>

Usato per determinare la distorsione che può essere applicata alle primitive coplanari per ridurre il combattimento z. Il valore predefinito è 0.

Bias = (Max \* D3DRS \_ SLOPESCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.

dove Max è la pendenza massima della profondità del triangolo sottoposto a rendering.

</dd> <dt>

<span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**\_ANTIALIASEDLINEENABLE D3DRS**
</dt> <dd>

**True** per abilitare l'anti-aliasing della riga, **false** per disabilitare l'anti-aliasing della riga. Il valore predefinito è **false**.

Quando si esegue il rendering in una destinazione di rendering multisample, D3DRS \_ ANTIALIASEDLINEENABLE viene ignorato e viene eseguito il rendering di tutte le righe con alias. Usare [**ID3DXLine**](id3dxline.md) per il rendering di una riga con alias in una destinazione di rendering multicampionamento.

</dd> <dt>

<span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**\_MINTESSELLATIONLEVEL D3DRS**
</dt> <dd>

Livello minimo a mosaico. Il valore predefinito è 1.0 f. Vedere [mosaico (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**\_MAXTESSELLATIONLEVEL D3DRS**
</dt> <dd>

Livello massimo a mosaico. Il valore predefinito è 1.0 f. Vedere [mosaico (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**
</dt> <dd>

Valore di in modo adattivo conteggiarla suddividerla, nella direzione x. Il valore predefinito è 0,0 f. Vedere [schema a mosaico adattivo](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**
</dt> <dd>

Valore di in modo adattivo conteggiarla suddividerla nella direzione y. Il valore predefinito è 0,0 f. Vedere [schema a \_ mosaico adattivo](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**
</dt> <dd>

Valore di in modo adattivo conteggiarla suddividerla, nella direzione z. Il valore predefinito è 1.0 f. Vedere [schema a \_ mosaico adattivo](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**
</dt> <dd>

Valore di in modo adattivo conteggiarla suddividerla, nella direzione w. Il valore predefinito è 0,0 f. Vedere [schema a \_ mosaico adattivo](tessellation.md).

</dd> <dt>

<span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**\_ENABLEADAPTIVETESSELLATION D3DRS**
</dt> <dd>

**True** per abilitare lo schema a mosaico adattivo, **false** per disabilitarlo. Il valore predefinito è **false**. Vedere [schema a \_ mosaico adattivo](tessellation.md).

</dd> <dt>

<span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**\_TWOSIDEDSTENCILMODE D3DRS**
</dt> <dd>

**True** Abilita lo stencil a due lati, **false** lo Disabilita. Il valore predefinito è **false**. Per \_ \_ abilitare la modalità stencil bilaterale, l'applicazione deve impostare D3DRS CULLMODE su D3DCULL None. Se l'ordine di avvolgimento del triangolo è in senso orario, \_ verranno usate le operazioni dello stencil D3DRS \* . Se l'ordine di avvolgimento è in senso antiorario, \_ \_ verranno usate le operazioni dello stencil D3DRS CCW \* .

Per verificare se lo stencil a due lati è supportato, controllare il membro StencilCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per D3DSTENCILCAPS \_ TWOSIDED. Vedere anche [D3DSTENCILCAPS](d3dstencilcaps.md).

</dd> <dt>

<span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCILFAIL**
</dt> <dd>

Operazione dello stencil da eseguire se il test di stencil CCW non riesce. I valori sono dal tipo enumerato [**D3DSTENCILOP**](./d3dstencilop.md) . Il valore predefinito è D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**
</dt> <dd>

Operazione dello stencil da eseguire se il test di stencil CCW supera e z-test ha esito negativo. I valori sono dal tipo enumerato [**D3DSTENCILOP**](./d3dstencilop.md) . Il valore predefinito è D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**
</dt> <dd>

Operazione dello stencil da eseguire se vengono superati sia lo stencil CCW che i test z. I valori sono dal tipo enumerato [**D3DSTENCILOP**](./d3dstencilop.md) . Il valore predefinito è D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**
</dt> <dd>

Funzione di confronto. Il test di stencil CCW passa se la funzione (((Ref & mask) dello stencil (stencil & mask)) è **true**. I valori sono dal tipo enumerato [**D3DCMPFUNC**](./d3dcmpfunc.md) . Il valore predefinito è D3DCMP \_ Always.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**\_COLORWRITEENABLE1 D3DRS**
</dt> <dd>

Valori ColorWriteEnable aggiuntivi per i dispositivi. Vedere D3DRS \_ COLORWRITEENABLE. Questa funzionalità è disponibile se il \_ bit D3DPMISCCAPS INDEPENDENTWRITEMASKS capabilities è impostato nel membro PrimitiveMiscCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo. Il valore predefinito è 0x0000000F.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**\_COLORWRITEENABLE2 D3DRS**
</dt> <dd>

Valori ColorWriteEnable aggiuntivi per i dispositivi. Vedere D3DRS \_ COLORWRITEENABLE. Questa funzionalità è disponibile se il \_ bit D3DPMISCCAPS INDEPENDENTWRITEMASKS capabilities è impostato nel membro PrimitiveMiscCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo. Il valore predefinito è 0x0000000F.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**\_COLORWRITEENABLE3 D3DRS**
</dt> <dd>

Valori ColorWriteEnable aggiuntivi per i dispositivi. Vedere D3DRS \_ COLORWRITEENABLE. Questa funzionalità è disponibile se il \_ bit D3DPMISCCAPS INDEPENDENTWRITEMASKS capabilities è impostato nel membro PrimitiveMiscCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo. Il valore predefinito è 0x0000000F.

</dd> <dt>

<span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**\_BLENDFACTOR D3DRS**
</dt> <dd>

[**D3DCOLOR**](d3dcolor.md) usato per un fattore di Blend costante durante la fusione alfa. Questa funzionalità è disponibile se il \_ bit D3DPBLENDCAPS BLENDFACTOR capabilities è impostato nel membro SrcBlendCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) o nel membro DestBlendCaps di **D3DCAPS9**. Vedere [**D3DRENDERSTATETYPE**](). Il valore predefinito è 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**\_SRGBWRITEENABLE D3DRS**
</dt> <dd>

Abilitare le scritture di destinazione rendering come gamma con correzione a sRGB. Il formato deve esporre D3DUSAGE \_ SRGBWRITE. Il valore predefinito è 0.

</dd> <dt>

<span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**\_DEPTHBIAS D3DRS**
</dt> <dd>

Valore a virgola mobile utilizzato per il confronto dei valori di profondità. Vedere [Bias Depth (Direct3D 9)](depth-bias.md). Il valore predefinito è 0.

</dd> <dt>

<span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**\_WRAP8 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**\_WRAP9 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**\_WRAP10 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**\_WRAP11 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**\_WRAP12 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**\_WRAP13 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**\_WRAP14 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**\_WRAP15 D3DRS**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**\_SEPARATEALPHABLENDENABLE D3DRS**
</dt> <dd>

**True** Abilita la modalità di Blend separata per il canale alfa. Il valore predefinito è **false**.

Se è impostato su **false**, i fattori e le operazioni di combinazione di destinazione di rendering applicati a alfa sono obbligati a essere uguali a quelli definiti per il colore. Questa modalità è effettivamente cablata su **false** nelle implementazioni che non impostano il CAP D3DPMISCCAPS \_ SEPARATEALPHABLEND. Vedere [D3DPMISCCAPS](d3dpmisccaps.md).

Il tipo di fusione alfa separata è determinato dagli \_ Stati di rendering D3DRS SRCBLENDALPHA e \_ D3DRS DESTBLENDALPHA.

</dd> <dt>

<span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**\_SRCBLENDALPHA D3DRS**
</dt> <dd>

Un membro del tipo enumerato [**D3DBLEND**](./d3dblend.md) . Questo valore viene ignorato a meno che D3DRS \_ SEPARATEALPHABLENDENABLE non sia **true**. Il valore predefinito è D3DBLEND \_ One.

</dd> <dt>

<span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**\_DESTBLENDALPHA D3DRS**
</dt> <dd>

Un membro del tipo enumerato [**D3DBLEND**](./d3dblend.md) . Questo valore viene ignorato a meno che D3DRS \_ SEPARATEALPHABLENDENABLE non sia **true**. Il valore predefinito è D3DBLEND \_ zero.

</dd> <dt>

<span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**\_BLENDOPALPHA D3DRS**
</dt> <dd>

Valore usato per selezionare l'operazione aritmetica applicata per separare la fusione alfa quando lo stato di rendering, D3DRS \_ SEPARATEALPHABLENDENABLE, è impostato su **true**.

I valori validi sono definiti dal tipo enumerato [**D3DBLENDOP**](./d3dblendop.md) . Il valore predefinito è D3DBLENDOP \_ Add.

Se la \_ funzionalità del dispositivo BLENDOP di D3DPMISCCAPS non è supportata, \_ viene eseguito D3DBLENDOP Add. Vedere [D3DPMISCCAPS](d3dpmisccaps.md).

</dd> <dt>

<span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti



| Stati di rendering        |                    |
|----------------------|--------------------|
| \_da PS 1 \_ 1 a PS \_ 1 \_ 3 | 4 campionatori trama |



 

Direct3D definisce la \_ costante D3DRENDERSTATE WRAPBIAS come comoda per le applicazioni per abilitare o disabilitare il wrapping della trama, in base al numero intero in base zero di un set di coordinate di trama, anziché usare in modo esplicito uno dei \_ valori di stato di incapsulamento n di D3DRS. Aggiungere il \_ valore D3DRENDERSTATE WRAPBIAS all'indice in base zero di un set di coordinate di trama per calcolare il \_ valore di D3DRS wrap n corrispondente a tale indice, come illustrato nell'esempio seguente.


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: GetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
