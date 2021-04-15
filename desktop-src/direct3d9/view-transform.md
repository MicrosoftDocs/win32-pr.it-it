---
description: In questa sezione vengono introdotti i concetti di base della trasformazione visualizzazione e vengono fornite informazioni dettagliate su come configurare una matrice di trasformazione visualizzazione in un'applicazione Direct3D.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Visualizzazione trasformazione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521906"
---
# <a name="view-transform-direct3d-9"></a><span data-ttu-id="4bd5b-103">Visualizzazione trasformazione (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4bd5b-103">View Transform (Direct3D 9)</span></span>

<span data-ttu-id="4bd5b-104">In questa sezione vengono introdotti i concetti di base della trasformazione visualizzazione e vengono fornite informazioni dettagliate su come configurare una matrice di trasformazione visualizzazione in un'applicazione Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-104">This section introduces the basic concepts of the view transform and provides details on how to set up a view transform matrix in a Direct3D application.</span></span>

<span data-ttu-id="4bd5b-105">La trasformazione visualizzazione individua il visualizzatore nello spazio globale, trasformando i vertici nello spazio della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-105">The view transform locates the viewer in world space, transforming vertices into camera space.</span></span> <span data-ttu-id="4bd5b-106">Nello spazio della fotocamera, la fotocamera o il visualizzatore si trova all'origine, osservando la direzione della z positiva.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-106">In camera space, the camera, or viewer, is at the origin, looking in the positive z-direction.</span></span> <span data-ttu-id="4bd5b-107">Si ricordi che Direct3D usa un sistema di coordinate a sinistra, quindi la z è positiva in una scena.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-107">Recall that Direct3D uses a left-handed coordinate system, so z is positive into a scene.</span></span> <span data-ttu-id="4bd5b-108">La matrice di visualizzazione Riloca gli oggetti nel mondo intorno alla posizione della fotocamera, ovvero l'origine dello spazio della fotocamera e l'orientamento.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-108">The view matrix relocates the objects in the world around a camera's position - the origin of camera space - and orientation.</span></span>

<span data-ttu-id="4bd5b-109">Esistono diversi modi per creare una matrice di viste.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-109">There are many ways to create a view matrix.</span></span> <span data-ttu-id="4bd5b-110">In tutti i casi, la fotocamera ha una posizione e un orientamento logici nello spazio globale usato come punto di partenza per creare una matrice di visualizzazione che verrà applicata ai modelli in una scena.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-110">In all cases, the camera has some logical position and orientation in world space that is used as a starting point to create a view matrix that will be applied to the models in a scene.</span></span> <span data-ttu-id="4bd5b-111">La matrice di visualizzazione converte e ruota gli oggetti in modo da posizionarli nello spazio della fotocamera, in cui la fotocamera è all'origine.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-111">The view matrix translates and rotates objects to place them in camera space, where the camera is at the origin.</span></span> <span data-ttu-id="4bd5b-112">Un modo per creare una matrice di viste consiste nel combinare una matrice di traslazione con matrici di rotazione per ogni asse.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-112">One way to create a view matrix is to combine a translation matrix with rotation matrices for each axis.</span></span> <span data-ttu-id="4bd5b-113">In questo approccio viene applicata la seguente equazione della matrice generale.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-113">In this approach, the following general matrix equation applies.</span></span>

![equazione della trasformazione visualizzazione](images/viewtran.png)

<span data-ttu-id="4bd5b-115">In questa formula, V è la matrice di visualizzazione da creare, T è una matrice di traslazione che riposiziona gli oggetti nel mondo e R ₓ tramite R<sub>z</sub> sono matrici di rotazione che ruotano gli oggetti lungo l'asse x, y e z.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-115">In this formula, V is the view matrix being created, T is a translation matrix that repositions objects in the world, and Rₓ through R<sub>z</sub> are rotation matrices that rotate objects along the x-, y-, and z-axis.</span></span> <span data-ttu-id="4bd5b-116">Le matrici di traslazione e rotazione sono basate sulla posizione logica e sull'orientamento della fotocamera nello spazio globale.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-116">The translation and rotation matrices are based on the camera's logical position and orientation in world space.</span></span> <span data-ttu-id="4bd5b-117">Quindi, se la posizione logica della fotocamera nel mondo è <10, 20100>, l'obiettivo della matrice di traslazione è spostare gli oggetti-10 unità lungo l'asse x,-20 unità lungo l'asse y e-100 unità lungo l'asse z.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-117">So, if the camera's logical position in the world is <10,20,100>, the aim of the translation matrix is to move objects -10 units along the x-axis, -20 units along the y-axis, and -100 units along the z-axis.</span></span> <span data-ttu-id="4bd5b-118">Le matrici di rotazione nella formula sono basate sull'orientamento della fotocamera, in termini di quanto gli assi dello spazio della fotocamera vengono ruotati dall'allineamento allo spazio globale.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-118">The rotation matrices in the formula are based on the camera's orientation, in terms of how much the axes of camera space are rotated out of alignment with world space.</span></span> <span data-ttu-id="4bd5b-119">Ad esempio, se la fotocamera indicata in precedenza punta verso il basso, l'asse z è 90 gradi (pi/2 radianti) dall'allineamento con l'asse z dello spazio globale, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-119">For example, if the camera mentioned earlier is pointing straight down, its z-axis is 90 degrees (pi/2 radians) out of alignment with the z-axis of world space, as shown in the following illustration.</span></span>

![illustrazione dello spazio di visualizzazione della fotocamera rispetto allo spazio globale](images/camtop.png)

<span data-ttu-id="4bd5b-121">Le matrici di rotazione applicano le rotazioni di uguale, ma opposto, alla grandezza dei modelli nella scena.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-121">The rotation matrices apply rotations of equal, but opposite, magnitude to the models in the scene.</span></span> <span data-ttu-id="4bd5b-122">La matrice di visualizzazione per questa fotocamera include una rotazione di-90 gradi intorno all'asse x.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-122">The view matrix for this camera includes a rotation of -90 degrees around the x-axis.</span></span> <span data-ttu-id="4bd5b-123">La matrice di rotazione viene combinata con la matrice di traslazione per creare una matrice di visualizzazione che consente di regolare la posizione e l'orientamento degli oggetti nella scena in modo che la parte superiore si trovi davanti alla fotocamera, fornendo l'aspetto che la fotocamera è sopra il modello.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-123">The rotation matrix is combined with the translation matrix to create a view matrix that adjusts the position and orientation of the objects in the scene so that their top is facing the camera, giving the appearance that the camera is above the model.</span></span>

## <a name="setting-up-a-view-matrix"></a><span data-ttu-id="4bd5b-124">Impostazione di una matrice di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="4bd5b-124">Setting Up a View Matrix</span></span>

<span data-ttu-id="4bd5b-125">Le funzioni di supporto [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) e [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) creano una matrice di viste basata sulla posizione della fotocamera e un punto di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-125">The [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) and [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) helper functions create a view matrix based on the camera location and a look-at point.</span></span>

<span data-ttu-id="4bd5b-126">Nell'esempio seguente viene creata una matrice di viste per le coordinate di sinistra.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-126">The following example creates a view matrix for left-handed coordinates.</span></span>


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



<span data-ttu-id="4bd5b-127">Direct3D usa le matrici World e View per configurare diverse strutture di dati interne.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-127">Direct3D uses the world and view matrices to configure several internal data structures.</span></span> <span data-ttu-id="4bd5b-128">Ogni volta che si imposta una nuova matrice World o View, il sistema ricalcola le strutture interne associate.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-128">Each time you set a new world or view matrix, the system recalculates the associated internal structures.</span></span> <span data-ttu-id="4bd5b-129">L'impostazione frequente di queste matrici è un calcolo che richiede molto tempo.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-129">Setting these matrices frequently is computationally time-consuming.</span></span> <span data-ttu-id="4bd5b-130">È possibile ridurre al minimo il numero di calcoli necessari concatenando il mondo e visualizzare le matrici in una matrice di visualizzazione globale impostata come matrice globale e quindi impostando la matrice di visualizzazione sull'identità.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-130">You can minimize the number of required calculations by concatenating your world and view matrices into a world-view matrix that you set as the world matrix, and then setting the view matrix to the identity.</span></span> <span data-ttu-id="4bd5b-131">Mantieni le copie memorizzate nella cache di singole matrici di mondo e di visualizzazione che puoi modificare, concatenare e reimpostare la matrice globale in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-131">Keep cached copies of individual world and view matrices that you can modify, concatenate, and reset the world matrix as needed.</span></span> <span data-ttu-id="4bd5b-132">Per maggiore chiarezza, i campioni utilizzano raramente questa ottimizzazione.</span><span class="sxs-lookup"><span data-stu-id="4bd5b-132">For clarity, the samples rarely employ this optimization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bd5b-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4bd5b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bd5b-134">Trasformazioni</span><span class="sxs-lookup"><span data-stu-id="4bd5b-134">Transforms</span></span>](transforms.md)
</dt> </dl>

 

 



