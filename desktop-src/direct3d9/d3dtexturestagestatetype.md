---
description: Gli stati della fase di trama definiscono le operazioni di trama multi blender.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Enumerazione D3DTEXTURESTAGESTATETYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4879009f603a6943302f0595f37176ec5edf8e1a1d3212efedb66c923d775104
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894151"
---
# <a name="d3dtexturestagestatetype-enumeration"></a>Enumerazione D3DTEXTURESTAGESTATETYPE

Gli stati della fase di trama definiscono le operazioni di trama multi blender. Alcuni stati del campionatore configurano l'elaborazione dei vertici e altri ancora l'elaborazione dei pixel. Gli stati della fase di trama possono essere salvati e ripristinati usando blocchi di stato (vedere [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ COLOROP**
</dt> <dd>

Lo stato della fase di trama è un'operazione di fusione del colore della trama identificata da un membro del [**tipo enumerato D3DTEXTUREOP.**](./d3dtextureop.md) Il valore predefinito per la prima fase della trama (fase 0) è D3DTOP MODULATE. Per tutte le altre fasi il valore predefinito è \_ D3DTOP \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**
</dt> <dd>

Lo stato della fase di trama è il primo argomento di colore per la fase, identificato da uno degli elementi [D3DTA.](d3dta.md) L'argomento predefinito è TEXTURE D3DTA. \_

Specificare D3DTA \_ TEMP per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA TEMP è supportato se è presente la funzionalità del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP. Il valore predefinito per il registro è (0.0, 0.0, 0.0, 0.0, 0.0).

</dd> <dt>

<span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**
</dt> <dd>

Lo stato della fase di trama è il secondo argomento di colore per la fase, identificato da [D3DTA.](d3dta.md) L'argomento predefinito è D3DTA \_ CURRENT. Specificare D3DTA \_ TEMP per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA TEMP è supportato se è presente la funzionalità del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP. Il valore predefinito per il registro è (0.0, 0.0, 0.0, 0.0, 0.0)

</dd> <dt>

<span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ ALPHAOP**
</dt> <dd>

Lo stato della fase di trama è un'operazione di fusione alfa della trama identificata da un membro del [**tipo enumerato D3DTEXTUREOP.**](./d3dtextureop.md) Il valore predefinito per la prima fase della trama (fase 0) è D3DTOP SELECTARG1 e per tutte le altre fasi il valore predefinito è \_ D3DTOP \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**
</dt> <dd>

Lo stato della fase di trama è il primo argomento alfa per la fase, identificato da [D3DTA.](d3dta.md) L'argomento predefinito è TEXTURE D3DTA. \_ Se per questa fase non è impostata alcuna trama, l'argomento predefinito è D3DTA \_ DIFFUSE. Specificare D3DTA \_ TEMP per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA TEMP è supportato se è presente la funzionalità del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP. Il valore predefinito per il registro è (0.0, 0.0, 0.0, 0.0, 0.0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**
</dt> <dd>

Lo stato della fase di trama è il secondo argomento alfa per la fase, identificato da [D3DTA.](d3dta.md) L'argomento predefinito è D3DTA \_ CURRENT. Specificare D3DTA \_ TEMP per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA TEMP è supportato se è presente la funzionalità del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP. Il valore predefinito per il registro è (0.0, 0.0, 0.0, 0.0, 0.0).

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**
</dt> <dd>

Lo stato della fase di trama è un valore a virgola mobile per il \[ \] \[ coefficiente 0 0 \] in una matrice di bump-mapping. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**
</dt> <dd>

Lo stato della fase di trama è un valore a virgola mobile per il \[ \] \[ coefficiente 0 1 \] in una matrice di bump mapping. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**
</dt> <dd>

Lo stato della fase di trama è un valore a virgola mobile per il \[ \] \[ coefficiente 1 0 \] in una matrice di bump mapping. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**
</dt> <dd>

Lo stato della fase di trama è un valore a virgola mobile per il \[ \] \[ coefficiente 1 1 \] in una matrice di bump mapping. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ TEXCOORDINDEX**
</dt> <dd>

Indice della coordinata di trama impostata da usare con questa fase della trama. È possibile specificare fino a otto set di coordinate di trama per vertice. Se un vertice non include un set di coordinate di trama in corrispondenza dell'indice specificato, il sistema imposta per impostazione predefinita le coordinate you e v (0,0).

Quando si esegue il rendering con vertex shader, l'indice delle coordinate di trama di ogni fase deve essere impostato sul valore predefinito. L'indice predefinito per ogni fase è uguale all'indice di fase. Impostare questo stato sull'indice in base zero del set di coordinate per ogni vertice utilizzato da questa fase di trama.

Inoltre, le applicazioni possono includere, come OR logico con l'indice impostato, una delle costanti per richiedere che Direct3D generi automaticamente le coordinate di trama di input per una trasformazione di trama. Per un elenco di tutte le costanti, vedere [D3DTSS \_ TCI](d3dtss-tci.md).

Ad eccezione di D3DTSS \_ TCI PASSTHRU, che si risolve in zero, se uno dei valori seguenti è incluso nell'indice impostato, il sistema usa l'indice esclusivamente per determinare la modalità di wrapping della \_ trama. Questi flag sono particolarmente utili quando si esegue il mapping dell'ambiente.

</dd> <dt>

<span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ BUMPENVLSCALE**
</dt> <dd>

Valore della scala a virgola mobile per la luminanza della mappa a rilievo. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ BUMPENVLOFFSET**
</dt> <dd>

Valore di offset a virgola mobile per la luminanza della mappa a rilievo. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ TEXTURETRANSFORMFLAGS**
</dt> <dd>

Membro del tipo [**enumerato D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) che controlla la trasformazione delle coordinate di trama per questa fase della trama. Il valore predefinito è D3DTTFF \_ DISABLE.

</dd> <dt>

<span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**
</dt> <dd>

Impostazioni per il terzo operando di colore per le operazioni triadic (moltiplicazione, aggiunta e interpolazione lineare), identificato da [D3DTA.](d3dta.md) Questa impostazione è supportata se sono presenti le funzionalità del dispositivo \_ LERP D3DTEXOPCAPS MULTIPLYADD o D3DTEXOPCAPS. \_ L'argomento predefinito è D3DTA \_ CURRENT. Specificare D3DTA \_ TEMP per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA TEMP è supportato se è presente la funzionalità del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP. Il valore predefinito per il registro è (0.0, 0.0, 0.0, 0.0, 0.0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**
</dt> <dd>

Impostazioni per l'operando del selettore del canale alfa per le operazioni triadic (moltiplicazione, aggiunta e interpolazione lineare), identificato da [D3DTA.](d3dta.md) Questa impostazione è supportata se sono presenti le funzionalità del dispositivo \_ LERP D3DTEXOPCAPS MULTIPLYADD o D3DTEXOPCAPS. \_ L'argomento predefinito è D3DTA \_ CURRENT. Specificare D3DTA \_ TEMP per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA TEMP è supportato se è presente la funzionalità del dispositivo \_ D3DPMISCCAPS \_ TSSARGTEMP. L'argomento predefinito è (0.0, 0.0, 0.0, 0.0).

</dd> <dt>

<span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ RESULTARG**
</dt> <dd>

Impostazione per selezionare il registro di destinazione per il risultato di questa fase, identificato da [D3DTA](d3dta.md). Questo valore può essere impostato su D3DTA \_ CURRENT (valore predefinito) o su D3DTA TEMP, ovvero un singolo registro temporaneo che può essere letto nelle fasi successive come argomento \_ di input. Il colore finale passato al blender e al buffer dei fotogrammi viene tratto da D3DTA CURRENT, quindi l'ultimo stato della fase di trama attiva deve essere impostato per scrivere su \_ current. Questa impostazione è supportata se è presente la funzionalità del dispositivo D3DPMISCCAPS \_ TSSARGTEMP.

</dd> <dt>

<span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**COSTANTE D3DTSS \_**
</dt> <dd>

Colore costante per fase. Per verificare se un dispositivo supporta un colore costante per fase, vedere la costante D3DPMISCCAPS \_ PERSTAGECONSTANT in [D3DPMISCCAPS](d3dpmisccaps.md). D3DTSS \_ CONSTANT viene usato da D3DTA \_ CONSTANT. Vedere [D3DTA](d3dta.md).

</dd> <dt>

<span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri di questo tipo enumerato vengono usati con i [**metodi IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) e [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) per recuperare e impostare i valori dello stato della trama.

L'intervallo valido di valori per i coefficienti D3DTSS \_ BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 e D3DTSS BUMPENVMAT11 è maggiore o uguale a \_ -8.0 e minore di 8.0. Questo intervallo, espresso in notazione matematica, è (-8.0,8.0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
