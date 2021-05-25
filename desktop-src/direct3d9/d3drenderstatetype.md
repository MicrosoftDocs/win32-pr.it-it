---
description: Gli stati di rendering definiscono gli stati di configurazione per tutti i tipi di elaborazione di vertici e pixel.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Enumerazione D3DRENDERSTATETYPE (D3D9Types.h)
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
ms.openlocfilehash: 0a7ad803535032705e6e1bb5456109486c59d190
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343066"
---
# <a name="d3drenderstatetype-enumeration"></a>Enumerazione D3DRENDERSTATETYPE

Gli stati di rendering definiscono gli stati di configurazione per tutti i tipi di elaborazione di vertici e pixel. Alcuni stati di rendering configurano l'elaborazione dei vertici e altri configurano l'elaborazione dei pixel (vedere Stati di rendering [(Direct3D 9)](render-states.md)). Gli stati di rendering possono essere salvati e ripristinati usando blocchi di stato (vedere [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).

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

<span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**
</dt> <dd>

Stato di buffering di profondità come membro del [**tipo enumerato D3DZBUFFERTYPE.**](./d3dzbuffertype.md) Impostare questo stato su D3DZB TRUE per abilitare il \_ buffering z, D3DZB USEW per abilitare \_ il w-buffering o D3DZB FALSE per disabilitare il buffering di \_ profondità.

Il valore predefinito per questo stato di rendering è D3DZB TRUE se è stato creato un depth stencil insieme alla catena di scambio impostando il membro \_ EnableAutoDepthStencil della struttura [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md) su **TRUE** e D3DZB FALSE in caso \_ contrario.

</dd> <dt>

<span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FILLMODE**
</dt> <dd>

Uno o più membri del [**tipo enumerato D3DFILLMODE.**](./d3dfillmode.md) Il valore predefinito è D3DFILL \_ SOLID.

</dd> <dt>

<span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**
</dt> <dd>

Uno o più membri del [**tipo enumerato D3DSHADEMODE.**](./d3dshademode.md) Il valore predefinito è D3DSHADE \_ GOURAUD.

</dd> <dt>

<span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**
</dt> <dd>

**TRUE** per consentire all'applicazione di scrivere nel buffer di profondità. Il valore predefinito è **TRUE.** Questo membro consente a un'applicazione di impedire al sistema di aggiornare il buffer di profondità con nuovi valori di profondità. Se **FALSE,** i confronti di profondità vengono comunque eseguono in base allo stato di rendering D3DRS ZFUNC, presupponendo che sia in corso il buffering della profondità, ma i valori di profondità non vengono scritti \_ nel buffer.

</dd> <dt>

<span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**
</dt> <dd>

**TRUE per** abilitare il test alfa per pixel. Se il test viene superato, il pixel viene elaborato dal buffer dei frame. In caso contrario, tutta l'elaborazione del buffer dei frame viene ignorata per il pixel.

Il test viene eseguito confrontando il valore alfa in ingresso con il valore alfa di riferimento, usando la funzione di confronto fornita dallo stato di rendering D3DRS \_ ALPHAFUNC. Il valore alfa di riferimento è determinato dal valore impostato per D3DRS \_ ALPHAREF. Per altre informazioni, vedere [Alpha Testing State (Direct3D 9) (Stato di test alfa - Direct3D 9).](alpha-testing-state.md)

Il valore predefinito di questo parametro è **FALSE.**

</dd> <dt>

<span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**
</dt> <dd>

Il valore predefinito è **TRUE,** che consente di disegnare l'ultimo pixel di una linea. Per impedire il disegno dell'ultimo pixel, impostare questo valore su **FALSE.** Per altre informazioni, vedere [Stato contorno e riempimento (Direct3D 9).](outline-and-fill-state.md)

</dd> <dt>

<span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**
</dt> <dd>

Membro del tipo [**enumerato D3DBLEND.**](./d3dblend.md) Il valore predefinito è D3DBLEND \_ ONE.

</dd> <dt>

<span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**
</dt> <dd>

Membro del tipo [**enumerato D3DBLEND.**](./d3dblend.md) Il valore predefinito è D3DBLEND \_ ZERO.

</dd> <dt>

<span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**
</dt> <dd>

Specifica come vengono espulsi i triangoli rivolti verso il retro, se non del tutto. Può essere impostato su un membro del [**tipo enumerato D3DCULL.**](./d3dcull.md) Il valore predefinito è D3DCULL \_ CCW.

</dd> <dt>

<span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ ZFUNC**
</dt> <dd>

Membro del tipo [**enumerato D3DCMPFUNC.**](./d3dcmpfunc.md) Il valore predefinito è D3DCMP \_ LESSEQUAL. Questo membro consente a un'applicazione di accettare o rifiutare un pixel, in base alla distanza dalla fotocamera.

Il valore di profondità del pixel viene confrontato con il valore depth-buffer. Se il valore di profondità del pixel supera la funzione di confronto, viene scritto il pixel.

Il valore di profondità viene scritto nel buffer di profondità solo se lo stato di rendering è **TRUE.**

I rasterizzatori software e molti acceleratori hardware funzionano più velocemente se il test di profondità ha esito negativo, perché non è necessario filtrare e modulare la trama se il pixel non verrà sottoposto a rendering.

</dd> <dt>

<span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**
</dt> <dd>

Valore che specifica un valore alfa di riferimento rispetto al quale vengono testati i pixel quando è abilitato il test alfa. Si tratta di un valore a 8 bit inserito negli 8 bit bassi del valore dello stato di rendering DWORD. I valori possono variare da 0x00000000 a 0x000000FF. Il valore predefinito è 0.

</dd> <dt>

<span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**
</dt> <dd>

Membro del tipo [**enumerato D3DCMPFUNC.**](./d3dcmpfunc.md) Il valore predefinito è D3DCMP \_ ALWAYS. Questo membro consente a un'applicazione di accettare o rifiutare un pixel, in base al relativo valore alfa.

</dd> <dt>

<span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**
</dt> <dd>

**TRUE** per abilitare il dithering. Il valore predefinito è **FALSE.**

</dd> <dt>

<span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**
</dt> <dd>

**TRUE** per abilitare la trasparenza con alpha blended. Il valore predefinito è **FALSE.**

Il tipo di fusione alfa è determinato dagli stati di rendering D3DRS \_ SRCBLEND e D3DRS \_ DESTBLEND.

</dd> <dt>

<span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ FOGENABLE**
</dt> <dd>

**TRUE per** abilitare la fusione. Il valore predefinito è **FALSE.** Per altre informazioni sull'uso della fusione blending, vedere [La combinazione di sfumature.](fog.md)

</dd> <dt>

<span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**
</dt> <dd>

**TRUE per** abilitare le evidenziazioni speculari. Il valore predefinito è **FALSE.**

Le evidenziazioni speculari vengono calcolate come se ogni vertice nell'oggetto acceso fosse all'origine dell'oggetto. In questo modo vengono restituiti i risultati previsti, purché l'oggetto sia modellato intorno all'origine e la distanza dalla luce all'oggetto sia relativamente grande. In altri casi, i risultati sono indefiniti.

Quando questo membro è impostato su **TRUE,** il colore speculare viene aggiunto al colore di base dopo la propagazione della trama ma prima della fusione alfa.

</dd> <dt>

<span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRSCOLOR \_**
</dt> <dd>

Valore il cui tipo è [**D3DCOLOR.**](d3dcolor.md) Il valore predefinito è 0. Per altre informazioni sul colore dei colori, vedere [Color Color (Direct3D 9)](fog-color.md).

</dd> <dt>

<span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ OSANNATABLEMODE**
</dt> <dd>

Formula della nebbia da usare per la nebbia in pixel. Impostare su uno dei membri del [**tipo enumerato D3DFOGMODE.**](./d3dfogmode.md) Il valore predefinito è D3DFOG \_ NONE. Per altre informazioni sulla nebbia dei pixel, vedere [Pixel Fog (Direct3D 9)](pixel-fog.md).

</dd> <dt>

<span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ FOGSTART**
</dt> <dd>

Profondità alla quale iniziano gli effetti della sfumatura di pixel o vertici per la modalità nebbia lineare. Il valore predefinito è 0,0f. La profondità viene specificata nello spazio mondo per la nebbia dei vertici e nello spazio del dispositivo \[ 0.0, 1.0 o nello spazio mondo per la nebbia \] dei pixel. Per la nebbia dei pixel, questi valori si verificano nello spazio del dispositivo quando il sistema usa z per i calcoli della nebbia e lo spazio mondiale quando il sistema usa la nebbia relativa agli occhi (w-nebbia). Per altre informazioni, vedere [Parametri di nebbia (Direct3D 9)](fog-parameters.md) e Profondità relativa agli occhi rispetto [a Z.](pixel-fog.md)

I valori per questo stato di rendering sono valori a virgola mobile. Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ OSANNA**
</dt> <dd>

Profondità alla quale terminano gli effetti di sfumatura di pixel o vertici per la modalità nebbia lineare. Il valore predefinito è 1,0f. La profondità viene specificata nello spazio mondo per la nebbia dei vertici e nello spazio del dispositivo \[ 0.0, 1.0 o nello spazio mondo per la nebbia \] dei pixel. Per la nebbia dei pixel, questi valori si verificano nello spazio del dispositivo quando il sistema usa z per i calcoli della nebbia e nello spazio mondiale quando il sistema usa la nebbia relativa agli occhi (w-nebbia). Per altre informazioni, vedere [Parametri di nebbia (Direct3D 9)](fog-parameters.md) e Profondità relativa agli occhi rispetto [a Z.](pixel-fog.md)

I valori per questo stato di rendering sono valori a virgola mobile. Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**\_D3DRSDENSITY**
</dt> <dd>

Densità di densità di pixel o vertice usata nelle modalità esponenziali di exp (D3DFOG \_ EXP e D3DFOG \_ EXP2). I valori di densità validi sono da 0,0 a 1,0. Il valore predefinito è 1,0. Per altre informazioni, vedere [Parameters (Direct3D 9) .](fog-parameters.md)

I valori per questo stato di rendering sono valori a virgola mobile. Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**
</dt> <dd>

**TRUE per** abilitare il vertice basato su intervalli. Il valore predefinito è **FALSE,** nel qual caso il sistema usa un oggetto basato sulla profondità. Nel caso di un oggetto basato su intervalli, la distanza di un oggetto dal visualizzatore viene usata per calcolare gli effetti dell'effetto, non la profondità dell'oggetto (ovvero la coordinata z) nella scena. Nel caso di un'applicazione basata su intervalli, tutti i metodi dell'intervallo funzionano come di consueto, ad eccezione del fatto che usano l'intervallo anziché la profondità nei calcoli.

L'intervallo è il fattore corretto da usare per i calcoli dei tempi di calcolo, ma la profondità viene in genere usata perché l'intervallo richiede molto tempo e la profondità è in genere già disponibile. L'uso della profondità per calcolare il visore ha l'effetto indesiderato di modificare l'intensità degli oggetti periferici quando l'occhio del visualizzatore si sposta. In questo caso, la profondità cambia e l'intervallo rimane costante.

Poiché attualmente nessun hardware supporta l'intervallo basato su intervalli per pixel, la correzione dell'intervallo è disponibile solo per vertexrere.

Per altre informazioni, vedere [VertexBie (Direct3D 9)](vertex-fog.md).

</dd> <dt>

<span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**STENCIL \_ D3DRSABILITA**
</dt> <dd>

**TRUE** per abilitare lo stencil o **FALSE per** disabilitare lo stencil. Il valore predefinito è **FALSE.** Per altre informazioni, vedere [Stencil Buffer Techniques (Direct3D 9) (Tecniche del buffer degli stencil ( Direct3D 9)](stencil-buffer-techniques.md)).

</dd> <dt>

<span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**
</dt> <dd>

Operazione di stencil da eseguire se il test di stencil ha esito negativo. I valori derivano [**dal tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md) Il valore predefinito è D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**
</dt> <dd>

Operazione di stencil da eseguire se il test di stencil supera e il test di profondità (z-test) ha esito negativo. I valori sono del [**tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md) Il valore predefinito è D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**
</dt> <dd>

Operazione di stencil da eseguire se vengono superati sia lo stencil che i test di profondità (z). I valori sono del [**tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md) Il valore predefinito è D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**
</dt> <dd>

Funzione di confronto per il test di stencil. I valori sono del [**tipo enumerato D3DCMPFUNC.**](./d3dcmpfunc.md) Il valore predefinito è D3DCMP \_ ALWAYS.

La funzione di confronto viene usata per confrontare il valore di riferimento con una voce del buffer di stencil. Questo confronto si applica solo ai bit nel valore di riferimento e nella voce del buffer di stencil impostati nella maschera di stencil (impostata dallo stato di rendering D3DRS \_ STENCILMASK). Se **TRUE,** il test dello stencil viene superato.

</dd> <dt>

<span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**
</dt> <dd>

Valore di riferimento int per il test dello stencil. Il valore predefinito è 0.

</dd> <dt>

<span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**
</dt> <dd>

Maschera applicata al valore di riferimento e a ogni voce del buffer degli stencil per determinare i bit significativi per il test dello stencil. La maschera predefinita è 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**STENCIL \_ D3DRSWRITEMASK**
</dt> <dd>

Maschera di scrittura applicata ai valori scritti nel buffer degli stencil. La maschera predefinita è 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**
</dt> <dd>

Colore usato per la fusione di più trame con l'argomento di fusione della trama D3DTA TFACTOR o l'operazione di fusione della trama \_ D3DTOP \_ BLENDFACTORALPHA. Il valore associato è una [**variabile D3DCOLOR.**](d3dcolor.md) Il valore predefinito è bianco opaco (0xFFFFFFFF).

</dd> <dt>

<span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**
</dt> <dd>

Comportamento di wrapping della trama per più set di coordinate di trama. I valori validi per questo stato di rendering possono essere qualsiasi combinazione dei flag \_ D3DWRAPCOORD 0 (o D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (o D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (o D3DWRAP W) e \_ D3DWRAPCOORD \_ 3. In questo modo il sistema esegue il wrapping nella direzione della prima, seconda, terza e quarta dimensione, a volte definita come direzioni s, t, r e q, per una determinata trama. Il valore predefinito per questo stato di rendering è 0 (il ritorno a capo è disabilitato in tutte le direzioni).

</dd> <dt>

<span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**WRAP D3DRS3 \_**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**WRAP D3DRS5 \_**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**WRAP D3DRS6 \_**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**WRAP D3DRS7 \_**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**RITAGLIO \_ D3DRS**
</dt> <dd>

**TRUE** per abilitare il ritaglio primitivo da Direct3D o **FALSE** per disabilitarlo. Il valore predefinito è **TRUE.**

</dd> <dt>

<span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**ILLUMINAZIONE \_ D3DRS**
</dt> <dd>

**TRUE** per abilitare l'illuminazione Direct3D o **FALSE** per disabilitarla. Il valore predefinito è **TRUE.** Vengono accesi correttamente solo i vertici che includono una normale vertice. I vertici che non contengono un normale utilizzano un prodotto punto 0 in tutti i calcoli di illuminazione.

</dd> <dt>

<span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**AMBIENTE D3DRS \_**
</dt> <dd>

Colore della luce ambientale. Questo valore è di tipo [**D3DCOLOR**](d3dcolor.md). Il valore predefinito è 0.

</dd> <dt>

<span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ EVERTEXMODE**
</dt> <dd>

Formula del vertice da usare per il vertice. Impostare su un membro del [**tipo enumerato D3DFOGMODE.**](./d3dfogmode.md) Il valore predefinito è D3DFOG \_ NONE.

</dd> <dt>

<span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**
</dt> <dd>

**TRUE** per abilitare il colore per vertice o **FALSE** per disabilitarlo. Il valore predefinito è **TRUE.** L'abilitazione del colore per vertice consente al sistema di includere il colore definito per i singoli vertici nei calcoli di illuminazione.

Per altre informazioni, vedere gli stati di rendering seguenti:

-   D3DRS \_ DIFFUSEMATERIALSOURCE
-   D3DRS \_ SPECULARMATERIALSOURCE
-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS \_ EMISSIVEMATERIALSOURCE

</dd> <dt>

<span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**
</dt> <dd>

**TRUE** per abilitare le evidenziazioni speculari relative alla fotocamera o **FALSE per** usare le evidenziazioni speculari ortogonali. Il valore predefinito è **TRUE.** Le applicazioni che usano la proiezione ortogonale devono specificare **FALSE.**

</dd> <dt>

<span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**
</dt> <dd>

**TRUE** per abilitare la normalizzazione automatica delle normali dei vertici o **FALSE** per disabilitarla. Il valore predefinito è **FALSE.** Se si abilita questa funzionalità, il sistema normalizza le normali vertici per i vertici dopo averli trasformati nello spazio della fotocamera, operazione che può richiedere molto tempo a livello di calcolo.

</dd> <dt>

<span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**
</dt> <dd>

Origine colore diffusa per i calcoli dell'illuminazione. I valori validi sono membri del [**tipo enumerato D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md) Il valore predefinito è D3DMCS \_ COLOR1. Il valore per questo stato di rendering viene usato solo se lo stato di rendering D3DRS \_ COLORVERTEX è impostato su **TRUE.**

</dd> <dt>

<span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**
</dt> <dd>

Origine di colore speculare per i calcoli di illuminazione. I valori validi sono membri del [**tipo enumerato D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md) Il valore predefinito è D3DMCS \_ COLOR2.

</dd> <dt>

<span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**
</dt> <dd>

Origine dei colori di ambiente per i calcoli di illuminazione. I valori validi sono membri del [**tipo enumerato D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md) Il valore predefinito è D3DMCS \_ MATERIAL.

</dd> <dt>

<span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**
</dt> <dd>

Origine del colore emissiva per i calcoli di illuminazione. I valori validi sono membri del [**tipo enumerato D3DMATERIALCOLORSOURCE.**](./d3dmaterialcolorsource.md) Il valore predefinito è D3DMCS \_ MATERIAL.

</dd> <dt>

<span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**
</dt> <dd>

Numero di matrici da usare per eseguire la fusione geometrica, se presente. I valori validi sono membri del [**tipo enumerato D3DVERTEXBLENDFLAGS.**](./d3dvertexblendflags.md) Il valore predefinito è D3DVBF \_ DISABLE.

</dd> <dt>

<span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**
</dt> <dd>

Abilita o disabilita i piani di ritaglio definiti dall'utente. I valori validi sono qualsiasi DWORD in cui lo stato di ogni bit (impostato o non impostato) attiva o disattiva lo stato di attivazione di un piano di ritaglio corrispondente definito dall'utente. Il bit meno significativo (bit 0) controlla il primo piano di ritaglio in corrispondenza dell'indice 0 e i bit successivi controllano l'attivazione dei piani di ritaglio in corrispondenza degli indici superiori. Se è impostato un bit, il sistema applica il piano di ritaglio appropriato durante il rendering della scena. Il valore predefinito è 0.

Le macro [**D3DCLIPPLANEn**](d3dclipplanen.md) sono definite per offrire un modo pratico per abilitare i piani di ritaglio.

</dd> <dt>

<span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ POINTSIZE**
</dt> <dd>

Valore float che specifica le dimensioni da usare per il calcolo delle dimensioni dei punti nei casi in cui la dimensione del punto non è specificata per ogni vertice. Questo valore non viene usato quando il vertice contiene dimensioni in punti. Questo valore è in unità di spazio dello schermo se D3DRS \_ POINTSCALEENABLE è **FALSE;** in caso contrario, questo valore è in unità di spazio del mondo. Il valore predefinito è il valore restituito da un driver. Se un driver restituisce 0 o 1, il valore predefinito è 64, che consente l'emulazione delle dimensioni dei punti software. Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ POINTSIZE \_ MIN**
</dt> <dd>

Valore float che specifica la dimensione minima delle primitive di punti. Le primitive punto vengono imposte su queste dimensioni durante il rendering. L'impostazione di questa proprietà su valori inferiori a 1,0 comporta l'eliminazione dei punti quando il punto non copre un centro pixel e l'antialiasing viene disabilitato o sottoposto a rendering con intensità ridotta quando è abilitato l'anti-aliasing. Il valore predefinito è 1,0f. L'intervallo per questo valore è maggiore o uguale a 0,0f. Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**PUNTI \_ D3DRSPRITEENABLE**
</dt> <dd>

valore bool. Se **TRUE,** le coordinate di trama delle primitive di punto vengono impostate in modo che le trame complete siano mappate su ogni punto. Quando **FALSE,** le coordinate della trama dei vertici vengono usate per l'intero punto. Il valore predefinito è **FALSE.** È possibile ottenere punti a pixel singolo in stile DirectX 7 impostando D3DRS \_ POINTSCALEENABLE su **FALSE** e D3DRS \_ POINTSIZE su 1.0, che sono i valori predefiniti.

</dd> <dt>

<span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**
</dt> <dd>

Valore bool che controlla il calcolo delle dimensioni per le primitive di punti. Quando **TRUE,** le dimensioni del punto vengono interpretate come un valore dello spazio della fotocamera e vengono ridimensionate dalla funzione distance e dal ridimensionamento dell'asse y del viewport al viewport per calcolare le dimensioni finali del punto dello spazio dello schermo. Quando **FALSE,** le dimensioni in punti vengono interpretate come spazio sullo schermo e usate direttamente. Il valore predefinito è **FALSE.**

</dd> <dt>

<span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_ A**
</dt> <dd>

Valore float che controlla l'attenuazione delle dimensioni basata sulla distanza per le primitive di punto. Attivo solo quando D3DRS \_ POINTSCALEENABLE è **TRUE.** Il valore predefinito è 1,0f. L'intervallo per questo valore è maggiore o uguale a 0,0f. Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**
</dt> <dd>

Valore float che controlla l'attenuazione delle dimensioni in base alla distanza per le primitive punto. Attiva solo quando D3DRS \_ POINTSCALEENABLE è **TRUE.** Il valore predefinito è 0,0f. L'intervallo per questo valore è maggiore o uguale a 0,0f. Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**
</dt> <dd>

Valore float che controlla l'attenuazione delle dimensioni in base alla distanza per le primitive punto. Attiva solo quando D3DRS \_ POINTSCALEENABLE è **TRUE.** Il valore predefinito è 0,0f. L'intervallo per questo valore è maggiore o uguale a 0,0f. Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**
</dt> <dd>

Valore bool che determina il modo in cui vengono calcolati i singoli campioni quando si usa un buffer di destinazione di rendering multicampionamento. Se impostato su **TRUE,** vengono calcolati più campioni in modo che l'anti-aliasing della scena completa sia eseguito tramite il campionamento in posizioni di campionamento diverse per ogni campione multiplo. Se impostato su **FALSE,** tutti i campioni multipli vengono scritti con lo stesso valore di campione, campionato al centro del pixel, che consente il rendering non antialias in un buffer multicampionamento. Questo stato di rendering non ha alcun effetto quando si esegue il rendering in un singolo buffer di esempio. Il valore predefinito è **TRUE.**

</dd> <dt>

<span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**
</dt> <dd>

Ogni bit di questa maschera, a partire dal bit meno significativo (LSB), controlla la modifica di uno degli esempi in una destinazione di rendering multicampionamento. Pertanto, per una destinazione di rendering di 8 campioni, il byte basso contiene le otto operazioni di scrittura abilitate per ognuno degli otto campioni. Questo stato di rendering non ha alcun effetto quando viene eseguito il rendering in un singolo buffer di esempio. Il valore predefinito è 0xFFFFFFFF.

Questo stato di rendering consente l'uso di un buffer multicampione come buffer di accumulo, eseguendo il rendering multipass della geometria in cui ogni passaggio aggiorna un subset di esempi.

Se sono presenti n campioni multicampionati e k abilitati, l'intensità risultante dell'immagine sottoposta a rendering deve essere k/n. Ogni componente RGB di ogni pixel viene fattoriato da k/n.

</dd> <dt>

<span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**
</dt> <dd>

Imposta un valore che indica se i bordi delle patch useranno la tessellazione in stile float. I valori possibili sono definiti dal [**tipo enumerato D3DPATCHEDGESTYLE.**](./d3dpatchedgestyle.md) Il valore predefinito è D3DPATCHEDGE \_ DISCRETE.

</dd> <dt>

<span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**
</dt> <dd>

Impostare solo per il debug del monitoraggio. I valori possibili sono definiti dal [**tipo enumerato D3DDEBUGMONITORTOKENS.**](./d3ddebugmonitortokens.md) Si noti che se d3DRS DEBUGMONITORTOKEN è impostato, la chiamata viene considerata come passaggio \_ di un token al monitoraggio di debug. Se, ad esempio, dopo aver passato D3DDMT ENABLE o \_ D3DDMT DISABLE a \_ D3DRS DEBUGMONITORTOKEN, vengono passati altri valori di token, lo stato (abilitato o disabilitato) del monitoraggio di debug continuerà a essere \_ persistente.

Questo stato è utile solo per le build di debug. Per impostazione predefinita, il monitoraggio del debug è D3DDMT \_ ENABLE.

</dd> <dt>

<span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ POINTSIZE \_ MAX**
</dt> <dd>

Valore float che specifica le dimensioni massime fino a cui verranno ancoraggio gli sprite di punti. Il valore deve essere minore o uguale al membro MaxPointSize di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) e maggiore o uguale a D3DRS \_ POINTSIZE \_ MIN. Il valore predefinito è 64.0. Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**
</dt> <dd>

Valore bool che abilita o disabilita la fusione dei vertici indicizzati. Il valore predefinito è **FALSE.** Se impostato su **TRUE,** la fusione dei vertici indicizzata è abilitata. Se impostata **su FALSE,** la fusione dei vertici indicizzata è disabilitata. Se questo stato di rendering è abilitato, l'utente deve passare gli indici di matrice come DWORD di tipo packedcon ogni vertice. Quando lo stato di rendering è disabilitato e la fusione dei vertici viene abilitata tramite lo stato VERTEXBLEND D3DRS, equivale a disporre di indici matrice \_ 0, 1, 2, 3 in ogni vertice.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**
</dt> <dd>

Valore UINT che abilita una scrittura per canale per il buffer dei colori di destinazione del rendering. Un bit impostato determina l'aggiornamento del canale colori durante il rendering 3D. Un bit chiaro fa in modo che il canale di colore non sia interessato. Questa funzionalità è disponibile se il bit di funzionalità D3DPMISCCAPS COLORWRITEENABLE è impostato nel membro \_ PrimitiveMiscCaps della [**struttura D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo. Questo stato di rendering non influisce sull'operazione di cancellazione. Il valore predefinito è 0x0000000F.

I valori validi per questo stato di rendering possono essere qualsiasi combinazione dei flag D3DCOLORWRITEENABLE \_ ALPHA, D3DCOLORWRITEENABLE \_ BLUE, D3DCOLORWRITEENABLE GREEN o \_ D3DCOLORWRITEENABLE \_ RED.

</dd> <dt>

<span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**
</dt> <dd>

Valore float che controlla il fattore di interpolazione. Il valore predefinito è 0,0f. Poiché il [**metodo IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta valori DWORD, l'applicazione deve eseguire il cast di una variabile che contiene il valore, come illustrato nell'esempio di codice seguente.


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**
</dt> <dd>

Valore utilizzato per selezionare l'operazione aritmetica applicata quando lo stato di rendering della fusione alfa, D3DRS \_ ALPHABLENDENABLE, è impostato su **TRUE.** I valori validi sono definiti dal [**tipo enumerato D3DBLENDOP.**](./d3dblendop.md) Il valore predefinito è D3DBLENDOP \_ ADD.

Se la funzionalità del dispositivo D3DPMISCCAPS BLENDOP non è supportata, viene eseguito \_ D3DBLENDOP \_ ADD.

</dd> <dt>

<span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**
</dt> <dd>

Grado di interpolazione posizione N-patch. I valori possono essere D3DDEGREE \_ CUBIC (impostazione predefinita) o D3DDEGREE \_ LINEAR. Per altre informazioni, vedere [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**
</dt> <dd>

Grado di interpolazione normale con patch a N. I valori possono essere D3DDEGREE \_ LINEAR (impostazione predefinita) o D3DDEGREE \_ QUADRATIC. Per altre informazioni, vedere [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**
</dt> <dd>

**TRUE** per abilitare il test della forbice e **FALSE** per disabilitarlo. Il valore predefinito è **FALSE.**

</dd> <dt>

<span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ SLOPESCALEDEPTHBIAS**
</dt> <dd>

Usato per determinare la quantità di distorsione che può essere applicata alle primitive co-planari per ridurre lo z-fighting. Il valore predefinito è 0.

bias = (max \* D3DRS \_ SLOPESCALEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.

dove max è l'inclinazione massima della profondità del triangolo sottoposto a rendering.

</dd> <dt>

<span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**
</dt> <dd>

**TRUE** per abilitare l'anti-aliasing delle righe, **FALSE per** disabilitare l'anti-aliasing di riga. Il valore predefinito è **FALSE.**

Quando si esegue il rendering in una destinazione di rendering multicampionamento, D3DRS ANTIALIASEDLINEENABLE viene ignorato e viene eseguito il rendering di tutte le \_ righe con alias. Usare [**ID3DXLine per**](id3dxline.md) il rendering di linee con antialias in una destinazione di rendering multicampionamento.

</dd> <dt>

<span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**
</dt> <dd>

Livello minimo a più livelli. Il valore predefinito è 1,0f. Vedere [Tessellation (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**
</dt> <dd>

Livello massimo a tessellazione. Il valore predefinito è 1,0f. Vedere [Tessellation (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**
</dt> <dd>

Quantità da a tessellare adattivamente, nella direzione x. Il valore predefinito è 0,0f. Vedere [a tessellazione adattiva.](tessellation.md)

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**
</dt> <dd>

Quantità da a tessellare adattivamente, nella direzione y. Il valore predefinito è 0,0f. Vedere [a \_ tessellazione adattiva.](tessellation.md)

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**
</dt> <dd>

Quantità da a tessellare adattivamente, nella direzione z. Il valore predefinito è 1,0f. Vedere [a \_ tessellazione adattiva.](tessellation.md)

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**
</dt> <dd>

Quantità da a tessellare in modo adattivo, nella direzione w. Il valore predefinito è 0,0f. Vedere [a \_ tessellazione adattiva.](tessellation.md)

</dd> <dt>

<span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**
</dt> <dd>

**TRUE** per abilitare la tessellazione adattiva, **FALSE** per disabilitarla. Il valore predefinito è **FALSE.** Vedere [a \_ tessellazione adattiva.](tessellation.md)

</dd> <dt>

<span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**
</dt> <dd>

**TRUE** abilita lo stencil su due lati, **FALSE** lo disabilita. Il valore predefinito è **FALSE.** L'applicazione deve impostare D3DRS \_ CULLMODE su D3DCULL NONE per abilitare la \_ modalità di stencil a due lati. Se l'ordine di avvolgimento del triangolo è in senso orario, verranno usate le operazioni D3DRS \_ \* STENCIL. Se l'ordine di avvolgimento è in senso antiorario, verranno usate le operazioni \_ CCW STENCIL D3DRS. \_ \*

Per verificare se lo stencil a due lati è supportato, controllare il membro StencilCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per D3DSTENCILCAPS \_ TWOSIDED. Vedere anche [D3DSTENCILCAPS](d3dstencilcaps.md).

</dd> <dt>

<span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**STENCIL \_ CCW D3DRSFAIL \_**
</dt> <dd>

Operazione stencil da eseguire se il test dello stencil CCW ha esito negativo. I valori derivano [**dal tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md) Il valore predefinito è D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**\_STENCIL CCW D3DRSZFAIL \_**
</dt> <dd>

Operazione stencil da eseguire se il test dello stencil CCW ha esito positivo e z-test ha esito negativo. I valori derivano [**dal tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md) Il valore predefinito è D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**
</dt> <dd>

Operazione stencil da eseguire se vengono superati sia lo stencil CCW che i test z. I valori derivano [**dal tipo enumerato D3DSTENCILOP.**](./d3dstencilop.md) Il valore predefinito è D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**
</dt> <dd>

Funzione di confronto. Il test degli stencil CCW viene superato se ((ref & mask) funzione stencil (stencil & mask)) è **TRUE.** I valori derivano [**dal tipo enumerato D3DCMPFUNC.**](./d3dcmpfunc.md) Il valore predefinito è D3DCMP \_ ALWAYS.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**
</dt> <dd>

Valori ColorWriteEnable aggiuntivi per i dispositivi. Vedere D3DRS \_ COLORWRITEENABLE. Questa funzionalità è disponibile se il bit di funzionalità D3DPMISCCAPS INDEPENDENTWRITEMASKS è impostato nel membro \_ PrimitiveMiscCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo. Il valore predefinito è 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**
</dt> <dd>

Valori ColorWriteEnable aggiuntivi per i dispositivi. Vedere D3DRS \_ COLORWRITEENABLE. Questa funzionalità è disponibile se il bit di funzionalità D3DPMISCCAPS INDEPENDENTWRITEMASKS è impostato nel membro \_ PrimitiveMiscCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo. Il valore predefinito è 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**
</dt> <dd>

Valori ColorWriteEnable aggiuntivi per i dispositivi. Vedere D3DRS \_ COLORWRITEENABLE. Questa funzionalità è disponibile se il bit di funzionalità D3DPMISCCAPS INDEPENDENTWRITEMASKS è impostato nel membro \_ PrimitiveMiscCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per il dispositivo. Il valore predefinito è 0x0000000f.

</dd> <dt>

<span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**
</dt> <dd>

[**D3DCOLOR usato**](d3dcolor.md) per un fattore di blend costante durante la fusione alfa. Questa funzionalità è disponibile se il bit di funzionalità D3DPBLENDCAPS BLENDFACTOR è impostato nel membro \_ SrcBlendCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) o nel membro DestBlendCaps di **D3DCAPS9.** Vedere [**D3DRENDERSTATETYPE**](). Il valore predefinito è 0xffffffff.

</dd> <dt>

<span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**
</dt> <dd>

Abilitare le scritture della destinazione di rendering per la correzione gamma in sRGB. Il formato deve esporre D3DUSAGE \_ SRGBWRITE. Il valore predefinito è 0.

</dd> <dt>

<span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**
</dt> <dd>

Valore a virgola mobile utilizzato per il confronto dei valori di profondità. Vedere [Distorsione della profondità (Direct3D 9).](depth-bias.md) Il valore predefinito è 0.

</dd> <dt>

<span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**
</dt> <dd>

Vedere D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**
</dt> <dd>

**TRUE** abilita la modalità di fusione separata per il canale alfa. Il valore predefinito è **FALSE.**

Se impostato su **FALSE,** i fattori di fusione della destinazione di rendering e le operazioni applicate al valore alfa devono essere uguali a quelli definiti per il colore. Questa modalità viene effettivamente impostata come hardwired su **FALSE** nelle implementazioni che non impostano il limite D3DPMISCCAPS \_ SEPARATEALPHABLEND. Vedere [D3DPMISCCAPS](d3dpmisccaps.md).

Il tipo di fusione alfa separata è determinato dagli stati di rendering D3DRS \_ SRCBLENDALPHA e D3DRS \_ DESTBLENDALPHA.

</dd> <dt>

<span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**
</dt> <dd>

Membro del tipo [**enumerato D3DBLEND.**](./d3dblend.md) Questo valore viene ignorato a meno che D3DRS \_ SEPARATEALPHABLENDENABLE non sia **TRUE.** Il valore predefinito è D3DBLEND \_ ONE.

</dd> <dt>

<span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**
</dt> <dd>

Membro del tipo [**enumerato D3DBLEND.**](./d3dblend.md) Questo valore viene ignorato a meno che D3DRS \_ SEPARATEALPHABLENDENABLE non sia **TRUE.** Il valore predefinito è D3DBLEND \_ ZERO.

</dd> <dt>

<span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**
</dt> <dd>

Valore utilizzato per selezionare l'operazione aritmetica applicata alla fusione alfa separata quando lo stato di rendering, D3DRS \_ SEPARATEALPHABLENDENABLE, è impostato su **TRUE.**

I valori validi sono definiti dal [**tipo enumerato D3DBLENDOP.**](./d3dblendop.md) Il valore predefinito è D3DBLENDOP \_ ADD.

Se la funzionalità del dispositivo D3DPMISCCAPS BLENDOP non è supportata, viene eseguito \_ D3DBLENDOP \_ ADD. Vedere [D3DPMISCCAPS](d3dpmisccaps.md).

</dd> <dt>

<span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti



| Stati di rendering        |   Campionatore di trama                 |
|----------------------|--------------------|
| ps \_ 1 \_ 1 a ps \_ 1 \_ 3 | 4 campionatori di trama |



 

Direct3D definisce la costante WRAPBIAS D3DRENDERSTATE per consentire alle applicazioni di abilitare o disabilitare il wrapping delle trame, in base all'intero in base zero di un set di coordinate di trama (anziché usare in modo esplicito uno dei valori di stato \_ WRAP n D3DRS). \_ Aggiungere il valore D3DRENDERSTATE WRAPBIAS all'indice in base zero di un set di coordinate di trama per calcolare il valore WRAP n D3DRS corrispondente a tale indice, come illustrato nell'esempio \_ \_ seguente.


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
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
