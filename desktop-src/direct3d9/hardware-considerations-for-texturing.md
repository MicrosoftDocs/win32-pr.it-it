---
description: L'hardware corrente non implementa necessariamente tutte le funzionalità abilitate dall'interfaccia Direct3D. L'applicazione deve testare l'hardware dell'utente e modificare di conseguenza le strategie di rendering.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Considerazioni sull'hardware per la funzionalità di texturing (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875897"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a><span data-ttu-id="302ac-104">Considerazioni sull'hardware per la funzionalità di texturing (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="302ac-104">Hardware Considerations for Texturing (Direct3D 9)</span></span>

<span data-ttu-id="302ac-105">L'hardware corrente non implementa necessariamente tutte le funzionalità abilitate dall'interfaccia Direct3D.</span><span class="sxs-lookup"><span data-stu-id="302ac-105">Current hardware does not necessarily implement all the functionality that the Direct3D interface enables.</span></span> <span data-ttu-id="302ac-106">L'applicazione deve testare l'hardware dell'utente e modificare di conseguenza le strategie di rendering.</span><span class="sxs-lookup"><span data-stu-id="302ac-106">Your application must test user hardware and adjust its rendering strategies accordingly.</span></span>

<span data-ttu-id="302ac-107">Molte schede di accelerazione 3D non supportano i valori di iterazione diffusi come argomenti per la fusione di unità.</span><span class="sxs-lookup"><span data-stu-id="302ac-107">Many 3D accelerator cards do not support diffuse iterated values as arguments to blending units.</span></span> <span data-ttu-id="302ac-108">Tuttavia, l'applicazione può introdurre dati di colore iterati quando esegue la fusione di trame.</span><span class="sxs-lookup"><span data-stu-id="302ac-108">However, your application can introduce iterated color data when it performs texture blending.</span></span>

<span data-ttu-id="302ac-109">Alcuni componenti hardware 3D potrebbero non avere una fase di fusione associata alla prima trama.</span><span class="sxs-lookup"><span data-stu-id="302ac-109">Some 3D hardware may not have a blending stage associated with the first texture.</span></span> <span data-ttu-id="302ac-110">In questi adapter, l'applicazione deve eseguire la fusione nella seconda e terza fase della trama nel set di trame correnti.</span><span class="sxs-lookup"><span data-stu-id="302ac-110">On these adapters, your application must perform blending in the second and third texture stages in the set of current textures.</span></span>

<span data-ttu-id="302ac-111">A causa delle limitazioni della maggior parte dell'hardware odierno, poche schede video possono eseguire l'interpolazione trilineare mipmap tramite l'interfaccia di combinazione di più trame offerta da [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="302ac-111">Because of limitations in much of today's hardware, few display adapters can perform trilinear mipmap interpolation through the multiple texture blending interface offered by [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span> <span data-ttu-id="302ac-112">L'applicazione può usare la combinazione di trame MultiPASS per ottenere gli stessi effetti o per ridurre la \_ modalità di filtro mipmap del punto D3DTEXF, che è ampiamente supportata.</span><span class="sxs-lookup"><span data-stu-id="302ac-112">Your application can use multipass texture blending to achieve the same effects, or degrade to the D3DTEXF\_POINT mipmap filter mode, which is widely supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="302ac-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="302ac-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="302ac-114">Trame Direct3D</span><span class="sxs-lookup"><span data-stu-id="302ac-114">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
