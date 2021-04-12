---
description: Definisce operazioni di combinazione di trame per fase.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: Enumerazione D3DTEXTUREOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354514"
---
# <a name="d3dtextureop-enumeration"></a>Enumerazione D3DTEXTUREOP

Definisce operazioni di combinazione di trame per fase.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**\_Disabilitazione D3DTOP**
</dt> <dd>

Disabilita l'output di questa fase di trama e tutte le fasi con un indice superiore. Per disabilitare il mapping della trama, impostarlo come operazione di colore per la prima fase della trama (fase 0). Non è possibile disabilitare le operazioni Alpha quando sono abilitate le operazioni sui colori. L'impostazione dell'operazione Alpha su D3DTOP \_ Disabilita quando è abilitata la fusione dei colori causa un comportamento non definito.

</dd> <dt>

<span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**\_SELECTARG1 D3DTOP**
</dt> <dd>

Usare il primo colore o l'argomento alfa della fase di trama, senza modifiche, come output. Questa operazione influiscono sull'argomento color se usato con lo \_ stato della fase della trama COLOROP di D3DTSS e l'argomento Alpha se usato con D3DTSS \_ ALPHAOP.

![equazione di questo argomento (s (RGBA) = arg1)](images/topfrm1.png)

</dd> <dt>

<span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**\_SELECTARG2 D3DTOP**
</dt> <dd>

Usare il secondo colore o l'argomento alfa della fase della trama, senza modifiche, come output. Questa operazione influiscono sull'argomento color se usato con lo \_ stato della fase della trama COLOROP di D3DTSS e l'argomento Alpha se usato con D3DTSS \_ ALPHAOP.

![equazione di questo argomento (s (RGBA) = arg2)](images/topfrm2.png)

</dd> <dt>

<span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**\_Modulazione D3DTOP**
</dt> <dd>

Moltiplicare i componenti degli argomenti.

![equazione dell'operazione di modulazione (s (RGBA) = arg1 x ARG 2)](images/topfrm3.png)

</dd> <dt>

<span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**\_MODULATE2X D3DTOP**
</dt> <dd>

Moltiplicare i componenti degli argomenti e spostare i prodotti fino a un bit a sinistra (moltiplicando in modo efficace per 2) per schiarire.

![equazione dell'operazione modulate2X (s (RGBA) = (arg1 x ARG 2), quindi Shift Left 1)](images/topfrm4.png)

</dd> <dt>

<span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**\_MODULATE4X D3DTOP**
</dt> <dd>

Moltiplicare i componenti degli argomenti e spostare i prodotti verso sinistra a 2 bit (moltiplicando in modo efficace per 4) per schiarire.

![equazione dell'operazione Modulate4X (s (RGBA) = (arg1 x ARG 2), quindi Shift Left 2)](images/topfrm5.png)

</dd> <dt>

<span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ aggiungere**
</dt> <dd>

Aggiungere i componenti degli argomenti.

![equazione dell'operazione di aggiunta (s (RGBA) = arg1 + ARG 2)](images/topfrm6.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**\_ADDSIGNED D3DTOP**
</dt> <dd>

Aggiungere i componenti degli argomenti con una deviazione-0,5, rendendo l'intervallo di valori effettivo compreso tra-0,5 e 0,5.

![equazione dell'operazione di aggiunta firmata (s (RGBA) = arg1 + ARG 2-0,5)](images/topfrm7.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**\_ADDSIGNED2X D3DTOP**
</dt> <dd>

Aggiungere i componenti degli argomenti con la distorsione-0,5 e spostare i prodotti sul bit a sinistra.

![equazione dell'operazione di aggiunta di un 2x firmato ((s (RGBA) = arg1 + ARG 2-0,5), quindi MAIUSC a sinistra 1)](images/topfrm8.png)

</dd> <dt>

<span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**\_Sottrazione D3DTOP**
</dt> <dd>

Sottrarre i componenti del secondo argomento da quelli del primo argomento.

![equazione dell'operazione di sottrazione (s (RGBA) = arg1-ARG 2)](images/topfrm9.png)

</dd> <dt>

<span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**\_ADDSMOOTH D3DTOP**
</dt> <dd>

Aggiungere il primo e il secondo argomento; quindi sottrarre il prodotto dalla somma.

![equazione dell'aggiunta di operazioni Smooth (s (RGBA) = arg1 + ARG 2 x (1-arg1))](images/topfrm10.png)

</dd> <dt>

<span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**\_BLENDDIFFUSEALPHA D3DTOP**
</dt> <dd>

Combina in modo lineare questa fase della trama, usando l'alfa interpolato da ogni vertice.

![equazione delle operazioni Alpha Diffusion Blend (s (RGBA) = arg1 x Alpha + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**\_BLENDTEXTUREALPHA D3DTOP**
</dt> <dd>

Combina in modo lineare questa fase della trama, usando l'alfa dalla trama di questa fase.

![equazione dell'operazione Alpha trama di Blend (s (RGBA) = arg1 x Alpha + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**\_BLENDFACTORALPHA D3DTOP**
</dt> <dd>

Combina in modo lineare questa fase della trama, usando un set di alfa scalari con lo \_ stato di rendering TEXTUREFACTOR di D3DRS.

![equazione del fattore di fusione Alpha Operation (s (RGBA) = arg1 x Alpha + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**\_BLENDTEXTUREALPHAPM D3DTOP**
</dt> <dd>

Combina in modo lineare una fase di trama che utilizza un valore alfa premoltiplicato.

![equazione della trama di Blend Alpha PM Operation (s (RGBA) = arg1 + ARG 2 x (1-Alpha))](images/topfrm12.png)

</dd> <dt>

<span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**\_BLENDCURRENTALPHA D3DTOP**
</dt> <dd>

Combina in modo lineare questa fase della trama, usando l'alfa tratto dalla fase di trama precedente.

![equazione dell'operazione Alpha corrente di Blend (s (RGBA) = arg1 x Alpha + arg2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**\_PREmodulazione D3DTOP**
</dt> <dd>

\_La PREmodulazione D3DTOP è impostata nella fase n. L'output della fase n è arg1. Inoltre, se è presente una trama nella fase n + 1, qualsiasi D3DTA \_ corrente nella fase n + 1 viene premoltiplicato per trama nella fase n + 1.

</dd> <dt>

<span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ MODULATEALPHA \_ ADDCOLOR**
</dt> <dd>

Modulare il colore del secondo argomento, usando l'alfa del primo argomento; Aggiungere quindi il risultato all'argomento 1. Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).

![equazione dell'operazione Alpha di modulazione del colore (s (RGBA) = arg1 (RGB) + arg1 (a) x arg2 (RGB)](images/topfrm13.png)

</dd> <dt>

<span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ MODULATECOLOR \_ ADDALPHA**
</dt> <dd>

Modulare gli argomenti; quindi aggiungere l'alfa del primo argomento. Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).

![equazione dell'operazione di aggiunta del colore Alpha modulate (s (RGBA) = arg1 (RGB) x arg2 (RGB) + arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ MODULATEINVALPHA \_ ADDCOLOR**
</dt> <dd>

Simile a D3DTOP \_ MODULATEALPHA \_ ADDCOLOR, ma usare l'inverso dell'alfa del primo argomento. Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).

![equazione del colore di aggiunta modulazione dell'operazione inversa Alpha (s (RGBA) = (1-arg1 (a)) x arg2 (RGB) + arg1 (RGB))](images/topfrm15.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ MODULATEINVCOLOR \_ ADDALPHA**
</dt> <dd>

Simile a D3DTOP \_ MODULATECOLOR \_ ADDALPHA, ma usare l'inverso del colore del primo argomento. Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).

![equazione dell'operazione di aggiunta del colore inverso Alpha modulazione (s (RGBA) = (1-arg1 (RGB)) x arg2 (RGB) + arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**\_BUMPENVMAP D3DTOP**
</dt> <dd>

Eseguire il mapping dei riscontri per pixel, usando la mappa dell'ambiente nella fase di trama successiva, senza luminanza. Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).

</dd> <dt>

<span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**\_BUMPENVMAPLUMINANCE D3DTOP**
</dt> <dd>

Eseguire il mapping dei riscontri per pixel, usando la mappa dell'ambiente nella fase di trama successiva, con luminanza. Questa operazione è supportata solo per le operazioni relative ai colori (D3DTSS \_ COLOROP).

</dd> <dt>

<span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**\_DOTPRODUCT3 D3DTOP**
</dt> <dd>

Modulare i componenti di ogni argomento come componenti firmati, aggiungere i relativi prodotti; quindi replicare la somma in tutti i canali di colore, incluso Alpha. Questa operazione è supportata per le operazioni di colore e alfa.

![equazione del prodotto 3 operazione (s (RGBA) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b)](images/topfrm17.png)

In DirectX 6 e DirectX 7, le operazioni di multitrama gli input precedenti sono tutte spostate verso la metà (y = x-0,5) prima dell'utilizzo per simulare i dati firmati e il risultato scalare viene automaticamente fissato ai valori positivi e viene replicato in tutti e tre i canali di output. Si noti inoltre che, come operazione di colore, questo non aggiorna l'Alpha aggiorna solo i componenti RGB.

Tuttavia, nello shader DirectX 8,1 è possibile specificare che l'output venga indirizzato ai componenti. RGB o. a o a entrambi (impostazione predefinita). È anche possibile specificare un'operazione scalare separata sul canale alfa.

</dd> <dt>

<span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**\_MULTIPLYADD D3DTOP**
</dt> <dd>

Esegue un'operazione di accumulo di moltiplicazione. Accetta gli ultimi due argomenti, li moltiplica insieme, li aggiunge all'argomento di input/origine rimanente e li inserisce nel risultato.

S<sub>RGBA</sub> = arg1 + arg2 \* Arg3

</dd> <dt>

<span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**\_LERP D3DTOP**
</dt> <dd>

Esegue l'interpolazione lineare tra il secondo e il terzo argomento di origine in base a una proporzione specificata nel primo argomento di origine.

S<sub>RGBA</sub> = (arg1) \* arg2 + (1-arg1) \* arg3.

</dd> <dt>

<span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri di questo tipo vengono usati quando si impostano le operazioni color o Alpha usando i \_ valori D3DTSS COLOROP o D3DTSS \_ ALPHAOP con il metodo [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .

Nelle formule precedenti, S<sub>RGBA</sub> è il colore RGBA prodotto da un'operazione di trama, mentre arg1, arg2 e arg3 rappresentano il colore RGBA completo degli argomenti della trama. I singoli componenti di un argomento vengono visualizzati con pedici. Ad esempio, il componente alfa per l'argomento 1 verrebbe visualizzato come arg1<sub>A</sub>.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
