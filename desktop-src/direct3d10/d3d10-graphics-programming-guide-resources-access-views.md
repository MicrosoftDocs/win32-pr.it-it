---
description: In Direct3D 10 le risorse di trama sono accessibili con una visualizzazione, che è un meccanismo per l'interpretazione hardware di una risorsa in memoria.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Visualizzazioni trama (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc420e39c4d577947cae657f3296b15f0052db9e823e07d3a3ba1ccb641fb6b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118101348"
---
# <a name="texture-views-direct3d-10"></a>Visualizzazioni trama (Direct3D 10)

In Direct3D 10 le risorse di trama sono accessibili con una visualizzazione, che è un meccanismo per l'interpretazione hardware di una risorsa in memoria. Una visualizzazione consente a una determinata fase della pipeline di accedere solo [alle sottorisorse](d3d10-graphics-programming-guide-resources-types.md) necessarie, nella rappresentazione desiderata dall'applicazione.

Una visualizzazione supporta la nozione di risorsa senza tipo. Una risorsa senza tipo è una risorsa creata con una dimensione specifica ma non con un tipo di dati specifico. I dati vengono interpretati in modo dinamico quando sono associati alla pipeline.

La figura seguente mostra un esempio di associazione di una matrice di trame 2D con 6 trame come risorsa shader creando una visualizzazione delle risorse shader. La risorsa viene quindi indirizzata come matrice di trame. Nota: una sottorisorsa non può essere associata contemporaneamente come input e output alla pipeline.

![illustrazione di una matrice di trame con sei trame](images/d3d10-cube-texture-faces.png)

Quando si usa una matrice di trame 2D come destinazione di rendering, la risorsa può essere visualizzata come matrice di trame 2D (6 in questo esempio) con livelli mipmap (3 in questo esempio).

Creare un oggetto visualizzazione per una destinazione di rendering chiamando CreateRenderTargetView. Chiamare quindi OMSetRenderTargets per impostare la visualizzazione della destinazione di rendering sulla pipeline. Eseguire il rendering nelle destinazioni di rendering chiamando Draw e usando RenderTargetArrayIndex per indicizzare la trama appropriata nella matrice. È possibile usare una sottorisorsa (una combinazione di livello mipmap e indice di matrice) per eseguire l'associazione a qualsiasi matrice di sottorisorse. È quindi possibile eseguire l'associazione al secondo livello mipmap e aggiornare questo particolare livello di mipmap solo se si vuole, come illustrato nella figura seguente.

![illustrazione del binding solo al secondo livello mipmap di una matrice di trame](images/d3d10-cube-texture-faces-subresource.png)



Differenze tra Direct3D 9 e Direct3D 10:

- In Direct3D 10 non si associa più una risorsa direttamente alla pipeline, si crea una visualizzazione di una risorsa e quindi si imposta la vista sulla pipeline. In questo modo la convalida e il mapping nel runtime e nel driver possono essere eseguiti durante la creazione della visualizzazione, riducendo al minimo il controllo dei tipi in fase di associazione.



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




