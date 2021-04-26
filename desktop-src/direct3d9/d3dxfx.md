---
description: Opzioni per il salvataggio e la creazione di effetti.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9077c8c7e3da479dd8963484bc289b84093ac0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995078"
---
# <a name="d3dxfx"></a><span data-ttu-id="fa88e-103">D3DXFX</span><span class="sxs-lookup"><span data-stu-id="fa88e-103">D3DXFX</span></span>

<span data-ttu-id="fa88e-104">Opzioni per il salvataggio e la creazione di effetti.</span><span class="sxs-lookup"><span data-stu-id="fa88e-104">Options for saving and creating effects.</span></span>

<span data-ttu-id="fa88e-105">Le costanti nella tabella seguente sono definite in d3dx9effect.h.</span><span class="sxs-lookup"><span data-stu-id="fa88e-105">The constants in the following table are defined in d3dx9effect.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa88e-106">Flag di salvataggio e ripristino dello stato dell'effetto</span><span class="sxs-lookup"><span data-stu-id="fa88e-106">Effect State Save and Restore Flags</span></span></td>
<td><span data-ttu-id="fa88e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa88e-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa88e-108">D3DXFX_DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="fa88e-108">D3DXFX_DONOTSAVESTATE</span></span></td>
<td><span data-ttu-id="fa88e-109">Non viene salvato alcuno stato quando si chiama <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> o restored quando si chiama <a href="id3dxeffect--end.md"><strong>End.</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa88e-109">No state is saved when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> or restored when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa88e-110">D3DXFX_DONOTSAVESAMPLERSTATE</span><span class="sxs-lookup"><span data-stu-id="fa88e-110">D3DXFX_DONOTSAVESAMPLERSTATE</span></span></td>
<td><span data-ttu-id="fa88e-111">Un blocco di stato salva lo stato quando si chiama <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> e ripristina lo stato quando si chiama <a href="id3dxeffect--end.md"><strong>End.</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa88e-111">A stateblock saves state when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa88e-112">D3DXFX_DONOTSAVESHADERSTATE</span><span class="sxs-lookup"><span data-stu-id="fa88e-112">D3DXFX_DONOTSAVESHADERSTATE</span></span></td>
<td><span data-ttu-id="fa88e-113">Un blocco di stato salva lo stato (ad eccezione degli shader e delle costanti shader) quando chiama <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> e ripristina lo stato quando si chiama <a href="id3dxeffect--end.md"><strong>End.</strong></a></span><span class="sxs-lookup"><span data-stu-id="fa88e-113">A stateblock saves state (except shaders and shader constants) when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa88e-114">Flag di creazione degli effetti</span><span class="sxs-lookup"><span data-stu-id="fa88e-114">Effect Creation Flags</span></span></td>
<td><span data-ttu-id="fa88e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa88e-115">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa88e-116">D3DXFX_NOT_CLONEABLE</span><span class="sxs-lookup"><span data-stu-id="fa88e-116">D3DXFX_NOT_CLONEABLE</span></span></td>
<td><span data-ttu-id="fa88e-117">L'effetto non sarà clonabile e non conterrà dati binari dello shader.</span><span class="sxs-lookup"><span data-stu-id="fa88e-117">The effect will be non-cloneable and will not contain any shader binary data.</span></span> <span data-ttu-id="fa88e-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc non</strong></a> restituirà puntatori a funzione shader.</span><span class="sxs-lookup"><span data-stu-id="fa88e-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> will not return shader function pointers.</span></span> <span data-ttu-id="fa88e-119">L'impostazione di questo flag riduce l'utilizzo della memoria degli effetti di circa il 50% perché elimina la necessità che il sistema di effetti manteni una copia degli shader in memoria.</span><span class="sxs-lookup"><span data-stu-id="fa88e-119">Setting this flag reduces effect memory usage by about 50% because it eliminates the need for the effect system to keep a copy of the shaders in memory.</span></span> <span data-ttu-id="fa88e-120">Questo flag viene usato da <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>e <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="fa88e-120">This flag is used by <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>, and <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa88e-121">D3DXFX_LARGEADDRESSAWARE</span><span class="sxs-lookup"><span data-stu-id="fa88e-121">D3DXFX_LARGEADDRESSAWARE</span></span></td>
<td><span data-ttu-id="fa88e-122">Abilita l'allocazione di una risorsa effetto nello spazio degli indirizzi uppder di un computer.</span><span class="sxs-lookup"><span data-stu-id="fa88e-122">Enables the allocation of an effect resource into the uppder address space of a machine.</span></span> <span data-ttu-id="fa88e-123">Una limitazione importante è che non è possibile usare stringhe e gestire in modo intercambiabile.</span><span class="sxs-lookup"><span data-stu-id="fa88e-123">One important limitation is that you cannot use strings and handles interchangeably.</span></span> <span data-ttu-id="fa88e-124">Ad esempio, gli elementi seguenti non funzionano più.</span><span class="sxs-lookup"><span data-stu-id="fa88e-124">For example, the following would no longer work.</span></span> <span data-codelanguage=""></span>
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

<span data-ttu-id="fa88e-125">È invece necessario usare un metodo come [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) per archiviare l'handle del parametro, che viene quindi usato per passare variabili all'effetto.</span><span class="sxs-lookup"><span data-stu-id="fa88e-125">Instead, a method such as [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) must be used to store the handle of the parameter, which is then used to pass variables to the effect.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fa88e-126">Le costanti nella tabella seguente non sono definite per impostazione predefinita e devono essere definite dallo sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="fa88e-126">The constants in the following table are not defined by default and must be defined by the developer.</span></span>



| <span data-ttu-id="fa88e-127">Definizione del \# preprocessore degli effetti</span><span class="sxs-lookup"><span data-stu-id="fa88e-127">Effect Preprocessor \#define's</span></span> | <span data-ttu-id="fa88e-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa88e-128">Description</span></span>                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa88e-129">D3DXFX \_ LARGEADDRESS \_ HANDLE</span><span class="sxs-lookup"><span data-stu-id="fa88e-129">D3DXFX\_LARGEADDRESS\_HANDLE</span></span>   | <span data-ttu-id="fa88e-130">Definire questo valore prima di includere d3dx9.h in modo che l'applicazione non venga compilata quando si tenta di passare stringhe nei parametri D3DXHANDLE.</span><span class="sxs-lookup"><span data-stu-id="fa88e-130">Define this value before including d3dx9.h so that your application fails to compile when attempting to pass strings into D3DXHANDLE parameters.</span></span> <span data-ttu-id="fa88e-131">Ciò consente di assicurarsi che le informazioni valide vengano passate al runtime.</span><span class="sxs-lookup"><span data-stu-id="fa88e-131">This will aid in making sure that valid information is being passed to the runtime.</span></span> |
| <span data-ttu-id="fa88e-132">Flag del linker degli effetti</span><span class="sxs-lookup"><span data-stu-id="fa88e-132">Effect Linker Flags</span></span>            | <span data-ttu-id="fa88e-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa88e-133">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="fa88e-134">INFORMAZIONI \_ SU INDIRIZZI DI GRANDI \_ DIMENSIONI</span><span class="sxs-lookup"><span data-stu-id="fa88e-134">LARGE\_ADDRESS\_AWARE</span></span>          | <span data-ttu-id="fa88e-135">L'impostazione del flag del linker LARGE ADDRESS AWARE = 1 consentirà all'applicazione di allocare risorse oltre il limite \_ \_ di indirizzi di 2 GB quando necessario.</span><span class="sxs-lookup"><span data-stu-id="fa88e-135">Setting the linker flag LARGE\_ADDRESS\_AWARE = 1 will will allow the application to allocate resources past the 2GB address limit when needed.</span></span>                                                                                      |



 

<span data-ttu-id="fa88e-136">Il sistema di effetti usa blocchi di stato per salvare e ripristinare automaticamente lo stato.</span><span class="sxs-lookup"><span data-stu-id="fa88e-136">The effect system uses state blocks to save and restore state automatically.</span></span> <span data-ttu-id="fa88e-137">Per altre informazioni sui blocchi di stato, vedere [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span><span class="sxs-lookup"><span data-stu-id="fa88e-137">For more information about state blocks, see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa88e-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa88e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa88e-139">Costanti degli effetti</span><span class="sxs-lookup"><span data-stu-id="fa88e-139">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



