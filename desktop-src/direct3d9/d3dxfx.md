---
description: Opzioni per il salvataggio e la creazione di effetti.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1e5e57b5fac94c1fb24d35cf1826057b75c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123387"
---
# <a name="d3dxfx"></a><span data-ttu-id="892b5-103">D3DXFX</span><span class="sxs-lookup"><span data-stu-id="892b5-103">D3DXFX</span></span>

<span data-ttu-id="892b5-104">Opzioni per il salvataggio e la creazione di effetti.</span><span class="sxs-lookup"><span data-stu-id="892b5-104">Options for saving and creating effects.</span></span>

<span data-ttu-id="892b5-105">Le costanti nella tabella seguente sono definite in d3dx9effect. h.</span><span class="sxs-lookup"><span data-stu-id="892b5-105">The constants in the following table are defined in d3dx9effect.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="892b5-106">Flag di salvataggio e ripristino dello stato degli effetti</span><span class="sxs-lookup"><span data-stu-id="892b5-106">Effect State Save and Restore Flags</span></span></td>
<td><span data-ttu-id="892b5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="892b5-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="892b5-108">D3DXFX_DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="892b5-108">D3DXFX_DONOTSAVESTATE</span></span></td>
<td><span data-ttu-id="892b5-109">Nessun stato viene salvato quando si chiama l' <a href="id3dxeffect--begin.md"><strong>inizio</strong></a> o il ripristino quando si chiama <a href="id3dxeffect--end.md"><strong>end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="892b5-109">No state is saved when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> or restored when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="892b5-110">D3DXFX_DONOTSAVESAMPLERSTATE</span><span class="sxs-lookup"><span data-stu-id="892b5-110">D3DXFX_DONOTSAVESAMPLERSTATE</span></span></td>
<td><span data-ttu-id="892b5-111">Un stateblock Salva lo stato quando si chiama <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> e ripristina lo stato quando si chiama <a href="id3dxeffect--end.md"><strong>end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="892b5-111">A stateblock saves state when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="892b5-112">D3DXFX_DONOTSAVESHADERSTATE</span><span class="sxs-lookup"><span data-stu-id="892b5-112">D3DXFX_DONOTSAVESHADERSTATE</span></span></td>
<td><span data-ttu-id="892b5-113">Un stateblock Salva lo stato (eccetto gli shader e le costanti shader) quando si chiama l'oggetto <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> e si ripristina lo stato quando si chiama <a href="id3dxeffect--end.md"><strong>end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="892b5-113">A stateblock saves state (except shaders and shader constants) when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="892b5-114">Flag di creazione effetti</span><span class="sxs-lookup"><span data-stu-id="892b5-114">Effect Creation Flags</span></span></td>
<td><span data-ttu-id="892b5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="892b5-115">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="892b5-116">D3DXFX_NOT_CLONEABLE</span><span class="sxs-lookup"><span data-stu-id="892b5-116">D3DXFX_NOT_CLONEABLE</span></span></td>
<td><span data-ttu-id="892b5-117">L'effetto sarà non clonabile e non conterrà dati binari dello shader.</span><span class="sxs-lookup"><span data-stu-id="892b5-117">The effect will be non-cloneable and will not contain any shader binary data.</span></span> <span data-ttu-id="892b5-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> non restituirà puntatori a funzioni shader.</span><span class="sxs-lookup"><span data-stu-id="892b5-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> will not return shader function pointers.</span></span> <span data-ttu-id="892b5-119">L'impostazione di questo flag riduce l'utilizzo della memoria da parte del 50% perché elimina la necessità che il sistema degli effetti mantenga una copia degli shader in memoria.</span><span class="sxs-lookup"><span data-stu-id="892b5-119">Setting this flag reduces effect memory usage by about 50% because it eliminates the need for the effect system to keep a copy of the shaders in memory.</span></span> <span data-ttu-id="892b5-120">Questo flag viene usato da <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>e <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="892b5-120">This flag is used by <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>, and <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="892b5-121">D3DXFX_LARGEADDRESSAWARE</span><span class="sxs-lookup"><span data-stu-id="892b5-121">D3DXFX_LARGEADDRESSAWARE</span></span></td>
<td><span data-ttu-id="892b5-122">Consente l'allocazione di una risorsa effetto nello spazio degli indirizzi di uppder di un computer.</span><span class="sxs-lookup"><span data-stu-id="892b5-122">Enables the allocation of an effect resource into the uppder address space of a machine.</span></span> <span data-ttu-id="892b5-123">Una limitazione importante è che non è possibile usare stringhe e handle in modo interscambiabile.</span><span class="sxs-lookup"><span data-stu-id="892b5-123">One important limitation is that you cannot use strings and handles interchangeably.</span></span> <span data-ttu-id="892b5-124">Ad esempio, il codice seguente non funzionerà più.</span><span class="sxs-lookup"><span data-stu-id="892b5-124">For example, the following would no longer work.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="892b5-125">Al contrario, è necessario usare un metodo come [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) per archiviare l'handle del parametro, che viene quindi usato per passare le variabili all'effetto.</span><span class="sxs-lookup"><span data-stu-id="892b5-125">Instead, a method such as [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) must be used to store the handle of the parameter, which is then used to pass variables to the effect.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="892b5-126">Le costanti nella tabella seguente non sono definite per impostazione predefinita e devono essere definite dallo sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="892b5-126">The constants in the following table are not defined by default and must be defined by the developer.</span></span>



|                                |                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="892b5-127">L'effetto del preprocessore \# definisce</span><span class="sxs-lookup"><span data-stu-id="892b5-127">Effect Preprocessor \#define's</span></span> | <span data-ttu-id="892b5-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="892b5-128">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="892b5-129">\_Handle LARGEADDRESS \_ D3DXFX</span><span class="sxs-lookup"><span data-stu-id="892b5-129">D3DXFX\_LARGEADDRESS\_HANDLE</span></span>   | <span data-ttu-id="892b5-130">Definire questo valore prima di includere d3dx9. h in modo che l'applicazione non venga compilata quando si tenta di passare le stringhe nei parametri D3DXHANDLE.</span><span class="sxs-lookup"><span data-stu-id="892b5-130">Define this value before including d3dx9.h so that your application fails to compile when attempting to pass strings into D3DXHANDLE parameters.</span></span> <span data-ttu-id="892b5-131">Ciò consentirà di garantire che le informazioni valide vengano passate al runtime.</span><span class="sxs-lookup"><span data-stu-id="892b5-131">This will aid in making sure that valid information is being passed to the runtime.</span></span> |
| <span data-ttu-id="892b5-132">Flag del linker effetti</span><span class="sxs-lookup"><span data-stu-id="892b5-132">Effect Linker Flags</span></span>            | <span data-ttu-id="892b5-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="892b5-133">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="892b5-134">\_compatibile con indirizzi di grandi dimensioni \_</span><span class="sxs-lookup"><span data-stu-id="892b5-134">LARGE\_ADDRESS\_AWARE</span></span>          | <span data-ttu-id="892b5-135">Se si imposta il flag del linker \_ con un indirizzo di grandi dimensioni \_ = 1, l'applicazione può allocare risorse oltre il limite di 2 GB di indirizzi, se necessario.</span><span class="sxs-lookup"><span data-stu-id="892b5-135">Setting the linker flag LARGE\_ADDRESS\_AWARE = 1 will will allow the application to allocate resources past the 2GB address limit when needed.</span></span>                                                                                      |



 

<span data-ttu-id="892b5-136">Il sistema degli effetti usa i blocchi di stato per salvare e ripristinare lo stato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="892b5-136">The effect system uses state blocks to save and restore state automatically.</span></span> <span data-ttu-id="892b5-137">Per ulteriori informazioni sui blocchi di stato, vedere state [Blocks Save and Restore state (Direct3D 9)](state-blocks-save-and-restore-state.md).</span><span class="sxs-lookup"><span data-stu-id="892b5-137">For more information about state blocks, see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="892b5-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="892b5-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="892b5-139">Costanti effetto</span><span class="sxs-lookup"><span data-stu-id="892b5-139">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



