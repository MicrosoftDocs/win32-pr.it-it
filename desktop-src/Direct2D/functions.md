---
title: Funzioni Direct2D
description: Direct2D offre le funzioni seguenti.
ms.assetid: 1a7ae962-9b70-442c-a676-f172a2d9bfd3
keywords:
- Direct2D, funzioni
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 7df417bbaba8c442f61005b35900641c379da9d7b61fa91e898d41e0d73821d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874481"
---
# <a name="direct2d-functions"></a>Funzioni Direct2D

Direct2D offre le funzioni seguenti. Le funzioni aggiuntive sono definite nello spazio [dei nomi D2D1](d2d1-namespace.md).

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**D2D1ComputeMaximumScaleFactor**](/windows/desktop/api/d2d1_2/nf-d2d1_2-d2d1computemaximumscalefactor) | Calcola il fattore massimo in base al quale una determinata trasformazione può estendere qualsiasi vettore. |
| [**D2D1CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) | Crea un nuovo dispositivo Direct2D associato al dispositivo DXGI specificato.  |
| [**D2D1CreateDeviceContext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext) | Crea un nuovo contesto di dispositivo Direct2D associato a una superficie DXGI.  |
| [**D2D1CreateFactory(D2D1_FACTORY_TYPE,REFIID,void \* \* )**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory-r1) | Crea un oggetto factory che può essere usato per creare risorse Direct2D. |
| [**D2D1CreateFactory(D2D1_FACTORY_TYPE,REFIID,D2D1_FACTORY_OPTIONS \* ,void \* \* )**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) | Crea un oggetto factory che può essere usato per creare risorse Direct2D. |
| [**D2D1GetGradientMeshInteriorPointsFromCoonsPatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-d2d1getgradientmeshinteriorpointsfromcoonspatch) | Restituisce i punti interni per una patch di mesh sfumato in base ai punti che definiscono una patch Coons. |
| [**D2D1InvertMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1invertmatrix) | Tenta di invertire la matrice specificata. |
| [**D2D1IsMatrixInvertible**](/windows/desktop/api/d2d1/nf-d2d1-d2d1ismatrixinvertible) | Indica se la matrice specificata è invertibile. |
| [**D2D1MakeRotateMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makerotatematrix) | Crea una trasformazione di rotazione che ruota in base all'angolo specificato intorno al punto specificato. |
| [**D2D1MakeSkewMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makeskewmatrix) | Crea una trasformazione di inclinazione con l'angolo dell'asse x, l'angolo dell'asse y e il punto centrale specificati.  |
| [**operatore \* (const D2D1\MATRIX\3X2\F&,const D2D1\MATRIX\3X2\F&)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-setproduct) | Moltiplica due matrici e restituisce il risultato. |
| [**BlobGetter**](blobgetter.md) | Chiama un callback del getter della proprietà della funzione membro per una proprietà di tipo BLOB. |
| [**BlobSetter**](blobsetter.md) | Chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo BLOB. |
| [**DeducingBlobGetter**](deducingblobgetter.md) | Deduce la classe e gli argomenti e quindi chiama un callback del getter della proprietà della funzione membro per una proprietà di tipo BLOB. |
| [**DeducingBlobSetter**](deducingblobsetter.md) | Deduce la classe e gli argomenti e quindi chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo BLOB. |
| [**DeducingStringGetter**](deducingstringgetter.md) | Deduce la classe e gli argomenti e quindi chiama un callback del getter della proprietà della funzione membro per una proprietà di tipo stringa. |
| [**DeducingStringSetter**](deducingstringsetter.md) | Deduce la classe e gli argomenti e quindi chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo stringa. |
| [**DeducingValueGetter**](deducingvaluegetter.md) | Deduce la classe e gli argomenti e quindi chiama un callback del getter della proprietà della funzione membro per una proprietà di tipo valore. |
| [**DeducingValueSetter**](deducingvaluesetter.md) | Deduce la classe e gli argomenti e quindi chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo valore. |
| [**GetType**](/previous-versions/windows/desktop/legacy/hh847962(v=vs.85)) | Recupera il tipo della proprietà specificata. |
| [**StringGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringgetter) | Chiama un callback del getter della proprietà della funzione membro per una proprietà di tipo stringa. |
| [**StringSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringsetter) | Chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo stringa. |
| [**Oggetto ValueGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuegetter) | Chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo valore. |
| [**ValueSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuesetter) | Chiama un callback del setter di proprietà della funzione membro per una proprietà di tipo valore. |
| [**D2D1ConvertColorSpace**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1convertcolorspace) | Converte il colore specificato da uno spazio dei colori a un altro. |
| [**D2D1SinCos**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1sincos) | Restituisce il seno e il coseno di un angolo. |
| [**D2D1Tan**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1tan) | Restituisce la tangente di un angolo. |
| [**D2D1Vec3Length**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1vec3length) | Restituisce la lunghezza di un vettore tridimensionale. |
| [**PD2D1\PROPERTY\GET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_get_function) | Ottiene una proprietà da un effetto. |
| [**PD2D1\PROPERTY\SET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_set_function) | Imposta una proprietà su un effetto. |