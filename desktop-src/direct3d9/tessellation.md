---
description: Suddivisione a mosaico (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Suddivisione a mosaico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82378caac1218158ffc1834c9a9b56fb8cbd250e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746935"
---
# <a name="tessellation-direct3d-9"></a>Suddivisione a mosaico (Direct3D 9)

## <a name="tessellator-unit"></a>Unità mosaico

L'unità mosaico è stata migliorata. È ora possibile usarlo per:

-   Esegue lo schema a mosaico adattivo di tutte le primitive di ordine superiore.
-   Cercare i valori di spostamento per vertice da una mappa di spostamento e passarli a un vertex shader.
-   Supporto dello schema a mosaico della patch. Questa operazione viene specificata tramite una dichiarazione vertex con D3DDECLMETHOD \_ partial o D3DDECLMETHOD \_ PARTIALV. Se viene usata una dichiarazione di vertice contenente questi metodi per creare una patch del triangolo, [**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api) avrà esito negativo. Per ulteriori informazioni sulle dichiarazioni dei vertici, vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

In DirectX 8. x, ciò che era stato chiamato ORDER era effettivamente il grado. In Direct3D 9 il grado è ora specificato da [**D3DDEGREETYPE**](./d3ddegreetype.md).


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



La modifica di tipo Degree ha interessato altre due strutture.


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



I driver devono correggere gli errori di compilazione che derivano da questa modifica quando vengono compilati con le nuove intestazioni. Non è necessario modificare alcuna funzionalità.

## <a name="adaptive-tessellation"></a>Mosaico adattivo

Lo schema a mosaico adattivo può essere applicato a primitive ad ordine elevato, tra cui N-patch, patch rettangolari e patch di triangolo. Questa funzionalità è abilitata dal D3DRS \_ ENABLEADAPTIVETESSELLATION e in modo adattivo tessellates una patch, in base al valore di profondità del vertice del controllo nello spazio degli occhi.

Le coordinate z (Zi) dei vertici di controllo (vi), che vengono trasformate nello spazio degli occhi (Zieye) eseguendo un prodotto punto con un vettore di 4, vengono usate come valori di profondità. Il vettore 4D (MDM) viene specificato dall'applicazione usando quattro stati di rendering (D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z e D3DRS \_ ADAPTIVETESS \_ W). Questo vettore di 4 può essere la terza colonna delle matrici del mondo concatenato e della vista. Potrebbe anche essere usato per applicare una scala a Zieye.

Si presuppone che la funzione per calcolare un livello a mosaico da Zieye sia (MaxTessellationLevel/Zieye), il che significa che il MaxTessellationLevel è il livello a mosaico a Z = 1 nello spazio degli occhi. MaxTessellationLevel è uguale a un valore impostato da [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) per N-patches e, per RT-patches, è uguale a pNumSegs. Il livello a mosaico viene quindi fissato ai valori, definiti dai due stati di rendering aggiuntivi D3DRS \_ MINTESSELLATIONLEVEL e D3DRS \_ MAXTESSELLATIONLEVEL, che definiscono i livelli minimo e massimo di mosaico da bloccare. Per ogni vertice lungo un bordo di una patch viene calcolata la media per ottenere un livello di mosaico per il bordo. L'algoritmo per il calcolo di ti per le patch rettangolari, le patch del triangolo e N-patch è diverso nei vertici di controllo usati per calcolare il livello di mosaico.

Per le patch rettangolari con una spline B-base, vengono usati i quattro vertici di controllo più esterni. Ad esempio, con D3DORDER \_ Cubic Order: vertici (1, 1) e (1, Width-2) vengono usati con pNumSegs \[ 0 \] , i vertici (1, Width-2) e (Height-2, Height-2) vengono usati con pNumSegs \[ 1 \] , i vertici (Height-2, Width-2) e (1, Width-2) vengono usati con pNumSegs 2 e i \[ \] vertici (2, 1) e (1, 1) vengono usati con pNumSegs \[ 3 \] .

Per le patch del triangolo, vengono usati i vertici delle patch d'angolo. Con l' \_ ordine cubico D3DORDER: i vertici (0) e (9) vengono usati con pNumSegs \[ 0 \] , i vertici (9) e (6) vengono usati con pNumSegs \[ 1 \] e i vertici (6) e (0) vengono usati con pNumSegs \[ 3 \] .

Per N-patch vengono usati i vertici del triangolo.

Per le patch rettangolo e triangolo con una base di Bezier, vengono usati i vertici di controllo angolo.

Controllo della frequenza a mosaico per vertice. Un'applicazione può facoltativamente fornire un singolo valore a virgola mobile positivo per vertice, che può essere usato per controllare la frequenza dello schema a mosaico. Viene fornito tramite il TESSFACTOR D3DDECLUSAGE \_ , per il quale l'indice di utilizzo deve essere 0 e il tipo di input deve essere D3DDECLTYPE \_ FLOAT1. Viene moltiplicato per il livello a mosaico per ogni vertice.

### <a name="math"></a>Math

Il livello a mosaico (te) per un bordo e, rappresentato da due vertici di controllo (VE1, VE2), viene calcolato come illustrato di seguito:


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



Quando D3DRS \_ ENABLEADAPTIVETESSELLATION è **true**, le primitive triangolari (elenchi di triangolo, fan, strip) vengono disegnate come N-patch, [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) ha un valore impostato inferiore a 1,0.

### <a name="api-changes"></a>Modifiche API

Nuovi Stati di rendering:


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



Nuovi tappi hardware:


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline Vertex](vertex-pipeline.md)
</dt> </dl>

 

 
