---
description: Questa sezione descrive gli shader che possono essere usati per il modello di flusso programmabile.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programmazione di uno o più Flussi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92440abfb6e343bdd3440f5608d6446c0390b1271e5c4c6686a3a46e578476ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118600"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a>Programmazione di uno o più Flussi (Direct3D 9)

Questa sezione descrive gli shader che possono essere usati per il modello di flusso programmabile.

## <a name="using-streams"></a>Uso di Flussi

DirectX 8 ha introdotto la nozione di flusso per associare i dati ai registri di input per l'uso da parte degli shader. Un flusso è una matrice uniforme di dati del componente, in cui ogni componente è costituito da uno o più elementi che rappresentano una singola entità, ad esempio posizione, normale, colore e così via. Flussi chip grafici per eseguire un accesso diretto alla memoria da più vertex buffer in parallelo e fornire anche un mapping più naturale dai dati dell'applicazione. Abilitano anche il multitexture semplice e il multipass. Si pensi al modo seguente:

-   Un vertice è costituito da n flussi.
-   Un flusso è costituito da elementi m.
-   Un elemento è \[ position, color, normal, texture coordinate \] .

Il metodo [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) associa un vertex buffer a un flusso di dati del dispositivo, creando un'associazione tra i dati dei vertici e una delle diverse porte del flusso di dati che alimentano le funzioni di elaborazione primitive. I riferimenti effettivi ai dati del flusso non si verificano fino a quando non viene chiamato un metodo di disegno, ad esempio [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).

Il mapping degli elementi dei vertici di input ai registri di input dei vertici per i vertex shader programmabili è definito nella dichiarazione dello shader, ma gli elementi dei vertici di input non hanno una semantica specifica sul loro uso. L'interpretazione degli elementi dei vertici di input viene programmata usando le istruzioni dello shader. La funzione vertex shader è definita da una matrice di istruzioni applicate a ogni vertice. I registri di output dei vertici vengono scritti in modo esplicito in , usando le istruzioni nella funzione shader.

Per questa discussione, tuttavia, è necessario preoccuparsi meno del mapping semantico degli elementi ai registri e del motivo dell'uso dei flussi e del problema risolto usando i flussi. Il vantaggio principale dei flussi è che rimuovono i costi dei dati dei vertici precedentemente associati al multitexturing. Prima dei flussi, un utente doveva duplicare i set di dati dei vertici per gestire il caso singolo e multitexture senza elementi di dati inutilizzati o portare elementi di dati che sarebbero stati inutilizzati tranne che nel caso multitexture.

Di seguito è riportato un esempio di uso di due set di dati dei vertici, uno per la trama singola e uno per il multitexturing.


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



L'alternativa consisteva nel disporre di un singolo elemento vertice che conteneva entrambi i set di coordinate di trama.


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



Con questi dati sui vertici, solo una copia dei dati relativi alla posizione e al colore viene trasportata in memoria, a spese del trasporto di entrambi i set di coordinate di trama per il rendering anche nel caso di trama singola.

Ora che il compromesso è chiaro, i flussi forniscono una correzione elegante a questo problema. Ecco un set di definizioni dei vertici per supportare tre flussi: uno con posizione e colore, uno con il primo set di coordinate di trama e uno con il secondo set di coordinate di trama.


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



Creare ora l'oggetto dichiarazione vertice e impostarlo come illustrato:


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a>Esempi di combinazioni

### <a name="one-stream-diffuse-color"></a>Un colore diffuso del flusso

La dichiarazione dei vertici e le impostazioni del flusso per il rendering a colori diffuso sono simili alle seguenti:


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



### <a name="two-streams-with-color-and-texture"></a>Due Flussi con colore e trama

La dichiarazione dei vertici e le impostazioni del flusso per il rendering a trama singola sono simili alle seguenti:


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



### <a name="two-streams-with-color-and-two-textures"></a>Due Flussi con colore e due trame

La dichiarazione dei vertici e le impostazioni del flusso per il rendering a più trame a due trame sono simili alle seguenti:The vertex declaration and stream settings for two-texture multi-texture rendering would look like this:


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



In ogni caso, è sufficiente la chiamata [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) seguente.


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



Ciò mostra la flessibilità dei flussi nella risoluzione del problema della duplicazione dei dati o della trasmissione dei dati ridondanti attraverso il bus, ovvero dello spremimento della larghezza di banda.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dichiarazione dei vertici](vertex-declaration.md)
</dt> </dl>

 

 
