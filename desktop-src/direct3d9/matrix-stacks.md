---
description: La libreria dell'utilità D3DX fornisce l'interfaccia ID3DXMATRIXStack.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Stack di matrici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d535307fb99d8743b910f2f3f8c6d55e197748e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876649"
---
# <a name="matrix-stacks-direct3d-9"></a><span data-ttu-id="828d7-103">Stack di matrici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="828d7-103">Matrix Stacks (Direct3D 9)</span></span>

<span data-ttu-id="828d7-104">La libreria dell'utilità D3DX fornisce l'interfaccia [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="828d7-104">The D3DX utility library provides the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span> <span data-ttu-id="828d7-105">Fornisce un meccanismo per consentire il push e la visualizzazione di matrici da uno stack di matrici.</span><span class="sxs-lookup"><span data-stu-id="828d7-105">It supplies a mechanism to enable matrices to be pushed onto and popped off of a matrix stack.</span></span> <span data-ttu-id="828d7-106">Implementare uno stack di matrici è un modo efficiente per tenere traccia delle matrici mentre si attraversa una gerarchia di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="828d7-106">Implementing a matrix stack is an efficient way to track matrices while traversing a transform hierarchy.</span></span>

<span data-ttu-id="828d7-107">La libreria di utilità D3DX utilizza uno stack di matrici per archiviare le trasformazioni come matrici.</span><span class="sxs-lookup"><span data-stu-id="828d7-107">The D3DX utility library uses a matrix stack to store transformations as matrices.</span></span> <span data-ttu-id="828d7-108">I vari metodi dell'interfaccia [**ID3DXMATRIXStack**](id3dxmatrixstack.md) gestiscono la matrice corrente o la matrice posizionata all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="828d7-108">The various methods of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface deal with the current matrix, or the matrix located on top of the stack.</span></span> <span data-ttu-id="828d7-109">È possibile cancellare la matrice corrente con il metodo [**ID3DXMATRIXStack:: LoadIdentity**](id3dxmatrixstack--loadidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="828d7-109">You can clear the current matrix with the [**ID3DXMATRIXStack::LoadIdentity**](id3dxmatrixstack--loadidentity.md) method.</span></span> <span data-ttu-id="828d7-110">Per specificare in modo esplicito una determinata matrice da caricare come matrice di trasformazione corrente, usare il metodo [**ID3DXMATRIXStack:: LoadMatrix**](id3dxmatrixstack--loadmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="828d7-110">To explicitly specify a certain matrix to load as the current transformation matrix, use the [**ID3DXMATRIXStack::LoadMatrix**](id3dxmatrixstack--loadmatrix.md) method.</span></span> <span data-ttu-id="828d7-111">È quindi possibile chiamare il metodo [**ID3DXMATRIXStack:: MultMatrix**](id3dxmatrixstack--multmatrix.md) o [**ID3DXMATRIXStack:: MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) per moltiplicare la matrice corrente in base alla matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="828d7-111">Then you can call either the [**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md) method or the [**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) method to multiply the current matrix by the specified matrix.</span></span>

<span data-ttu-id="828d7-112">Il metodo [**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md) consente di tornare alla matrice di trasformazione precedente e il metodo [**ID3DXMATRIXStack::P USH**](id3dxmatrixstack--push.md) aggiunge una matrice di trasformazione allo stack.</span><span class="sxs-lookup"><span data-stu-id="828d7-112">The [**ID3DXMATRIXStack::Pop**](id3dxmatrixstack--pop.md) method enables you to return to the previous transformation matrix and the [**ID3DXMATRIXStack::Push**](id3dxmatrixstack--push.md) method adds a transformation matrix to the stack.</span></span>

<span data-ttu-id="828d7-113">Le singole matrici nello stack della matrice sono rappresentate come matrici omogenee 4x4, definite dalla struttura [**D3DXMATRIX**](d3dxmatrix.md) della libreria dell'utilità D3DX.</span><span class="sxs-lookup"><span data-stu-id="828d7-113">The individual matrices on the matrix stack are represented as 4x4 homogeneous matrices, defined by the D3DX utility library [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

<span data-ttu-id="828d7-114">La libreria di utilità D3DX fornisce uno stack di matrici tramite un oggetto COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="828d7-114">The D3DX utility library provides a matrix stack through a component object model (COM) object.</span></span>

## <a name="implementing-a-scene-hierarchy"></a><span data-ttu-id="828d7-115">Implementazione di una gerarchia della scena</span><span class="sxs-lookup"><span data-stu-id="828d7-115">Implementing a Scene Hierarchy</span></span>

<span data-ttu-id="828d7-116">Uno stack di matrici semplifica la creazione di modelli gerarchici, in cui gli oggetti complessi vengono costruiti da una serie di oggetti più semplici.</span><span class="sxs-lookup"><span data-stu-id="828d7-116">A matrix stack simplifies the construction of hierarchical models, in which complicated objects are constructed from a series of simpler objects.</span></span>

<span data-ttu-id="828d7-117">Una scena, o trasformazione, è in genere rappresentata da una struttura di dati dell'albero.</span><span class="sxs-lookup"><span data-stu-id="828d7-117">A scene, or transform, hierarchy is usually represented by a tree data structure.</span></span> <span data-ttu-id="828d7-118">Ogni nodo nella struttura dei dati dell'albero contiene una matrice.</span><span class="sxs-lookup"><span data-stu-id="828d7-118">Each node in the tree data structure contains a matrix.</span></span> <span data-ttu-id="828d7-119">Una matrice specifica rappresenta la modifica nei sistemi di coordinate dall'elemento padre del nodo al nodo.</span><span class="sxs-lookup"><span data-stu-id="828d7-119">A particular matrix represents the change in coordinate systems from the node's parent to the node.</span></span> <span data-ttu-id="828d7-120">Se, ad esempio, si modella un ARM umano, è possibile implementare la gerarchia mostrata nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="828d7-120">For example, if you are modeling a human arm, you might implement the hierarchy that is shown in the following diagram.</span></span>

![diagramma della gerarchia di un ARM umano](images/stack1.png)

<span data-ttu-id="828d7-122">In questa gerarchia la matrice Body posiziona il corpo nel mondo.</span><span class="sxs-lookup"><span data-stu-id="828d7-122">In this hierarchy, the Body matrix places the body in the world.</span></span> <span data-ttu-id="828d7-123">La matrice UpperArm contiene la rotazione della spalla, la matrice LowerArm contiene la rotazione del gomito e la matrice della mano contiene la rotazione del polso.</span><span class="sxs-lookup"><span data-stu-id="828d7-123">The UpperArm matrix contains the rotation of the shoulder, the LowerArm matrix contains the rotation of the elbow, and the Hand matrix contains the rotation of the wrist.</span></span> <span data-ttu-id="828d7-124">Per determinare il punto in cui la mano è relativa al mondo, si moltiplicano tutte le matrici dal corpo fino a mano insieme.</span><span class="sxs-lookup"><span data-stu-id="828d7-124">To determine where the hand is relative to the world, you multiply all the matrices from Body down through Hand together.</span></span>

<span data-ttu-id="828d7-125">La gerarchia precedente è troppo semplicistica, perché ogni nodo ha un solo figlio.</span><span class="sxs-lookup"><span data-stu-id="828d7-125">The previous hierarchy is overly simplistic, because each node has only one child.</span></span> <span data-ttu-id="828d7-126">Se si inizia a modellare la mano in modo più dettagliato, è probabile che si aggiungano dita e un pollice.</span><span class="sxs-lookup"><span data-stu-id="828d7-126">If you begin to model the hand in more detail, you will probably add fingers and a thumb.</span></span> <span data-ttu-id="828d7-127">Ogni cifra può essere aggiunta alla gerarchia come elementi figlio di mano, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="828d7-127">Each digit can be added to the hierarchy as children of Hand, as shown in the following diagram.</span></span>

![diagramma della gerarchia di una mano umana](images/stack2.png)

<span data-ttu-id="828d7-129">Se si attraversa il grafico completo del ARM in un livello di profondità incrociato prima di un percorso, prima di passare al percorso successivo, per disegnare la scena, è possibile eseguire una sequenza di rendering segmentato.</span><span class="sxs-lookup"><span data-stu-id="828d7-129">If you traverse the complete graph of the arm in depth-first order - traversing as far down one path as possible before moving on to the next path - to draw the scene, you perform a sequence of segmented rendering.</span></span> <span data-ttu-id="828d7-130">Ad esempio, per eseguire il rendering della mano e delle dita, si implementa il modello seguente.</span><span class="sxs-lookup"><span data-stu-id="828d7-130">For example, to render the hand and fingers, you implement the following pattern.</span></span>

1.  <span data-ttu-id="828d7-131">Eseguire il push della matrice Hand nello stack della matrice.</span><span class="sxs-lookup"><span data-stu-id="828d7-131">Push the Hand matrix onto the matrix stack.</span></span>
2.  <span data-ttu-id="828d7-132">Creare la mano.</span><span class="sxs-lookup"><span data-stu-id="828d7-132">Draw the hand.</span></span>
3.  <span data-ttu-id="828d7-133">Eseguire il push della matrice thumb nello stack della matrice.</span><span class="sxs-lookup"><span data-stu-id="828d7-133">Push the Thumb matrix onto the matrix stack.</span></span>
4.  <span data-ttu-id="828d7-134">Creare il cursore.</span><span class="sxs-lookup"><span data-stu-id="828d7-134">Draw the thumb.</span></span>
5.  <span data-ttu-id="828d7-135">Estrae la matrice Thumb dallo stack.</span><span class="sxs-lookup"><span data-stu-id="828d7-135">Pop the Thumb matrix off the stack.</span></span>
6.  <span data-ttu-id="828d7-136">Inserire la matrice del dito 1 nello stack della matrice.</span><span class="sxs-lookup"><span data-stu-id="828d7-136">Push the Finger 1 matrix onto the matrix stack.</span></span>
7.  <span data-ttu-id="828d7-137">Viene disegnato il primo dito.</span><span class="sxs-lookup"><span data-stu-id="828d7-137">Draw the first finger.</span></span>
8.  <span data-ttu-id="828d7-138">Estrae la matrice del dito 1 dallo stack.</span><span class="sxs-lookup"><span data-stu-id="828d7-138">Pop the Finger 1 matrix off the stack.</span></span>
9.  <span data-ttu-id="828d7-139">Eseguire il push della matrice Finger 2 nello stack della matrice.</span><span class="sxs-lookup"><span data-stu-id="828d7-139">Push the Finger 2 matrix onto the matrix stack.</span></span> <span data-ttu-id="828d7-140">Si continua in questo modo fino a quando non viene eseguito il rendering di tutte le dita e Thumb.</span><span class="sxs-lookup"><span data-stu-id="828d7-140">You continue in this manner until all the fingers and thumb are rendered.</span></span>

<span data-ttu-id="828d7-141">Dopo aver completato il rendering delle dita, si estrae la matrice della mano dallo stack.</span><span class="sxs-lookup"><span data-stu-id="828d7-141">After you have completed rendering the fingers, you would pop the Hand matrix off the stack.</span></span>

<span data-ttu-id="828d7-142">È possibile seguire questo processo di base nel codice con gli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="828d7-142">You can follow this basic process in code with the following examples.</span></span> <span data-ttu-id="828d7-143">Quando si verifica un nodo durante la ricerca depth-first della struttura di dati dell'albero, inserire la matrice nella parte superiore dello stack della matrice.</span><span class="sxs-lookup"><span data-stu-id="828d7-143">When you encounter a node during the depth-first search of the tree data structure, push the matrix onto the top of the matrix stack.</span></span>


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



<span data-ttu-id="828d7-144">Al termine di un nodo, estrarre la matrice dalla parte superiore dello stack della matrice.</span><span class="sxs-lookup"><span data-stu-id="828d7-144">When you are finished with a node, pop the matrix off the top of the matrix stack.</span></span>


```
MatrixStack->Pop();
```



<span data-ttu-id="828d7-145">In questo modo, la matrice nella parte superiore dello stack rappresenta sempre la trasformazione globale del nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="828d7-145">In this way, the matrix on the top of the stack always represents the world-transform of the current node.</span></span> <span data-ttu-id="828d7-146">Pertanto, prima di disegnare ogni nodo, è necessario impostare la matrice Direct3D.</span><span class="sxs-lookup"><span data-stu-id="828d7-146">Therefore, before drawing each node, you should set the Direct3D matrix.</span></span>


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



<span data-ttu-id="828d7-147">Per ulteriori informazioni sui metodi specifici che è possibile eseguire su uno stack della matrice D3DX, vedere l'argomento di riferimento [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="828d7-147">For more information about the specific methods that you can perform on a D3DX matrix stack, see the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) reference topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="828d7-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="828d7-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="828d7-149">Pipeline Vertex</span><span class="sxs-lookup"><span data-stu-id="828d7-149">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 



