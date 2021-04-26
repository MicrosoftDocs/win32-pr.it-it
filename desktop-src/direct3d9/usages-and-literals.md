---
description: L'utilizzo è simile all'ambito di un parametro, perché definisce l'ambito in cui il parametro è valido.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Utilizzi e valori letterali (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62dc1d7b40e66aaa6499dd2aa00c37d4564df2ab
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998538"
---
# <a name="usages-and-literals-direct3d-9"></a><span data-ttu-id="b6241-103">Utilizzi e valori letterali (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b6241-103">Usages and Literals (Direct3D 9)</span></span>

<span data-ttu-id="b6241-104">L'utilizzo è simile all'ambito di un parametro, perché definisce l'ambito in cui il parametro è valido.</span><span class="sxs-lookup"><span data-stu-id="b6241-104">Usage is similar to a parameter's scope, because it defines the scope in which the parameter is valid.</span></span>



| <span data-ttu-id="b6241-105">Valore</span><span class="sxs-lookup"><span data-stu-id="b6241-105">Value</span></span>  | <span data-ttu-id="b6241-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6241-106">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6241-107">const</span><span class="sxs-lookup"><span data-stu-id="b6241-107">const</span></span>  | <span data-ttu-id="b6241-108">Il parametro sarà costante nell'ambito di tutte le funzioni.</span><span class="sxs-lookup"><span data-stu-id="b6241-108">The parameter will be constant within the scope of all functions.</span></span> <span data-ttu-id="b6241-109">Si noti che tali parametri possono comunque essere scritti in con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), perché ciò si verifica all'esterno dell'ambito di tutte le funzioni.</span><span class="sxs-lookup"><span data-stu-id="b6241-109">(Note that such parameters can still be written to with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), because this occurs outside the scope of all functions.)</span></span> |
| <span data-ttu-id="b6241-110">shared</span><span class="sxs-lookup"><span data-stu-id="b6241-110">shared</span></span> | <span data-ttu-id="b6241-111">Il parametro verrà condiviso nel pool di effetti.</span><span class="sxs-lookup"><span data-stu-id="b6241-111">The parameter will be shared in the effect pool.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="b6241-112">static</span><span class="sxs-lookup"><span data-stu-id="b6241-112">static</span></span> | <span data-ttu-id="b6241-113">Il parametro non sarà visibile all'applicazione, in altri modo non sarà possibile accedervi da [**ID3DXEffect**](id3dxeffect.md) [**o ID3DXEffectCompiler.**](id3dxeffectcompiler.md)</span><span class="sxs-lookup"><span data-stu-id="b6241-113">The parameter will be invisible to the application, that is, you cannot access them from [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>                                                                                                  |



 

<span data-ttu-id="b6241-114">Se si contrassegna un parametro come valore letterale, il relativo valore non cambierà mai.</span><span class="sxs-lookup"><span data-stu-id="b6241-114">Marking a parameter as literal indicates that its value will never change.</span></span> <span data-ttu-id="b6241-115">Ciò consente al compilatore di effetti di eseguire un'ottimizzazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="b6241-115">This enables the effect compiler to do extra optimization.</span></span>

<span data-ttu-id="b6241-116">Solo i parametri di primo livello non condivisi possono essere contrassegnati come valori letterali.</span><span class="sxs-lookup"><span data-stu-id="b6241-116">Only non-shared top-level parameters can be marked as literal.</span></span> <span data-ttu-id="b6241-117">I parametri possono essere contrassegnati come letterali solo con [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="b6241-117">Parameters can only be marked as literal with [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span> <span data-ttu-id="b6241-118">I valori letterali non possono essere impostati [**con ID3DXEffect.**](id3dxeffect.md)</span><span class="sxs-lookup"><span data-stu-id="b6241-118">Literal values cannot be set with [**ID3DXEffect**](id3dxeffect.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6241-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6241-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6241-120">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="b6241-120">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



