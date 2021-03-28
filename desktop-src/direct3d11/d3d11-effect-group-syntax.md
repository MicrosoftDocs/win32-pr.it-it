---
title: Sintassi del gruppo di effetti (Direct3D 11)
description: Un gruppo di effetti viene dichiarato con la sintassi descritta in questa sezione.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9221341810990801f1ed07005e0dcb917df42360
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104472046"
---
# <a name="effect-group-syntax-direct3d-11"></a><span data-ttu-id="55fca-103">Sintassi del gruppo di effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="55fca-103">Effect Group Syntax (Direct3D 11)</span></span>

<span data-ttu-id="55fca-104">Un gruppo di effetti viene dichiarato con la sintassi descritta in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="55fca-104">An effect group is declared with the syntax described in this section.</span></span>


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a><span data-ttu-id="55fca-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="55fca-105">Parameters</span></span>



| <span data-ttu-id="55fca-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="55fca-106">Item</span></span>                                                                                                                                                                           | <span data-ttu-id="55fca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55fca-107">Description</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55fca-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span><span class="sxs-lookup"><span data-stu-id="55fca-108"><span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup</span></span><br/>                                                                                                         | <span data-ttu-id="55fca-109">parola chiave ecessario.</span><span class="sxs-lookup"><span data-stu-id="55fca-109">equired keyword.</span></span><br/>                                                                                                                                                                                                         |
| <span data-ttu-id="55fca-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span><span class="sxs-lookup"><span data-stu-id="55fca-110"><span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName</span></span><br/>                                                                       | <span data-ttu-id="55fca-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="55fca-111">Required.</span></span> <span data-ttu-id="55fca-112">Stringa ASCII che identifica in modo univoco il nome del gruppo di effetti.</span><span class="sxs-lookup"><span data-stu-id="55fca-112">An ASCII string that uniquely identifies the name of the effect group.</span></span> <span data-ttu-id="55fca-113">Diversamente dalle tecniche, i gruppi devono avere nomi per assicurarsi che le tecniche abbiano un identificatore univoco (vedere la sezione relativa a gruppi e tecniche di seguito).</span><span class="sxs-lookup"><span data-stu-id="55fca-113">Unlike techniques, groups must have names to ensure that techniques have a unique identifier (see Groups and Techniques section below).</span></span><br/> |
| <span data-ttu-id="55fca-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> Annotazioni < ></span><span class="sxs-lookup"><span data-stu-id="55fca-114"><span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < Annotations ></span></span><br/> | <span data-ttu-id="55fca-115">\[in \] facoltativo.</span><span class="sxs-lookup"><span data-stu-id="55fca-115">\[in\] Optional.</span></span> <span data-ttu-id="55fca-116">Una o più parti di informazioni (metadati) fornite dall'utente ignorate dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="55fca-116">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="55fca-117">Per la sintassi, vedere Sintassi delle annotazioni (Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="55fca-117">For syntax, see Annotation Syntax (Direct3D 11).</span></span> <br/>                                                      |
| <span data-ttu-id="55fca-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span><span class="sxs-lookup"><span data-stu-id="55fca-118"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/>                                           | <span data-ttu-id="55fca-119">"Technique10" o "technique11".</span><span class="sxs-lookup"><span data-stu-id="55fca-119">Either "technique10" or "technique11".</span></span> <span data-ttu-id="55fca-120">Le tecniche che usano la nuova funzionalità di Direct3D 11 (5 \_ 0 Shader, BindInterfaces e così via) devono usare "technique11".</span><span class="sxs-lookup"><span data-stu-id="55fca-120">Techniques which use functionality new to Direct3D 11 (5\_0 shaders, BindInterfaces, etc) must use "technique11".</span></span><br/>                                                                 |
| <span data-ttu-id="55fca-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>Techniquename</span><span class="sxs-lookup"><span data-stu-id="55fca-121"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName</span></span><br/>                                                       | <span data-ttu-id="55fca-122">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="55fca-122">Optional.</span></span> <span data-ttu-id="55fca-123">Stringa ASCII che identifica in modo univoco il nome della tecnica degli effetti.</span><span class="sxs-lookup"><span data-stu-id="55fca-123">An ASCII string that uniquely identifies the name of the effect technique.</span></span> <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a><span data-ttu-id="55fca-124">Gruppi e tecniche</span><span class="sxs-lookup"><span data-stu-id="55fca-124">Groups and Techniques</span></span>

<span data-ttu-id="55fca-125">Per mantenere la compatibilità con \_ \_ gli effetti FX 4 0, i gruppi sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="55fca-125">In order to maintain compatibility with fx\_4\_0 effects, groups are optional.</span></span> <span data-ttu-id="55fca-126">È presente un gruppo implicito con nome NULL che circonda tutte le tecniche globali.</span><span class="sxs-lookup"><span data-stu-id="55fca-126">There is an implicit NULL-named group surrounding all global techniques.</span></span>

<span data-ttu-id="55fca-127">Si consideri l'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="55fca-127">Consider the following example:</span></span>


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



<span data-ttu-id="55fca-128">In C++, è possibile ottenere una tecnica in base al nome in due modi.</span><span class="sxs-lookup"><span data-stu-id="55fca-128">In C++, one can get a technique by name in two ways.</span></span> <span data-ttu-id="55fca-129">I comandi seguenti troveranno le tecniche più ovvie:</span><span class="sxs-lookup"><span data-stu-id="55fca-129">The following commands will find the obvious techniques:</span></span>


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



<span data-ttu-id="55fca-130">Per assicurarsi che [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) funzioni in modo analogo agli effetti 10, tutti i gruppi definiti devono avere un nome.</span><span class="sxs-lookup"><span data-stu-id="55fca-130">In order to ensure that [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) works similarly to Effects 10, all defined groups must have a name.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55fca-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55fca-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55fca-132">Formato effetto</span><span class="sxs-lookup"><span data-stu-id="55fca-132">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="55fca-133">Sintassi della tecnica degli effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="55fca-133">Effect Technique Syntax (Direct3D 11)</span></span>](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





