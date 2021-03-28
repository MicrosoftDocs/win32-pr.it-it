---
title: register
description: register
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- Registra HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b378cd97bc9779951d62873d393009c98d32823
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399055"
---
# <a name="register"></a><span data-ttu-id="b586e-104">register</span><span class="sxs-lookup"><span data-stu-id="b586e-104">register</span></span>

<span data-ttu-id="b586e-105">Parola chiave facoltativa per l'assegnazione di una variabile shader a un particolare registro, che usa la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="b586e-105">Optional keyword for assigning a shader variable to a particular register, which uses the following syntax:</span></span>



| <span data-ttu-id="b586e-106">: Register ( *\[ \_ profilo \] shader*, *tipo \# \[ sottocomponente \]* )</span><span class="sxs-lookup"><span data-stu-id="b586e-106">: register ( *\[shader\_profile\]*, *Type\#\[subcomponent\]* )</span></span> |
|----------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="b586e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b586e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b586e-108"><span id="register"></span><span id="REGISTER"></span>Registro</span><span class="sxs-lookup"><span data-stu-id="b586e-108"><span id="register"></span><span id="REGISTER"></span>register</span></span>
</dt> <dd>

<span data-ttu-id="b586e-109">Parola chiave required.</span><span class="sxs-lookup"><span data-stu-id="b586e-109">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="b586e-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[profilo shader \_\]*</span><span class="sxs-lookup"><span data-stu-id="b586e-110"><span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[shader\_profile\]*</span></span>
</dt> <dd>

<span data-ttu-id="b586e-111">[Profilo shader](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)facoltativo, che può essere una destinazione shader o semplicemente **PS** o **vs**.</span><span class="sxs-lookup"><span data-stu-id="b586e-111">Optional [shader profile](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax), which can be a shader target or simply **ps** or **vs**.</span></span>

</dd> <dt>

<span data-ttu-id="b586e-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Sottocomponente di tipo \# \[\]*</span><span class="sxs-lookup"><span data-stu-id="b586e-112"><span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Type\#\[subcomponent\]*</span></span>
</dt> <dd>

<span data-ttu-id="b586e-113">Tipo di registrazione, numero e dichiarazione di sottocomponente.</span><span class="sxs-lookup"><span data-stu-id="b586e-113">Register type, number, and subcomponent declaration.</span></span>

-   <span data-ttu-id="b586e-114">Il tipo è uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="b586e-114">Type is one of the following:</span></span>

    

    | <span data-ttu-id="b586e-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="b586e-115">Type</span></span> | <span data-ttu-id="b586e-116">Descrizione registro</span><span class="sxs-lookup"><span data-stu-id="b586e-116">Register Description</span></span>       |
    |------|----------------------------|
    | <span data-ttu-id="b586e-117">b</span><span class="sxs-lookup"><span data-stu-id="b586e-117">b</span></span>    | <span data-ttu-id="b586e-118">Buffer costante</span><span class="sxs-lookup"><span data-stu-id="b586e-118">Constant buffer</span></span>            |
    | <span data-ttu-id="b586e-119">u</span><span class="sxs-lookup"><span data-stu-id="b586e-119">t</span></span>    | <span data-ttu-id="b586e-120">Trama e buffer di trama</span><span class="sxs-lookup"><span data-stu-id="b586e-120">Texture and texture buffer</span></span> |
    | <span data-ttu-id="b586e-121">c</span><span class="sxs-lookup"><span data-stu-id="b586e-121">c</span></span>    | <span data-ttu-id="b586e-122">Offset del buffer</span><span class="sxs-lookup"><span data-stu-id="b586e-122">Buffer offset</span></span>              |
    | <span data-ttu-id="b586e-123">s</span><span class="sxs-lookup"><span data-stu-id="b586e-123">s</span></span>    | <span data-ttu-id="b586e-124">Campionatore</span><span class="sxs-lookup"><span data-stu-id="b586e-124">Sampler</span></span>                    |
    | <span data-ttu-id="b586e-125">u</span><span class="sxs-lookup"><span data-stu-id="b586e-125">u</span></span>    | <span data-ttu-id="b586e-126">Unordered Access View</span><span class="sxs-lookup"><span data-stu-id="b586e-126">Unordered Access View</span></span>      |

    

     

-   <span data-ttu-id="b586e-127">*\#* numero del registro, ovvero un numero intero.</span><span class="sxs-lookup"><span data-stu-id="b586e-127">*\#* is the register number, which is an integer number.</span></span>
-   <span data-ttu-id="b586e-128">Il *sottocomponente* è un numero intero facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b586e-128">The *subcomponent* is an optional integer number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b586e-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="b586e-129">Remarks</span></span>

<span data-ttu-id="b586e-130">È possibile aggiungere una o più assegnazioni di registro alla stessa dichiarazione di variabile, separate da spazi.</span><span class="sxs-lookup"><span data-stu-id="b586e-130">You may add one or more register assignments to the same variable declaration, separated by spaces.</span></span>

<span data-ttu-id="b586e-131">Per le variabili Direct3D 10 nell'ambito globale, la parola chiave **Register** funziona come la parola chiave [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .</span><span class="sxs-lookup"><span data-stu-id="b586e-131">For Direct3D 10 variables in global scope, the **register** keyword acts the same as the [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) keyword.</span></span>

## <a name="examples"></a><span data-ttu-id="b586e-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="b586e-132">Examples</span></span>

<span data-ttu-id="b586e-133">Ecco alcuni esempi:</span><span class="sxs-lookup"><span data-stu-id="b586e-133">Here are some examples:</span></span>


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a><span data-ttu-id="b586e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b586e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b586e-135">Sintassi delle variabili</span><span class="sxs-lookup"><span data-stu-id="b586e-135">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="b586e-136">Variabili (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b586e-136">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 