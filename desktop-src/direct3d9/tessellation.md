---
description: Tessellazione (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Tessellazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aedc6b435c2993e213e8a4445682725ddb4d460c146afbe420da996e3dbb887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984831"
---
# <a name="tessellation-direct3d-9"></a>Tessellazione (Direct3D 9)

## <a name="tessellator-unit"></a>Unità tessellator

L'unità a tessellatore è stata migliorata. È ora possibile usarlo per:

-   Eseguire il tessellamento adattivo di tutte le primitive di ordine superiore.
-   Cercare i valori di spostamento per vertice da una mappa di spostamento e passarli a un vertex shader.
-   Supporto della tessellazione a patch rettangolare. Viene specificato tramite una dichiarazione di vertice usando D3DDECLMETHOD \_ PARTIALU o D3DDECLMETHOD \_ PARTIALV. Se viene usata una dichiarazione di vertice contenente questi metodi per disegnare una patch di triangolo, [**IDirect3DDevice9::D rawTriPatch**](/windows/desktop/api) avrà esito negativo. Per altre informazioni sulle dichiarazioni dei vertici, vedere [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

In DirectX 8.x, ciò che è stato chiamato ORDER era effettivamente il grado. In Direct3D 9 il grado è ora specificato da [**D3DDEGREETYPE.**](./d3ddegreetype.md)


```
 // This used to be D3DORDERTYPE and D3DORDER* 
 typedef enum _D3DDEGREETYPE 
 { 
 D3DDEGREE_LINEAR = 1, 
 D3DDEGREE_QUADRATIC = 2, 
 D3DDEGREE_CUBIC = 3, 
 D3DDEGREE_QUINTIC = 5, 
 D3DDEGREE_FORCE_DWORD = 0x7fffffff, 
 } D3DDEGREETYPE; 
```



La modifica del tipo di grado ha interessato altre due strutture.


```
typedef struct _D3DRECTPATCH_INFO 
 { 
 UINT StartVertexOffsetWidth; 
 UINT StartVertexOffsetHeight; 
 UINT Width; 
 UINT Height; 
 UINT Stride; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DRECTPATCH_INFO; 
```




```
 typedef struct _D3DTRIPATCH_INFO 
 { 
 UINT StartVertexOffset; 
 UINT NumVertices; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DTRIPATCH_INFO; 
```



I driver devono correggere gli errori di compilazione che saranno risultati da questa modifica quando vengono compilati con le nuove intestazioni. Non è necessario modificare alcuna funzionalità.

## <a name="adaptive-tessellation"></a>Tessellazione adattiva

La tessellazione adattiva può essere applicata a primitive di ordine elevato, tra cui patch N, patch per rettangoli e patch di triangolo. Questa funzionalità è abilitata da D3DRS ENABLEADAPTIVETESSELLATION e a tessitura adattiva di una patch, in base al valore di profondità del vertice di controllo nello spazio \_ oculare.

Le coordinate z (Zi) dei vertici di controllo (Vi), che vengono trasformate nello spazio oculare (Zieye) eseguendo un prodotto punto con un vettore a 4, vengono usate come valori di profondità. Il vettore 4D (Mdm) viene specificato dall'applicazione usando quattro stati di rendering (D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS Z e \_ D3DRS \_ ADAPTIVETESS \_ W). Questo vettore a 4 potrebbe essere la terza colonna delle matrici di mondo e visualizzazione concatenate. Può anche essere usato per applicare una scala a Zieye.

Si presuppone che la funzione per calcolare un livello a tessellazione Ti da Zieye sia (MaxTessellationLevel/Zieye), il che significa che MaxTessellationLevel è il livello a tessellazione in Z = 1 nello spazio oculare. MaxTessellationLevel è uguale a un valore impostato da [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) per le patch N e, per le patch RT, è uguale a pNumSegs. Il livello a tessellazione viene quindi impostato su valori, definiti dai due stati di rendering aggiuntivi D3DRS \_ MINTESSELLATIONLEVEL e D3DRS MAXTESSELLATIONLEVEL, che definiscono i livelli minimo e massimo a cui \_ accollarsi. La media dei ti per ogni vertice lungo un bordo di una patch viene mediata per ottenere un livello a tessellazione per tale bordo. L'algoritmo per il calcolo di Ti per le patch dei rettangoli, le patch di triangolo e le patch N differisce in base ai vertici di controllo usati per calcolare il livello a scorrimento.

Per le patch dei rettangoli con base B spline, vengono usati i quattro vertici di controllo più esterni. Ad esempio, con ordine CUBIC D3DORDER: i vertici \_ (1,1) e (1,width-2) vengono usati con pNumSegs \[ 0, i \] vertici (1,width-2) e (height-2,height-2) vengono usati con pNumSeg \[ \] 1, i vertici (height-2,width-2) e (1,width-2) vengono usati con pNumSegs 2 e i \[ vertici \] (2,1) e (1,1) vengono usati con pNumSegs \[ 3 \] .

Per le patch triangolare, vengono usati i vertici delle patch degli angoli. Con l'ordine D3DORDER CUBIC: i vertici (0) e (9) vengono usati con \_ pNumSegs 0, i vertici (9) e (6) vengono usati con \[ \] pNumSegs 1 e i vertici (6) e (0) vengono usati con \[ \] pNumSegs \[ 3 \] .

Per le patch N vengono usati i vertici del triangolo.

Per le patch di rettangolo e triangolo con una base di Bézier, vengono usati i vertici di controllo degli angoli.

Controllo della frequenza a tessitori per vertice. Un'applicazione può facoltativamente fornire un singolo valore positivo a virgola mobile per vertice, che può essere usato per controllare la frequenza di tessellazione. Viene fornito utilizzando il TESSFACTOR D3DDECLUSAGE, per il quale l'indice di utilizzo deve essere 0 e il tipo di input deve essere \_ D3DDECLTYPE \_ FLOAT1. Questo valore viene moltiplicato per il livello a tessellazione per vertice.

### <a name="math"></a>Math

Il livello a tessellazione (Te) per un bordo e, rappresentato da due vertici di controllo (Ve1, Ve2), viene calcolato come illustrato di seguito:


```
Vertex Vi: (Xi, Yi, Zi, TFactori (optional)). 
Ze1eye = Ve1 . Mdm 
Ze2eye = Ve2 . Mdm 
Te1 = MaxTessellationLevel * TFactore1 / Ze1eye 
Te2 = MaxTessellationLevel * TFactore2 / Ze2eye 
Te = ( Te1 + Te2 ) / 2; 
if Te > D3DRS_MAXTESSELLATIONLEVEL || Te < 0, then Te = D3DRS_MAXTESSELLATIONLEVEL 
if Te < D3DRS_MINTESSELLATIONLEVEL, then Te = D3DRS_MINTESSELLATIONLEVEL 
```



Quando D3DRS ENABLEADAPTIVETESSELLATION è TRUE, le primitive di triangolo (elenchi di triangoli, ventole, strisce) vengono disegnate come \_ N patch, [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) ha un valore impostato minore di 1,0. 

### <a name="api-changes"></a>Modifiche all'API

Nuovi stati di rendering:


```
 D3DRS_ENABLEADAPTIVETESSELLATION // BOOL 
 D3DRS_MAXTESSELLATIONLEVEL       // Float 
 D3DRS_MINTESSELLATIONLEVEL       // Float 
 D3DRS_ADAPTIVETESS_X             // Float 
 D3DRS_ADAPTIVETESS_Y             // Float 
 D3DRS_ADAPTIVETESS_Z             // Float 
 D3DRS_ADAPTIVETESS_W             // Float 
 
 // D3DRS_MINTESSELLATIONLEVEL and D3DRS_MAXTESSELLATIONLEVEL 
 // cannot be less than 1 
```



E i relativi valori predefiniti:


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



Nuovi limiti hardware:


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex Pipeline](vertex-pipeline.md)
</dt> </dl>

 

 
