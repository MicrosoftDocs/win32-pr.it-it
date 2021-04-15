---
description: In questa sezione viene descritto come utilizzare le interfacce relative al percorso dell'API documento XPS in un modello OM XPS.
ms.assetid: 4e76355a-ad53-4177-b8c7-3e768a1d4e3f
title: Utilizzo delle interfacce di percorso OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca66b65c6f20dc3b585de706e223df1f76d518a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529353"
---
# <a name="working-with-xps-om-path-interfaces"></a>Utilizzo delle interfacce di percorso OM XPS

In questa sezione viene descritto come utilizzare le interfacce relative al percorso dell'API documento XPS in un modello OM XPS.



| Nome interfaccia                                                            | Elementi figlio concettuali                                                                                                                                                                                                                                                                                                                                                                                                                                         | Descrizione                                                                                                                                                                                       |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                               | nessuno<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descrive un elemento di percorso grafico.<br/>                                                                                                                                                    |
| [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/>                             | [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/> [**IXpsOMTileBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)<br/> [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/> [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/> [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)<br/> [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | Viene utilizzato un pennello per riempire un'area o una linea.<br/>                                                                                                                                             |
| [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/>         | nessuno<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fornisce riempimenti o tratti a tinta unita. <br/>                                                                                                                                                |
| [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/>                 | nessuno<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fornisce un oggetto visivo, ad esempio un percorso, un glifo o un'area di disegno, o un oggetto visivo parziale da utilizzare come riempimento o tratto di affiancamento. <br/>                                                                  |
| [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/>                   | nessuno<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fornisce un'immagine (o immagine parziale) da utilizzare come riempimento o tratto affiancato. <br/>                                                                                                           |
| [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> | nessuno<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fornisce una sfumatura lineare da utilizzare come riempimento o tratto. <br/>                                                                                                                            |
| [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | nessuno<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fornisce una sfumatura radiale da utilizzare come riempimento o tratto. <br/>                                                                                                                            |
| [**IXpsOMGradientStop**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop)<br/>               | nessuno<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Definisce un punto di flessione del valore di un singolo colore all'interno di una sfumatura lineare o radiale. <br/>                                                                                                     |
| [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/>                       | [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>                                                                                                                                                                                                                                                                                                                                                                                             | Fornisce una definizione di un'area vettoriale da utilizzare come area di ridimensionamento o definizione del percorso. È costituito da una o più interfacce [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) . <br/> |
| [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>           | nessuno<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Parte della definizione di un'area a cui fa riferimento un'interfaccia [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) ed è costituita da uno o più segmenti. <br/>                                    |
| [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/>         | nessuno<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Specifica la trasformazione della matrice affine da applicare all'oggetto durante il rendering. <br/>                                                                                              |



 

## <a name="contents"></a>Contenuto

-   [Pennelli OM XPS](xps-object-model-brushes.md)
-   [Gradienti OM XPS](xps-object-model-gradients.md)
-   [Oggetti Geometry OM di XPS](xps-object-model-geometry-objects.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**Interfaccia IXpsOMDashCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)
</dt> <dt>

[**Interfaccia IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)
</dt> </dl>

 

 




