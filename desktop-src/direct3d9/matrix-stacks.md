---
description: La libreria di utilità D3DX fornisce l'interfaccia ID3DXMATRIXStack.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Stack di matrici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a480236bc42142b725e232a9fb92807be73fb03097104a0cc4fc08643f4361af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044331"
---
# <a name="matrix-stacks-direct3d-9"></a>Stack di matrici (Direct3D 9)

La libreria di utilità D3DX fornisce [**l'interfaccia ID3DXMATRIXStack.**](id3dxmatrixstack.md) Fornisce un meccanismo per consentire il push delle matrici e il loro es estratto da uno stack di matrici. L'implementazione di uno stack di matrici è un modo efficiente per tenere traccia delle matrici durante l'attraversamento di una gerarchia di trasformazione.

La libreria di utilità D3DX usa uno stack di matrici per archiviare le trasformazioni come matrici. I vari metodi [**dell'interfaccia ID3DXMATRIXStack**](id3dxmatrixstack.md) si occupano della matrice corrente o della matrice posizionata all'inizio dello stack. È possibile cancellare la matrice corrente con il [**metodo ID3DXMATRIXStack::LoadIdentity.**](id3dxmatrixstack--loadidentity.md) Per specificare in modo esplicito una determinata matrice da caricare come matrice di trasformazione corrente, usare il [**metodo ID3DXMATRIXStack::LoadMatrix.**](id3dxmatrixstack--loadmatrix.md) È quindi possibile chiamare il [**metodo ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md) o il metodo [**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) per moltiplicare la matrice corrente per la matrice specificata.

Il [**metodo ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md) consente di tornare alla matrice di trasformazione precedente e il metodo [**ID3DXMATRIXStack::P ush**](id3dxmatrixstack--push.md) aggiunge una matrice di trasformazione nello stack.

Le singole matrici nello stack di matrici sono rappresentate come matrici omogenee 4x4, definite dalla struttura [**D3DXMATRIX**](d3dxmatrix.md) della libreria di utilità D3DX.

La libreria di utilità D3DX fornisce uno stack di matrici tramite un oggetto COM (Component Object Model).

## <a name="implementing-a-scene-hierarchy"></a>Implementazione di una gerarchia di scene

Uno stack di matrici semplifica la costruzione di modelli gerarchici, in cui oggetti complessi vengono costruiti da una serie di oggetti più semplici.

Una scena, o trasformazione, gerarchia è in genere rappresentata da una struttura di dati dell'albero. Ogni nodo nella struttura dei dati dell'albero contiene una matrice. Una particolare matrice rappresenta la modifica dei sistemi di coordinate dall'elemento padre del nodo al nodo. Ad esempio, se si modella un arm umano, è possibile implementare la gerarchia illustrata nel diagramma seguente.

![diagramma della gerarchia di un arm umano](images/stack1.png)

In questa gerarchia, la matrice Body posiziona il corpo nel mondo. La matrice UpperArm contiene la rotazione della lenza, la matrice LowerArm contiene la rotazione del gomito e la matrice Hand contiene la rotazione del gomito. Per determinare dove la mano è relativa al mondo, moltiplicare tutte le matrici da Corpo fino a Mano insieme.

La gerarchia precedente è esemplistica, perché ogni nodo ha un solo elemento figlio. Se si inizia a modellare la mano in modo più dettagliato, probabilmente si aggiungeranno le dita e un pollice. Ogni cifra può essere aggiunta alla gerarchia come elementi figlio di Hand, come illustrato nel diagramma seguente.

![diagramma della gerarchia di una mano umana](images/stack2.png)

Se si attraversa il grafico completo del arm in ordine di profondità, che attraversa il più in basso possibile un tracciato prima di passare al tracciato successivo, per disegnare la scena, esegui una sequenza di rendering segmentato. Ad esempio, per eseguire il rendering della mano e delle dita, implementare il modello seguente.

1.  Inserire la matrice Hand nello stack della matrice.
2.  Disegnare la mano.
3.  Inserire la matrice Thumb nello stack della matrice.
4.  Disegnare il cursore.
5.  Espulsa la matrice Thumb dallo stack.
6.  Inserire la matrice Finger 1 nello stack della matrice.
7.  Disegnare il primo dito.
8.  Espulse la matrice Finger 1 dallo stack.
9.  Inserire la matrice Finger 2 nello stack della matrice. Si continua in questo modo fino a quando non viene eseguito il rendering di tutte le dita e il cursore.

Dopo aver completato il rendering delle dita, si espulse la matrice Hand dallo stack.

È possibile seguire questo processo di base nel codice con gli esempi seguenti. Quando si rileva un nodo durante la ricerca depth-first della struttura dei dati dell'albero, eseguire il push della matrice all'inizio dello stack di matrici.


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



Al termine dell'esecuzione di un nodo, espulse la matrice dall'inizio dello stack di matrici.


```
MatrixStack->Pop();
```



In questo modo, la matrice all'inizio dello stack rappresenta sempre la trasformazione globale del nodo corrente. Pertanto, prima di disegnare ogni nodo, è necessario impostare la matrice Direct3D.


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



Per altre informazioni sui metodi specifici che è possibile eseguire in uno stack di matrici D3DX, vedere l'argomento di riferimento [**ID3DXMATRIXStack.**](id3dxmatrixstack.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex Pipeline](vertex-pipeline.md)
</dt> </dl>

 

 



