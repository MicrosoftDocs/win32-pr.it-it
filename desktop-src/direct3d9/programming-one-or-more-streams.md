---
description: Questa sezione descrive gli shader che è possibile usare per il modello di flusso programmabile.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programmazione di uno o più flussi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304065"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a>Programmazione di uno o più flussi (Direct3D 9)

Questa sezione descrive gli shader che è possibile usare per il modello di flusso programmabile.

## <a name="using-streams"></a>Uso di flussi

DirectX 8 ha introdotto la nozione di flusso per associare i dati ai registri di input per l'uso da parte degli shader. Un flusso è una matrice uniforme di dati del componente, in cui ogni componente è costituito da uno o più elementi che rappresentano una singola entità, ad esempio posizione, normale, colore e così via. I flussi consentono ai chip grafici di eseguire un accesso diretto alla memoria da più buffer dei vertici in parallelo e forniscono anche un mapping più naturale dai dati dell'applicazione. Abilitano anche Trivial multitexture rispetto a MultiPASS. Si pensi a questo:

-   Un vertice è costituito da n flussi.
-   Un flusso è costituito da elementi m.
-   Un elemento è \[ position, color, Normal e coordinata di trama \] .

Il metodo [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) associa un buffer vertex a un flusso di dati del dispositivo, creando un'associazione tra i dati dei vertici e una delle diverse porte del flusso di dati che alimentano le funzioni di elaborazione primitive. I riferimenti effettivi ai dati del flusso non si verificano fino a quando non viene chiamato un metodo di disegno, ad esempio [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

Il mapping degli elementi del vertice di input ai registri di input dei vertici per i vertex shader programmabili è definito nella dichiarazione dello shader, ma gli elementi del vertice di input non hanno una semantica specifica relativa all'utilizzo. L'interpretazione degli elementi del vertice di input viene programmata usando le istruzioni dello shader. La funzione vertex shader viene definita da una matrice di istruzioni applicate a ogni vertice. I registri di output dei vertici vengono scritti in modo esplicito in, usando le istruzioni nella funzione shader.

Per questa discussione, tuttavia, è preoccupante del mapping semantico degli elementi ai registri e più riguarda il motivo per l'uso dei flussi e il problema che viene risolto usando i flussi. Il vantaggio principale dei flussi consiste nel fatto che i dati dei vertici vengono rimossi in precedenza dai costi associati al multitexturing. Prima dei flussi, un utente doveva duplicare i set di dati dei vertici per gestire il case singolo e multitrama senza elementi dati inutilizzati o includere elementi di dati che sarebbero stati inutilizzati tranne nel caso di multitexture.

Di seguito è riportato un esempio di utilizzo di due set di dati dei vertici, uno per la trama singola e uno per la multitexturing.


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



In alternativa, era necessario disporre di un singolo elemento Vertex che conteneva entrambi i set di coordinate di trama.


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



Con questi dati dei vertici, solo una copia dei dati di posizione e colore viene mantenuta in memoria, a scapito del fatto di portare entrambi i set di coordinate di trama per il rendering anche nel caso di una singola trama.

Ora che il compromesso è chiaro, i flussi forniscono una soluzione elegante a questo dilemma. Di seguito è riportato un set di definizioni dei vertici per supportare tre flussi: uno con la posizione e il colore, uno con il primo set di coordinate di trama e uno con il secondo set di coordinate di trama.


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



La dichiarazione del vertice sarà la seguente:


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



A questo punto, creare l'oggetto dichiarazione vertici e impostarlo come illustrato di seguito:


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a>Esempi di combinazioni

### <a name="one-stream-diffuse-color"></a>Colore diffuso di un flusso

La dichiarazione dei vertici e le impostazioni di flusso per il rendering dei colori diffusi sono simili alle seguenti:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a>Due flussi con colore e trama

La dichiarazione dei vertici e le impostazioni di flusso per il rendering a trama singola avranno un aspetto simile al seguente:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a>Due flussi con colore e due trame

La dichiarazione dei vertici e le impostazioni di flusso per il rendering a più trame a due trame avranno un aspetto simile al seguente:


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



In ogni caso, è sufficiente la chiamata [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



Questo mostra la flessibilità dei flussi per la risoluzione del problema di duplicazione dei dati/trasmissione di dati ridondanti sul bus (ovvero, di sprecare larghezza di banda).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione vertici](vertex-declaration.md)
</dt> </dl>

 

 
