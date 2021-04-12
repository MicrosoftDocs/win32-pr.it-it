---
description: Gli effetti di nebbia possono dare maggiore realismo a una scena 3D.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Stato di nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401043"
---
# <a name="fog-state-direct3d-9"></a><span data-ttu-id="b6a76-103">Stato di nebbia (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b6a76-103">Fog State (Direct3D 9)</span></span>

<span data-ttu-id="b6a76-104">Gli effetti di nebbia possono dare maggiore realismo a una scena 3D.</span><span class="sxs-lookup"><span data-stu-id="b6a76-104">Fog effects can give a 3D scene greater realism.</span></span> <span data-ttu-id="b6a76-105">È possibile utilizzare gli effetti di nebbia per più della simulazione della nebbia.</span><span class="sxs-lookup"><span data-stu-id="b6a76-105">You can use fog effects for more than simulating fog.</span></span> <span data-ttu-id="b6a76-106">Possono anche ridurre la chiarezza di una scena con distanza.</span><span class="sxs-lookup"><span data-stu-id="b6a76-106">They can also decrease the clarity of a scene with distance.</span></span> <span data-ttu-id="b6a76-107">Questo rispecchia ciò che accade nel mondo reale. Poiché gli oggetti diventano più distanti dall'utente, i relativi dettagli sono meno distinti.</span><span class="sxs-lookup"><span data-stu-id="b6a76-107">This mirrors what happens in the real world; as objects become more distant from the user, their detail is less distinct.</span></span>

<span data-ttu-id="b6a76-108">Per ulteriori informazioni sull'utilizzo di fog nell'applicazione, vedere [Fog (Direct3D 9)](fog.md).</span><span class="sxs-lookup"><span data-stu-id="b6a76-108">For more information about using fog in your application, see [Fog (Direct3D 9)](fog.md).</span></span>

<span data-ttu-id="b6a76-109">Un'applicazione C++ controlla la nebbia tramite gli Stati di rendering del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b6a76-109">A C++ application controls fog through device rendering states.</span></span> <span data-ttu-id="b6a76-110">Il tipo enumerato [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) include gli Stati per controllare se vengono usati pixel (tabella) o la nebbia dei vertici, il colore, la formula di nebbia applicata dal sistema e i parametri della formula.</span><span class="sxs-lookup"><span data-stu-id="b6a76-110">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes states to control whether pixel (table) or vertex fog is used, what color it is, the fog formula the system applies, and the parameters of the formula.</span></span>

<span data-ttu-id="b6a76-111">Per abilitare la nebbia, impostare lo \_ stato di rendering FOGENABLE di D3DRS su **true**.</span><span class="sxs-lookup"><span data-stu-id="b6a76-111">You enable fog by setting the D3DRS\_FOGENABLE render state to **TRUE**.</span></span> <span data-ttu-id="b6a76-112">Il colore di nebbia può essere impostato su qualsiasi valore di colore utilizzando lo \_ stato di rendering FogColor di D3DRS. il componente alfa del colore di nebbia viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b6a76-112">The fog color can be set to any color value by using the D3DRS\_FOGCOLOR render state; the alpha component of the fog color is ignored.</span></span>

<span data-ttu-id="b6a76-113">Gli \_ Stati di rendering D3DRS FOGTABLEMODE e D3DRS \_ FOGVERTEXMODE controllano la formula di nebbia applicata ai calcoli di nebbia e controllano indirettamente quale tipo di nebbia viene applicato.</span><span class="sxs-lookup"><span data-stu-id="b6a76-113">The D3DRS\_FOGTABLEMODE and D3DRS\_FOGVERTEXMODE render states control the fog formula applied for fog calculations, and they indirectly control which type of fog is applied.</span></span> <span data-ttu-id="b6a76-114">Entrambi gli Stati di rendering possono essere impostati su un membro del tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="b6a76-114">Both render states can be set to a member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="b6a76-115">L'impostazione dello stato di rendering su D3DFOG \_ none Disabilita rispettivamente il pixel o la nebbia del vertice.</span><span class="sxs-lookup"><span data-stu-id="b6a76-115">Setting either render state to D3DFOG\_NONE disables pixel or vertex fog, respectively.</span></span> <span data-ttu-id="b6a76-116">Se entrambi gli Stati di rendering sono impostati su modalità valide, il sistema applica solo gli effetti di nebbia dei pixel.</span><span class="sxs-lookup"><span data-stu-id="b6a76-116">If both render states are set to valid modes, the system applies only pixel fog effects.</span></span>

<span data-ttu-id="b6a76-117">Gli \_ Stati D3DRS FOGSTART e D3DRS \_ FOGEND render controllano i parametri della Formula Fog per la \_ modalità lineare D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="b6a76-117">The D3DRS\_FOGSTART and D3DRS\_FOGEND render states control fog formula parameters for the D3DFOG\_LINEAR mode.</span></span> <span data-ttu-id="b6a76-118">Lo \_ stato di rendering FOGDENSITY di D3DRS controlla la densità della nebbia nelle modalità di nebbia esponenziale.</span><span class="sxs-lookup"><span data-stu-id="b6a76-118">The D3DRS\_FOGDENSITY render state controls fog density in the exponential fog modes.</span></span>

<span data-ttu-id="b6a76-119">Per altre informazioni, vedere [parametri di nebbia (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b6a76-119">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6a76-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6a76-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6a76-121">Stati di rendering</span><span class="sxs-lookup"><span data-stu-id="b6a76-121">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
