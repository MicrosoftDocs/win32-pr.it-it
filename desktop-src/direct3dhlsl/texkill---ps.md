---
title: texkill-PS
description: Annulla il rendering del pixel corrente se uno dei primi tre componenti (UVW) delle coordinate di trama è minore di zero.
ms.assetid: 7641aef8-8931-4a19-827a-75ab17e901ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4da9c6b59a3c16eeecb8755f2f19542df6ee8a7b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335447"
---
# <a name="texkill---ps"></a>texkill-PS

Annulla il rendering del pixel corrente se uno dei primi tre componenti (UVW) delle coordinate di trama è minore di zero.

## <a name="syntax"></a>Sintassi



| texkill DST |
|-------------|



 

dove

-   DST è un registro di destinazione

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texkill               | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Questa istruzione corrisponde alla funzione di [**ritaglio**](dx-graphics-hlsl-clip.md) HLSL.

texkill non campiona alcuna trama. Opera sui primi tre componenti delle coordinate di trama fornite dal numero di registro di destinazione. Per PS \_ 1 \_ 4, texkill opera sui dati nei primi tre componenti del registro di destinazione.

È possibile utilizzare questa istruzione per implementare piani di ritaglio arbitrari nel rasterizzatore.

Quando si usano vertex shader, l'applicazione è responsabile dell'applicazione della trasformazione della prospettiva. Questo può causare problemi per i piani di ritaglio arbitrari perché se contiene fattori di scala anisomorphic, è necessario trasformare anche i piani di ritaglio. Pertanto, è preferibile fornire una posizione di vertice non proiettata da usare nel Clipper arbitrario, ovvero il set di coordinate di trama identificato dall'operatore texkill.

Questa istruzione viene utilizzata come segue:

<dl> texkill TN  
Il mascheramento dei pixel viene eseguito come segue:  
if (i componenti x, y, z di TextureCoordinates (fase n)<sub>UVWQ</sub>< 0)  
Annulla rendering pixel
</dl>

Per pixel shader 1 \_ 1, 1 \_ 2 e 1 \_ 3, texkill opera sul set di coordinate di trama fornito dal numero di registro di destinazione. Nella versione 1 \_ 4, tuttavia, texkill opera sui dati contenuti nel registro delle [coordinate di trama](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) o nel registro temporaneo (RN) specificato come destinazione.

Quando è abilitato il campionamento multiplo, qualsiasi effetto di anti-aliasing raggiunto sui bordi del poligono a causa del campionamento multiplo non verrà raggiunto lungo i bordi generati da texkill. Il pixel shader viene eseguito una volta per pixel.

Questo esempio viene utilizzato solo a scopo illustrativo.

Questo esempio Mostra come mascherare i pixel con coordinate di trama negative. I colori dei pixel vengono interpolati dai colori dei vertici forniti nei dati del vertice.


```
ps_1_1       // Version instruction
texkill t0   // Mask out pixel using texture coordinates from stage 0
mov r0, v0   // Move the diffuse color in v0 to r0

// The rendered output from the pixel shader is shown below
```



Le coordinate di trama variano da-0,5 a 0,5 in u e da 0,0 a 1,0 in v. Con questa istruzione i valori u negativi vengono mascherati. La prima figura seguente mostra il colore del vertice applicato al quad senza l'istruzione texkill applicata. La seconda illustrazione seguente mostra il risultato dell'istruzione texkill. I colori dei pixel dalle coordinate di trama inferiori a 0 (dove x passa da-0,5 a 0,0) sono mascherati. Il colore di sfondo (bianco) viene usato quando il colore del pixel è mascherato.

![illustrazione dell'output con il colore del vertice applicato al quad senza l'istruzione texkill](images/pstexkill-in.jpg)![illustrazione dell'output con l'istruzione texkill applicata](images/pstexkill-out.jpg)

I dati delle coordinate di trama sono dichiarati nella dichiarazione dei dati dei vertici in questo esempio.


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

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




