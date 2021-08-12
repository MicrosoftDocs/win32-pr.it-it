---
title: texkill - ps
description: Annulla il rendering del pixel corrente se uno dei primi tre componenti (UVW) delle coordinate della trama è minore di zero.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 462549a9caba9b4b49ca5b5ac088e41320b3d6f731a78a0251d5191cc601a2e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118284029"
---
# <a name="texkill---ps"></a>texkill - ps

Annulla il rendering del pixel corrente se uno dei primi tre componenti (UVW) delle coordinate della trama è minore di zero.

## <a name="syntax"></a>Sintassi



| texkill dst |
|-------------|



 

dove

-   dst è un registro di destinazione

## <a name="remarks"></a>Commenti



| Versioni dei pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texkill               | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Questa istruzione corrisponde alla funzione [**clip**](dx-graphics-hlsl-clip.md) di HLSL.

texkill non campionare alcuna trama. Opera sui primi tre componenti delle coordinate della trama specificate dal numero di registro di destinazione. Per ps \_ 1 \_ 4, texkill opera sui dati nei primi tre componenti del registro di destinazione.

È possibile usare questa istruzione per implementare piani di ritaglio arbitrari nel rasterizzatore.

Quando si usano vertex shader, l'applicazione è responsabile dell'applicazione della trasformazione della prospettiva. Ciò può causare problemi per i piani di ritaglio arbitrari perché se contiene fattori di scala anisomorfici, anche i piani di ritaglio devono essere trasformati. Pertanto, è meglio fornire una posizione di vertice non progetto da usare nel clipper arbitrario, ovvero il set di coordinate della trama identificato dall'operatore texkill.

Questa istruzione viene usata come segue:

<dl> texkill tn  
La maschera dei pixel viene eseguita nel modo seguente:  
if ( componenti x,y,z di TextureCoordinates(stage n)<sub>UVWQ</sub>< 0 )  
annullare il rendering dei pixel
</dl>

Per pixel shader \_ 1 1, 1 2 e \_ 1 3, texkill opera sulla coordinata di trama specificata dal numero di registro \_ di destinazione. Nella versione \_ 1 4, tuttavia, texkill opera [](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) sui dati contenuti nel Registro coordinate trama (tn) o nel registro temporaneo (rn) specificato come destinazione.

Quando il multicampionamento è abilitato, qualsiasi effetto di antialiasing ottenuto sui bordi dei poligoni a causa del multicampionamento non verrà ottenuto lungo alcun bordo generato da texkill. Il pixel shader viene eseguito una volta per pixel.

Questo esempio viene utilizzato solo a scopo illustrativo.

Questo esempio maschera i pixel con coordinate di trama negative. I colori dei pixel vengono interpolati dai colori dei vertici forniti nei dati dei vertici.


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



Le coordinate della trama vanno da -0,5 a 0,5 in u e da 0,0 a 1,0 in v. Questa istruzione fa sì che i valori u negativi vengono mascherati. La prima figura seguente mostra il colore del vertice applicato al quad senza l'istruzione texkill applicata. La seconda figura seguente mostra il risultato dell'istruzione texkill. I colori dei pixel delle coordinate della trama inferiori a 0 (dove x va da -0,5 a 0,0) vengono mascherati. Il colore di sfondo (bianco) viene usato quando il colore del pixel viene mascherato.

![illustrazione dell'output con il colore del vertice applicato al quad senza l'istruzione texkill](images/pstexkill-in.jpg)![Illustrazione dell'output con l'istruzione texkill applicata](images/pstexkill-out.jpg)

I dati delle coordinate della trama vengono dichiarati nella dichiarazione dei dati dei vertici in questo esempio.


```
   
struct CUSTOMVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu1, tv1;
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_TEX1|D3DTEXCOORD2(0))

static CUSTOMVERTEX g_Vertices[]=
{
    //  x      y     z    color         u1,    v1  
    { -1.0f, -1.0f, 0.0f, 0xffff0000, -0.5f,  1.0f, },
    {  1.0f, -1.0f, 0.0f, 0xff00ff00,  0.5f,  1.0f, },
    {  1.0f,  1.0f, 0.0f, 0xff0000ff,  0.5f,  0.0f, },
    { -1.0f,  1.0f, 0.0f, 0xffffffff, -0.5f,  0.0f, },

};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




