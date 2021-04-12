---
description: La discussione sulla trasformazione globale introduce i concetti di base e fornisce informazioni dettagliate su come configurare una trasformazione globale.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: Trasformazione globale (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e192f8ce4350c767122ef60f3cd36777753d2e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401106"
---
# <a name="world-transform-direct3d-9"></a><span data-ttu-id="99d87-103">Trasformazione globale (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="99d87-103">World Transform (Direct3D 9)</span></span>

<span data-ttu-id="99d87-104">La discussione sulla trasformazione globale introduce i concetti di base e fornisce informazioni dettagliate su come configurare una trasformazione globale.</span><span class="sxs-lookup"><span data-stu-id="99d87-104">The discussion of the world transformation introduces basic concepts and provides details on how to set up a world transform.</span></span>

## <a name="what-is-a-world-transform"></a><span data-ttu-id="99d87-105">Che cos'è una trasformazione globale?</span><span class="sxs-lookup"><span data-stu-id="99d87-105">What Is a World Transform?</span></span>

<span data-ttu-id="99d87-106">Una trasformazione globale modifica le coordinate dallo spazio del modello, in cui i vertici vengono definiti in relazione all'origine locale di un modello, allo spazio globale, in cui i vertici vengono definiti in relazione a un'origine comune a tutti gli oggetti in una scena.</span><span class="sxs-lookup"><span data-stu-id="99d87-106">A world transform changes coordinates from model space, where vertices are defined relative to a model's local origin, to World Space, where vertices are defined relative to an origin common to all the objects in a scene.</span></span> <span data-ttu-id="99d87-107">In sostanza, la trasformazione mondiale inserisce un modello nel mondo; quindi il nome.</span><span class="sxs-lookup"><span data-stu-id="99d87-107">In essence, the world transform places a model into the world; hence its name.</span></span> <span data-ttu-id="99d87-108">Nel diagramma seguente viene illustrata la relazione tra il sistema di coordinate globale e il sistema di coordinate locale di un modello.</span><span class="sxs-lookup"><span data-stu-id="99d87-108">The following diagram shows the relationship between the world coordinate system and a model's local coordinate system.</span></span>

![diagramma del modo in cui le coordinate globali e le coordinate locali sono correlate](images/worldcrd.png)

<span data-ttu-id="99d87-110">La trasformazione mondiale può includere qualsiasi combinazione di traslazioni, rotazioni e scalabilità.</span><span class="sxs-lookup"><span data-stu-id="99d87-110">The world transform can include any combination of translations, rotations, and scalings.</span></span>

## <a name="setting-up-a-world-matrix"></a><span data-ttu-id="99d87-111">Configurazione di una matrice globale</span><span class="sxs-lookup"><span data-stu-id="99d87-111">Setting Up a World Matrix</span></span>

<span data-ttu-id="99d87-112">Come per qualsiasi altra trasformazione, creare la trasformazione globale concatenando una serie di matrici in un'unica matrice che contiene la somma totale degli effetti.</span><span class="sxs-lookup"><span data-stu-id="99d87-112">As with any other transform, create the world transform by concatenating a series of matrices into a single matrix that contains the sum total of their effects.</span></span> <span data-ttu-id="99d87-113">Nel caso più semplice, quando un modello si trova all'origine mondiale e gli assi delle coordinate locali sono orientati allo stesso modo dello spazio globale, la matrice globale è la matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="99d87-113">In the simplest case, when a model is at the world origin and its local coordinate axes are oriented the same as world space, the world matrix is the identity matrix.</span></span> <span data-ttu-id="99d87-114">Più comunemente, la matrice globale è una combinazione di una traduzione nello spazio globale e possibilmente una o più rotazioni per trasformare il modello in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="99d87-114">More commonly, the world matrix is a combination of a translation into world space and possibly one or more rotations to turn the model as needed.</span></span>

<span data-ttu-id="99d87-115">Nell'esempio seguente, da una classe di modello 3D fittizia scritta in C++, USA le funzioni di supporto incluse nella libreria di utilità D3DX per creare una matrice globale che include tre rotazioni per orientare un modello e una traduzione per rilocarlo rispetto alla relativa posizione nello spazio globale.</span><span class="sxs-lookup"><span data-stu-id="99d87-115">The following example, from a fictitious 3D model class written in C++, uses the helper functions included in the D3DX utility library to create a world matrix that includes three rotations to orient a model and a translation to relocate it relative to its position in world space.</span></span>


```
/*
 * For the purposes of this example, the following variables
 * are assumed to be valid and initialized.
 *
 * The m_xPos, m_yPos, m_zPos variables contain the model's
 * location in world coordinates.
 *
 * The m_fPitch, m_fYaw, and m_fRoll variables are floats that 
 * contain the model's orientation in terms of pitch, yaw, and roll
 * angles, in radians.
 */
 
void C3DModel::MakeWorldMatrix( D3DXMATRIX* pMatWorld )
{
    D3DXMATRIX MatTemp;  // Temp matrix for rotations.
    D3DXMATRIX MatRot;   // Final rotation matrix, applied to 
                         // pMatWorld.
 
    // Using the left-to-right order of matrix concatenation,
    // apply the translation to the object's world position
    // before applying the rotations.
    D3DXMatrixTranslation(pMatWorld, m_xPos, m_yPos, m_zPos);
    D3DXMatrixIdentity(&MatRot);

    // Now, apply the orientation variables to the world matrix
    if(m_fPitch || m_fYaw || m_fRoll) {
        // Produce and combine the rotation matrices.
        D3DXMatrixRotationX(&MatTemp, m_fPitch);         // Pitch
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationY(&MatTemp, m_fYaw);           // Yaw
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationZ(&MatTemp, m_fRoll);          // Roll
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
 
        // Apply the rotation matrices to complete the world matrix.
        D3DXMatrixMultiply(pMatWorld, &MatRot, pMatWorld);
    }
}
```



<span data-ttu-id="99d87-116">Dopo aver preparato la matrice globale, chiamare il metodo [**IDirect3DDevice9:: setransform**](/windows/desktop/api) per impostarlo, specificando la macro [**D3DTS \_ World**](d3dts-world.md) per il primo parametro.</span><span class="sxs-lookup"><span data-stu-id="99d87-116">After you prepare the world matrix, call the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method to set it, specifying the [**D3DTS\_WORLD**](d3dts-world.md) macro for the first parameter.</span></span>

> [!Note]  
> <span data-ttu-id="99d87-117">Direct3D usa le matrici World e View impostate per configurare diverse strutture di dati interne.</span><span class="sxs-lookup"><span data-stu-id="99d87-117">Direct3D uses the world and view matrices that you set to configure several internal data structures.</span></span> <span data-ttu-id="99d87-118">Ogni volta che si imposta una nuova matrice World o View, il sistema ricalcola le strutture interne associate.</span><span class="sxs-lookup"><span data-stu-id="99d87-118">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="99d87-119">L'impostazione frequente di queste matrici, ad esempio migliaia di volte per fotogramma, richiede molto tempo.</span><span class="sxs-lookup"><span data-stu-id="99d87-119">Setting these matrices frequently-for example, thousands of times per frame-is computationally time-consuming.</span></span> <span data-ttu-id="99d87-120">È possibile ridurre al minimo il numero di calcoli necessari concatenando il mondo e visualizzare le matrici in una matrice di visualizzazione globale impostata come matrice globale e quindi impostando la matrice di visualizzazione sull'identità.</span><span class="sxs-lookup"><span data-stu-id="99d87-120">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="99d87-121">Conserva le copie memorizzate nella cache di singole matrici e visualizza le matrici in modo che sia possibile modificare, concatenare e reimpostare la matrice globale in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="99d87-121">Keep cached copies of individual world and view matrices so that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="99d87-122">Per maggiore chiarezza, in questa documentazione gli esempi di Direct3D utilizzano raramente questa ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="99d87-122">For clarity, in this documentation Direct3D samples rarely employ this optimization.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="99d87-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99d87-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99d87-124">Trasformazioni</span><span class="sxs-lookup"><span data-stu-id="99d87-124">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 



