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
# <a name="matrix-stacks-direct3d-9"></a>Stack di matrici (Direct3D 9)

La libreria dell'utilità D3DX fornisce l'interfaccia [**ID3DXMATRIXStack**](id3dxmatrixstack.md) . Fornisce un meccanismo per consentire il push e la visualizzazione di matrici da uno stack di matrici. Implementare uno stack di matrici è un modo efficiente per tenere traccia delle matrici mentre si attraversa una gerarchia di trasformazione.

La libreria di utilità D3DX utilizza uno stack di matrici per archiviare le trasformazioni come matrici. I vari metodi dell'interfaccia [**ID3DXMATRIXStack**](id3dxmatrixstack.md) gestiscono la matrice corrente o la matrice posizionata all'inizio dello stack. È possibile cancellare la matrice corrente con il metodo [**ID3DXMATRIXStack:: LoadIdentity**](id3dxmatrixstack--loadidentity.md) . Per specificare in modo esplicito una determinata matrice da caricare come matrice di trasformazione corrente, usare il metodo [**ID3DXMATRIXStack:: LoadMatrix**](id3dxmatrixstack--loadmatrix.md) . È quindi possibile chiamare il metodo [**ID3DXMATRIXStack:: MultMatrix**](id3dxmatrixstack--multmatrix.md) o [**ID3DXMATRIXStack:: MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) per moltiplicare la matrice corrente in base alla matrice specificata.

Il metodo [**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md) consente di tornare alla matrice di trasformazione precedente e il metodo [**ID3DXMATRIXStack::P USH**](id3dxmatrixstack--push.md) aggiunge una matrice di trasformazione allo stack.

Le singole matrici nello stack della matrice sono rappresentate come matrici omogenee 4x4, definite dalla struttura [**D3DXMATRIX**](d3dxmatrix.md) della libreria dell'utilità D3DX.

La libreria di utilità D3DX fornisce uno stack di matrici tramite un oggetto COM (Component Object Model).

## <a name="implementing-a-scene-hierarchy"></a>Implementazione di una gerarchia della scena

Uno stack di matrici semplifica la creazione di modelli gerarchici, in cui gli oggetti complessi vengono costruiti da una serie di oggetti più semplici.

Una scena, o trasformazione, è in genere rappresentata da una struttura di dati dell'albero. Ogni nodo nella struttura dei dati dell'albero contiene una matrice. Una matrice specifica rappresenta la modifica nei sistemi di coordinate dall'elemento padre del nodo al nodo. Se, ad esempio, si modella un ARM umano, è possibile implementare la gerarchia mostrata nel diagramma seguente.

![diagramma della gerarchia di un ARM umano](images/stack1.png)

In questa gerarchia la matrice Body posiziona il corpo nel mondo. La matrice UpperArm contiene la rotazione della spalla, la matrice LowerArm contiene la rotazione del gomito e la matrice della mano contiene la rotazione del polso. Per determinare il punto in cui la mano è relativa al mondo, si moltiplicano tutte le matrici dal corpo fino a mano insieme.

La gerarchia precedente è troppo semplicistica, perché ogni nodo ha un solo figlio. Se si inizia a modellare la mano in modo più dettagliato, è probabile che si aggiungano dita e un pollice. Ogni cifra può essere aggiunta alla gerarchia come elementi figlio di mano, come illustrato nella figura seguente.

![diagramma della gerarchia di una mano umana](images/stack2.png)

Se si attraversa il grafico completo del ARM in un livello di profondità incrociato prima di un percorso, prima di passare al percorso successivo, per disegnare la scena, è possibile eseguire una sequenza di rendering segmentato. Ad esempio, per eseguire il rendering della mano e delle dita, si implementa il modello seguente.

1.  Eseguire il push della matrice Hand nello stack della matrice.
2.  Creare la mano.
3.  Eseguire il push della matrice thumb nello stack della matrice.
4.  Creare il cursore.
5.  Estrae la matrice Thumb dallo stack.
6.  Inserire la matrice del dito 1 nello stack della matrice.
7.  Viene disegnato il primo dito.
8.  Estrae la matrice del dito 1 dallo stack.
9.  Eseguire il push della matrice Finger 2 nello stack della matrice. Si continua in questo modo fino a quando non viene eseguito il rendering di tutte le dita e Thumb.

Dopo aver completato il rendering delle dita, si estrae la matrice della mano dallo stack.

È possibile seguire questo processo di base nel codice con gli esempi seguenti. Quando si verifica un nodo durante la ricerca depth-first della struttura di dati dell'albero, inserire la matrice nella parte superiore dello stack della matrice.


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



Al termine di un nodo, estrarre la matrice dalla parte superiore dello stack della matrice.


```
MatrixStack->Pop();
```



In questo modo, la matrice nella parte superiore dello stack rappresenta sempre la trasformazione globale del nodo corrente. Pertanto, prima di disegnare ogni nodo, è necessario impostare la matrice Direct3D.


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



Per ulteriori informazioni sui metodi specifici che è possibile eseguire su uno stack della matrice D3DX, vedere l'argomento di riferimento [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline Vertex](vertex-pipeline.md)
</dt> </dl>

 

 



