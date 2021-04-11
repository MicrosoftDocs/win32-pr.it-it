---
description: Gli Stati della fase trama definiscono le operazioni di trama a più Blend.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Enumerazione D3DTEXTURESTAGESTATETYPE (D3D9Types. h)
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
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234983"
---
# <a name="d3dtexturestagestatetype-enumeration"></a>Enumerazione D3DTEXTURESTAGESTATETYPE

Gli Stati della fase trama definiscono le operazioni di trama a più Blend. Alcuni Stati del campionatore configurano l'elaborazione dei vertici e alcuni configurano l'elaborazione dei pixel. Gli Stati della fase della trama possono essere salvati e ripristinati usando stateblocks (vedere lo stato [di salvataggio e ripristino del blocco di stato (Direct3D 9)](state-blocks-save-and-restore-state.md)).

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

<span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**\_COLOROP D3DTSS**
</dt> <dd>

Lo stato della fase di trama è un'operazione di combinazione dei colori di trama identificata da un membro del tipo enumerato [**D3DTEXTUREOP**](./d3dtextureop.md) . Il valore predefinito per la prima fase della trama (fase 0) è D3DTOP \_ Modulation. per tutte le altre fasi, il valore predefinito è D3DTOP \_ Disable.

</dd> <dt>

<span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**\_COLORARG1 D3DTSS**
</dt> <dd>

Trama: lo stato della fase è il primo argomento di colore per la fase, identificato da uno dei [D3DTA](d3dta.md). L'argomento predefinito è D3DTA \_ texture.

Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP. Il valore predefinito per il registro è (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**\_COLORARG2 D3DTSS**
</dt> <dd>

Trama: lo stato della fase è il secondo argomento di colore per la fase, identificato da [D3DTA](d3dta.md). L'argomento predefinito è D3DTA \_ Current. Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP. Il valore predefinito per il registro è (0,0, 0,0, 0,0, 0,0)

</dd> <dt>

<span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**\_ALPHAOP D3DTSS**
</dt> <dd>

Lo stato della fase di trama è un'operazione di fusione alfa di trama identificata da un membro del tipo enumerato [**D3DTEXTUREOP**](./d3dtextureop.md) . Il valore predefinito per la prima fase della trama (fase 0) è D3DTOP \_ SELECTARG1 e per tutte le altre fasi il valore predefinito è D3DTOP \_ Disable.

</dd> <dt>

<span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**\_ALPHAARG1 D3DTSS**
</dt> <dd>

Trama: lo stato della fase è il primo argomento alfa per la fase, identificato da da [D3DTA](d3dta.md). L'argomento predefinito è D3DTA \_ texture. Se per questa fase non è impostata alcuna trama, l'argomento predefinito è D3DTA \_ Diffusion. Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP. Il valore predefinito per il registro è (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**\_ALPHAARG2 D3DTSS**
</dt> <dd>

Lo stato della fase di trama è il secondo argomento Alpha per la fase, identificato da da [D3DTA](d3dta.md). L'argomento predefinito è D3DTA \_ Current. Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP. Il valore predefinito per il registro è (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**\_BUMPENVMAT00 D3DTSS**
</dt> <dd>

Lo stato della fase della trama è un valore a virgola mobile per il \[ \] \[ \] coefficiente 0 0 in una matrice di mapping Bump. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**\_BUMPENVMAT01 D3DTSS**
</dt> <dd>

Lo stato della fase della trama è un valore a virgola mobile per il \[ \] \[ \] coefficiente 0 1 in una matrice di mapping Bump. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**\_BUMPENVMAT10 D3DTSS**
</dt> <dd>

Lo stato della fase trama è un valore a virgola mobile per il \[ \] \[ \] coefficiente 1 0 in una matrice di mapping Bump. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**\_BUMPENVMAT11 D3DTSS**
</dt> <dd>

Lo stato della fase della trama è un valore a virgola mobile per il \[ \] \[ \] coefficiente 1 1 in una matrice di mapping Bump. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**\_TEXCOORDINDEX D3DTSS**
</dt> <dd>

Indice del set di coordinate di trama da usare con questa fase della trama. È possibile specificare fino a otto set di coordinate di trama per vertice. Se un vertice non include un set di coordinate di trama in corrispondenza dell'indice specificato, l'impostazione predefinita del sistema è le coordinate utente e v (0,0).

Quando si esegue il rendering usando vertex shader, l'indice delle coordinate di trama di ogni fase deve essere impostato sul valore predefinito. L'indice predefinito per ogni fase è uguale all'indice della fase. Impostare questo stato sull'indice in base zero del set di coordinate per ogni vertice utilizzato da questa fase della trama.

Inoltre, le applicazioni possono includere, come Logical o con l'indice da impostare, una delle costanti per richiedere che Direct3D generi automaticamente le coordinate di trama di input per una trasformazione di trama. Per un elenco di tutte le costanti, vedere [D3DTSS \_ TCI](d3dtss-tci.md).

Ad eccezione di D3DTSS \_ TCI \_ PassThru, che viene risolto in zero, se è incluso uno dei valori seguenti con l'indice da impostare, il sistema usa l'indice esclusivamente per determinare la modalità di wrapping della trama. Questi flag sono particolarmente utili quando si esegue il mapping dell'ambiente.

</dd> <dt>

<span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**\_BUMPENVLSCALE D3DTSS**
</dt> <dd>

Valore della scala a virgola mobile per la luminanza della mappa Bump. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**\_BUMPENVLOFFSET D3DTSS**
</dt> <dd>

Valore di offset a virgola mobile per la luminanza della mappa Bump. Il valore predefinito è 0,0.

</dd> <dt>

<span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**\_TEXTURETRANSFORMFLAGS D3DTSS**
</dt> <dd>

Membro del tipo enumerato [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) che controlla la trasformazione delle coordinate di trama per questa fase della trama. Il valore predefinito è D3DTTFF \_ Disable.

</dd> <dt>

<span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**\_COLORARG0 D3DTSS**
</dt> <dd>

Impostazioni per il terzo operando di colore per le operazioni triadi (moltiplicazione, aggiunta e interpolazione lineare), identificate da [D3DTA](d3dta.md). Questa impostazione è supportata se \_ sono presenti le funzionalità del dispositivo D3DTEXOPCAPS MULTIPLYADD o D3DTEXOPCAPS \_ LERP. L'argomento predefinito è D3DTA \_ Current. Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP. Il valore predefinito per il registro è (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**\_ALPHAARG0 D3DTSS**
</dt> <dd>

Impostazioni per l'operando del selettore di canale alfa per le operazioni di triade (moltiplicazione, aggiunta e interpolazione lineare), identificate da [D3DTA](d3dta.md). Questa impostazione è supportata se \_ sono presenti le funzionalità del dispositivo D3DTEXOPCAPS MULTIPLYADD o D3DTEXOPCAPS \_ LERP. L'argomento predefinito è D3DTA \_ Current. Specificare D3DTA \_ Temp per selezionare un colore di registro temporaneo per la lettura o la scrittura. D3DTA \_ Temp è supportato se \_ è presente la funzionalità del dispositivo D3DPMISCCAPS TSSARGTEMP. L'argomento predefinito è (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**\_RESULTARG D3DTSS**
</dt> <dd>

Impostazione per selezionare il registro di destinazione per il risultato di questa fase, identificato da [D3DTA](d3dta.md). Questo valore può essere impostato su D3DTA \_ Current (valore predefinito) o su D3DTA \_ Temp, ovvero un singolo registro temporaneo che può essere letto nelle fasi successive come argomento di input. Il colore finale passato al Blender di nebbia e al buffer dei frame viene ricavato da D3DTA \_ Current, quindi l'ultimo stato della fase della trama attivo deve essere impostato su Write in Current. Questa impostazione è supportata se \_ è presente la funzionalità del dispositivo TSSARGTEMP D3DPMISCCAPS.

</dd> <dt>

<span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**\_Costante D3DTSS**
</dt> <dd>

Colore costante per fase. Per verificare se un dispositivo supporta un colore costante per fase, vedere la costante D3DPMISCCAPS \_ PERSTAGECONSTANT in [D3DPMISCCAPS](d3dpmisccaps.md). \_La costante D3DTSS viene utilizzata dalla \_ costante D3DTA. Vedere [D3DTA](d3dta.md).

</dd> <dt>

<span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri di questo tipo enumerato vengono utilizzati con i metodi [**IDirect3DDevice9:: GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) e [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) per recuperare e impostare i valori dello stato della trama.

L'intervallo valido di valori per i \_ coefficienti della matrice di mapping di D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 e D3DTSS BUMPENVMAT11 \_ è maggiore o uguale a-8,0 e minore di 8,0. Questo intervallo, espresso in notazione matematica è (-8.0, 8.0).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
