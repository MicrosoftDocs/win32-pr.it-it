---
description: In Direct3D 10, le risorse di trama sono accessibili con una visualizzazione, che è un meccanismo per l'interpretazione hardware di una risorsa in memoria.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Visualizzazioni di trama (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06cd98a00782b826713e68304ad7cc132e4e0fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966214"
---
# <a name="texture-views-direct3d-10"></a>Visualizzazioni di trama (Direct3D 10)

In Direct3D 10, le risorse di trama sono accessibili con una visualizzazione, che è un meccanismo per l'interpretazione hardware di una risorsa in memoria. Una visualizzazione consente a una determinata fase della pipeline di accedere solo alle [risorse sottorisorse](d3d10-graphics-programming-guide-resources-types.md) necessarie, nella rappresentazione desiderata dall'applicazione.

Una vista supporta la nozione di una risorsa senza tipo. Una risorsa senza tipo è una risorsa creata con una dimensione specifica ma non con un tipo di dati specifico. I dati vengono interpretati dinamicamente quando vengono associati alla pipeline.

La figura seguente mostra un esempio di associazione di una matrice di trame 2D con 6 trame come risorsa dello shader creando una visualizzazione risorse dello shader. La risorsa viene quindi risolta come una matrice di trame. Nota: non è possibile associare contemporaneamente una risorsa subresource come input e output alla pipeline.

![illustrazione di una matrice di trame con sei trame](images/d3d10-cube-texture-faces.png)

Quando si usa una matrice di trame 2D come destinazione di rendering, la risorsa può essere visualizzata come una matrice di trame 2D (6 in questo esempio) con livelli mipmap (3 in questo esempio).

Creare un oggetto visualizzazione per una destinazione di rendering chiamando CreateRenderTargetView. Chiamare quindi OMSetRenderTargets per impostare la visualizzazione della destinazione di rendering sulla pipeline. Eseguire il rendering nelle destinazioni di rendering chiamando disegnare e usando RenderTargetArrayIndex per eseguire l'indicizzazione nella trama corretta nella matrice. Per eseguire l'associazione a qualsiasi matrice di sottorisorse, è possibile usare una sottorisorsa, ovvero una combinazione di indice di matrice o di mipmap. Quindi, è possibile eseguire l'associazione al secondo livello di mipmap e aggiornare questo particolare livello di mipmap, come illustrato nella figura seguente.

![illustrazione dell'associazione solo al secondo livello di mipmap di una matrice di trama](images/d3d10-cube-texture-faces-subresource.png)



|                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 10: in Direct3D 10 non si associa più una risorsa direttamente alla pipeline, si crea una vista di una risorsa e quindi si imposta la visualizzazione sulla pipeline. Ciò consente di eseguire la convalida e il mapping nel runtime e nel driver in fase di creazione della visualizzazione, riducendo al minimo il controllo dei tipi in fase di binding.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




