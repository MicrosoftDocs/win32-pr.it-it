---
description: L'utilizzo è simile all'ambito di un parametro, perché definisce l'ambito in cui il parametro è valido.
ms.assetid: 9ba10dba-626f-4cb8-8dc2-1419329b199e
title: Utilizzi e valori letterali (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ca6f010d2c1e05055fd4427b8b5f7d4ab445ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304357"
---
# <a name="usages-and-literals-direct3d-9"></a><span data-ttu-id="30557-103">Utilizzi e valori letterali (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="30557-103">Usages and Literals (Direct3D 9)</span></span>

<span data-ttu-id="30557-104">L'utilizzo è simile all'ambito di un parametro, perché definisce l'ambito in cui il parametro è valido.</span><span class="sxs-lookup"><span data-stu-id="30557-104">Usage is similar to a parameter's scope, because it defines the scope in which the parameter is valid.</span></span>



|        |                                                                                                                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30557-105">Valore</span><span class="sxs-lookup"><span data-stu-id="30557-105">Value</span></span>  | <span data-ttu-id="30557-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30557-106">Description</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="30557-107">const</span><span class="sxs-lookup"><span data-stu-id="30557-107">const</span></span>  | <span data-ttu-id="30557-108">Il parametro sarà costante nell'ambito di tutte le funzioni.</span><span class="sxs-lookup"><span data-stu-id="30557-108">The parameter will be constant within the scope of all functions.</span></span> <span data-ttu-id="30557-109">Si noti che tali parametri possono comunque essere scritti con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), perché questo errore si verifica al di fuori dell'ambito di tutte le funzioni.</span><span class="sxs-lookup"><span data-stu-id="30557-109">(Note that such parameters can still be written to with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md), because this occurs outside the scope of all functions.)</span></span> |
| <span data-ttu-id="30557-110">shared</span><span class="sxs-lookup"><span data-stu-id="30557-110">shared</span></span> | <span data-ttu-id="30557-111">Il parametro verrà condiviso nel pool di effetti.</span><span class="sxs-lookup"><span data-stu-id="30557-111">The parameter will be shared in the effect pool.</span></span>                                                                                                                                                                                                                                    |
| <span data-ttu-id="30557-112">static</span><span class="sxs-lookup"><span data-stu-id="30557-112">static</span></span> | <span data-ttu-id="30557-113">Il parametro sarà invisibile per l'applicazione, ovvero non è possibile accedervi da [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="30557-113">The parameter will be invisible to the application, that is, you cannot access them from [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>                                                                                                  |



 

<span data-ttu-id="30557-114">Contrassegnando un parametro come valore letterale viene indicato che il valore non viene mai modificato.</span><span class="sxs-lookup"><span data-stu-id="30557-114">Marking a parameter as literal indicates that its value will never change.</span></span> <span data-ttu-id="30557-115">Ciò consente al compilatore degli effetti di eseguire un'ottimizzazione aggiuntiva.</span><span class="sxs-lookup"><span data-stu-id="30557-115">This enables the effect compiler to do extra optimization.</span></span>

<span data-ttu-id="30557-116">Solo i parametri di primo livello non condivisi possono essere contrassegnati come valori letterali.</span><span class="sxs-lookup"><span data-stu-id="30557-116">Only non-shared top-level parameters can be marked as literal.</span></span> <span data-ttu-id="30557-117">I parametri possono essere contrassegnati solo come valori letterali con [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="30557-117">Parameters can only be marked as literal with [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span> <span data-ttu-id="30557-118">Non è possibile impostare valori letterali con [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="30557-118">Literal values cannot be set with [**ID3DXEffect**](id3dxeffect.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="30557-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="30557-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30557-120">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="30557-120">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



