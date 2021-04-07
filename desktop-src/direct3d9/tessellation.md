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
# <a name="tessellation-direct3d-9"></a><span data-ttu-id="c904a-103">Suddivisione a mosaico (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c904a-103">Tessellation (Direct3D 9)</span></span>

## <a name="tessellator-unit"></a><span data-ttu-id="c904a-104">Unità mosaico</span><span class="sxs-lookup"><span data-stu-id="c904a-104">Tessellator Unit</span></span>

<span data-ttu-id="c904a-105">L'unità mosaico è stata migliorata.</span><span class="sxs-lookup"><span data-stu-id="c904a-105">The tessellator unit has been enhanced.</span></span> <span data-ttu-id="c904a-106">È ora possibile usarlo per:</span><span class="sxs-lookup"><span data-stu-id="c904a-106">You can now use it to:</span></span>

-   <span data-ttu-id="c904a-107">Esegue lo schema a mosaico adattivo di tutte le primitive di ordine superiore.</span><span class="sxs-lookup"><span data-stu-id="c904a-107">Perform adaptive tessellation of all higher-order primitives.</span></span>
-   <span data-ttu-id="c904a-108">Cercare i valori di spostamento per vertice da una mappa di spostamento e passarli a un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="c904a-108">Look up per-vertex displacement values from a displacement map and pass them on to a vertex shader.</span></span>
-   <span data-ttu-id="c904a-109">Supporto dello schema a mosaico della patch.</span><span class="sxs-lookup"><span data-stu-id="c904a-109">Support rectangle-patch tessellation.</span></span> <span data-ttu-id="c904a-110">Questa operazione viene specificata tramite una dichiarazione vertex con D3DDECLMETHOD \_ partial o D3DDECLMETHOD \_ PARTIALV.</span><span class="sxs-lookup"><span data-stu-id="c904a-110">This is specified through a vertex declaration using D3DDECLMETHOD\_PARTIALU or D3DDECLMETHOD\_PARTIALV.</span></span> <span data-ttu-id="c904a-111">Se viene usata una dichiarazione di vertice contenente questi metodi per creare una patch del triangolo, [**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="c904a-111">If a vertex declaration containing these methods is used to draw a triangle patch, [**IDirect3DDevice9::DrawTriPatch**](/windows/desktop/api) will fail.</span></span> <span data-ttu-id="c904a-112">Per ulteriori informazioni sulle dichiarazioni dei vertici, vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="c904a-112">For more information about vertex declarations, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="c904a-113">In DirectX 8. x, ciò che era stato chiamato ORDER era effettivamente il grado.</span><span class="sxs-lookup"><span data-stu-id="c904a-113">In DirectX 8.x, what was called ORDER was really the degree.</span></span> <span data-ttu-id="c904a-114">In Direct3D 9 il grado è ora specificato da [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="c904a-114">In Direct3D 9, the degree is now specified by [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>


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



<span data-ttu-id="c904a-115">La modifica di tipo Degree ha interessato altre due strutture.</span><span class="sxs-lookup"><span data-stu-id="c904a-115">The change in degree type affected two other structures.</span></span>


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



<span data-ttu-id="c904a-116">I driver devono correggere gli errori di compilazione che derivano da questa modifica quando vengono compilati con le nuove intestazioni.</span><span class="sxs-lookup"><span data-stu-id="c904a-116">Drivers need to fix compilation errors that will result from this change when they compile with the new headers.</span></span> <span data-ttu-id="c904a-117">Non è necessario modificare alcuna funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c904a-117">No functionality has to be changed.</span></span>

## <a name="adaptive-tessellation"></a><span data-ttu-id="c904a-118">Mosaico adattivo</span><span class="sxs-lookup"><span data-stu-id="c904a-118">Adaptive Tessellation</span></span>

<span data-ttu-id="c904a-119">Lo schema a mosaico adattivo può essere applicato a primitive ad ordine elevato, tra cui N-patch, patch rettangolari e patch di triangolo.</span><span class="sxs-lookup"><span data-stu-id="c904a-119">Adaptive tessellation can be applied to high-order primitives including N-patches, rectangle patches, and triangle patches.</span></span> <span data-ttu-id="c904a-120">Questa funzionalità è abilitata dal D3DRS \_ ENABLEADAPTIVETESSELLATION e in modo adattivo tessellates una patch, in base al valore di profondità del vertice del controllo nello spazio degli occhi.</span><span class="sxs-lookup"><span data-stu-id="c904a-120">This feature is enabled by the D3DRS\_ENABLEADAPTIVETESSELLATION and adaptively tessellates a patch, based on the depth value of the control vertex in eye space.</span></span>

<span data-ttu-id="c904a-121">Le coordinate z (Zi) dei vertici di controllo (vi), che vengono trasformate nello spazio degli occhi (Zieye) eseguendo un prodotto punto con un vettore di 4, vengono usate come valori di profondità.</span><span class="sxs-lookup"><span data-stu-id="c904a-121">The z-coordinates (Zi) of control vertices (Vi), which are transformed into eye space (Zieye) by performing a dot product with a 4-vector, are used as the depth values.</span></span> <span data-ttu-id="c904a-122">Il vettore 4D (MDM) viene specificato dall'applicazione usando quattro stati di rendering (D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z e D3DRS \_ ADAPTIVETESS \_ W).</span><span class="sxs-lookup"><span data-stu-id="c904a-122">The 4D vector (Mdm) is specified by the application using four render states (D3DRS\_ADAPTIVETESS\_X, D3DRS\_ADAPTIVETESS\_Y, D3DRS\_ADAPTIVETESS\_Z, and D3DRS\_ADAPTIVETESS\_W).</span></span> <span data-ttu-id="c904a-123">Questo vettore di 4 può essere la terza colonna delle matrici del mondo concatenato e della vista.</span><span class="sxs-lookup"><span data-stu-id="c904a-123">This 4-vector could be the third column of the concatenated world and view matrices.</span></span> <span data-ttu-id="c904a-124">Potrebbe anche essere usato per applicare una scala a Zieye.</span><span class="sxs-lookup"><span data-stu-id="c904a-124">It also could be used to apply a scale to Zieye.</span></span>

<span data-ttu-id="c904a-125">Si presuppone che la funzione per calcolare un livello a mosaico da Zieye sia (MaxTessellationLevel/Zieye), il che significa che il MaxTessellationLevel è il livello a mosaico a Z = 1 nello spazio degli occhi.</span><span class="sxs-lookup"><span data-stu-id="c904a-125">The function to compute a tessellation level Ti from Zieye is assumed to be (MaxTessellationLevel/Zieye), which means that the MaxTessellationLevel is the tessellation level at Z = 1 in eye space.</span></span> <span data-ttu-id="c904a-126">MaxTessellationLevel è uguale a un valore impostato da [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) per N-patches e, per RT-patches, è uguale a pNumSegs.</span><span class="sxs-lookup"><span data-stu-id="c904a-126">The MaxTessellationLevel is equal to a value set by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) for N-patches and, for RT-patches, it is equal to pNumSegs.</span></span> <span data-ttu-id="c904a-127">Il livello a mosaico viene quindi fissato ai valori, definiti dai due stati di rendering aggiuntivi D3DRS \_ MINTESSELLATIONLEVEL e D3DRS \_ MAXTESSELLATIONLEVEL, che definiscono i livelli minimo e massimo di mosaico da bloccare.</span><span class="sxs-lookup"><span data-stu-id="c904a-127">The tessellation level is then clamped to values, defined by the two additional render states D3DRS\_MINTESSELLATIONLEVEL and D3DRS\_MAXTESSELLATIONLEVEL, which define the minimum and maximum tessellation levels to be clamped to.</span></span> <span data-ttu-id="c904a-128">Per ogni vertice lungo un bordo di una patch viene calcolata la media per ottenere un livello di mosaico per il bordo.</span><span class="sxs-lookup"><span data-stu-id="c904a-128">The Ti's for each vertex along an edge of a patch are averaged to obtain a tessellation level for that edge.</span></span> <span data-ttu-id="c904a-129">L'algoritmo per il calcolo di ti per le patch rettangolari, le patch del triangolo e N-patch è diverso nei vertici di controllo usati per calcolare il livello di mosaico.</span><span class="sxs-lookup"><span data-stu-id="c904a-129">The algorithm for computing Ti for rectangle patches, triangle patches, and N-patches differs in what control vertices are used to compute the tessellation level.</span></span>

<span data-ttu-id="c904a-130">Per le patch rettangolari con una spline B-base, vengono usati i quattro vertici di controllo più esterni.</span><span class="sxs-lookup"><span data-stu-id="c904a-130">For the rectangle patches with a B-spline basis, the four outermost control vertices are used.</span></span> <span data-ttu-id="c904a-131">Ad esempio, con D3DORDER \_ Cubic Order: vertici (1, 1) e (1, Width-2) vengono usati con pNumSegs \[ 0 \] , i vertici (1, Width-2) e (Height-2, Height-2) vengono usati con pNumSegs \[ 1 \] , i vertici (Height-2, Width-2) e (1, Width-2) vengono usati con pNumSegs 2 e i \[ \] vertici (2, 1) e (1, 1) vengono usati con pNumSegs \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="c904a-131">For example, with D3DORDER\_CUBIC order: vertices (1,1) and (1,width-2) are used with pNumSegs\[0\], vertices (1,width-2) and (height-2,height-2) are used with pNumSegs\[1\], vertices (height-2,width-2) and (1,width-2) are used with pNumSegs\[2\], and vertices (2,1) and (1,1) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="c904a-132">Per le patch del triangolo, vengono usati i vertici delle patch d'angolo.</span><span class="sxs-lookup"><span data-stu-id="c904a-132">For the triangle patches, the corner patch vertices are used.</span></span> <span data-ttu-id="c904a-133">Con l' \_ ordine cubico D3DORDER: i vertici (0) e (9) vengono usati con pNumSegs \[ 0 \] , i vertici (9) e (6) vengono usati con pNumSegs \[ 1 \] e i vertici (6) e (0) vengono usati con pNumSegs \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="c904a-133">With D3DORDER\_CUBIC order: vertices (0) and (9) are used with pNumSegs\[0\], vertices (9) and (6) are used with pNumSegs\[1\] and vertices (6) and (0) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="c904a-134">Per N-patch vengono usati i vertici del triangolo.</span><span class="sxs-lookup"><span data-stu-id="c904a-134">For N-patches the triangle vertices are used.</span></span>

<span data-ttu-id="c904a-135">Per le patch rettangolo e triangolo con una base di Bezier, vengono usati i vertici di controllo angolo.</span><span class="sxs-lookup"><span data-stu-id="c904a-135">For the rectangle and triangle patches with a Bezier basis, the corner-control vertices are used.</span></span>

<span data-ttu-id="c904a-136">Controllo della frequenza a mosaico per vertice.</span><span class="sxs-lookup"><span data-stu-id="c904a-136">Per-vertex tessellation rate control.</span></span> <span data-ttu-id="c904a-137">Un'applicazione può facoltativamente fornire un singolo valore a virgola mobile positivo per vertice, che può essere usato per controllare la frequenza dello schema a mosaico.</span><span class="sxs-lookup"><span data-stu-id="c904a-137">An application can optionally supply a single positive floating-point value per vertex, which can be used to control the rate of tessellation.</span></span> <span data-ttu-id="c904a-138">Viene fornito tramite il TESSFACTOR D3DDECLUSAGE \_ , per il quale l'indice di utilizzo deve essere 0 e il tipo di input deve essere D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="c904a-138">This is supplied using the D3DDECLUSAGE\_TESSFACTOR, for which usage index must be 0 and input type must be D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="c904a-139">Viene moltiplicato per il livello a mosaico per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="c904a-139">This is multiplied to the per-vertex tessellation level.</span></span>

### <a name="math"></a><span data-ttu-id="c904a-140">Math</span><span class="sxs-lookup"><span data-stu-id="c904a-140">Math</span></span>

<span data-ttu-id="c904a-141">Il livello a mosaico (te) per un bordo e, rappresentato da due vertici di controllo (VE1, VE2), viene calcolato come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c904a-141">The tessellation level (Te) for an edge e, represented by two control vertices (Ve1, Ve2), is computed as shown below :</span></span>


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



<span data-ttu-id="c904a-142">Quando D3DRS \_ ENABLEADAPTIVETESSELLATION è **true**, le primitive triangolari (elenchi di triangolo, fan, strip) vengono disegnate come N-patch, [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) ha un valore impostato inferiore a 1,0.</span><span class="sxs-lookup"><span data-stu-id="c904a-142">When D3DRS\_ENABLEADAPTIVETESSELLATION is **TRUE**, triangle primitives (triangle lists, fans, strips) are drawn as N-patches, [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) has set value less than 1.0.</span></span>

### <a name="api-changes"></a><span data-ttu-id="c904a-143">Modifiche API</span><span class="sxs-lookup"><span data-stu-id="c904a-143">API Changes</span></span>

<span data-ttu-id="c904a-144">Nuovi Stati di rendering:</span><span class="sxs-lookup"><span data-stu-id="c904a-144">New render states:</span></span>


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



<span data-ttu-id="c904a-145">E i relativi valori predefiniti:</span><span class="sxs-lookup"><span data-stu-id="c904a-145">And their default values:</span></span>


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



<span data-ttu-id="c904a-146">Nuovi tappi hardware:</span><span class="sxs-lookup"><span data-stu-id="c904a-146">New hardware caps:</span></span>


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a><span data-ttu-id="c904a-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c904a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c904a-148">Pipeline Vertex</span><span class="sxs-lookup"><span data-stu-id="c904a-148">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
