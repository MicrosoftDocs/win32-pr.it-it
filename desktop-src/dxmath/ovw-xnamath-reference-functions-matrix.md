---
description: Elenca le funzioni di matrice fornite da DirectXMath.
ms.assetid: d59d0dcc-deae-3f7e-55c5-0c5ff383343b
title: Funzioni della matrice della libreria DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a91ecdef8389bf60594d370c2b3de01995bc1169
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826766"
---
# <a name="directxmath-library-matrix-functions"></a>Funzioni della matrice della libreria DirectXMath

Elenca le funzioni di matrice fornite da DirectXMath.

> [!Note]  
> DirectXMath offre entrambe le versioni mancino e destro delle funzioni di matrice con "mania", ma presuppone sempre un formato di riga principale.

 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                               | Descrizione                                                                                                                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**XMMatrixAffineTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)<br/>                     | Compila una matrice di trasformazione affine.<br/>                                                                                     |
| [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)<br/>                 | Compila una matrice di trasformazione affine 2D nel piano xy. <br/>                                                                  |
| [**XMMatrixDecompose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)<br/>                                           | Suddivide una matrice di trasformazione 3D generale nei relativi componenti scalari, rotazionali e traslazionali.<br/>                   |
| [**XMMatrixDeterminant**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)<br/>                                       | Calcola il determinante di una matrice.<br/>                                                                                       |
| [**XMMatrixIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)<br/>                                             | Compila la matrice di identità.<br/>                                                                                                 |
| [**XMMatrixInverse**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)<br/>                                               | Calcola l'inverso di una matrice.<br/>                                                                                           |
| [**XMMatrixIsIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisidentity)<br/>                                         | Verifica se una matrice è la matrice di identità.<br/>                                                                              |
| [**XMMatrixIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisinfinite)<br/>                                         | Verifica se uno degli elementi di una matrice è infinito positivo o negativo.<br/>                                            |
| [**XMMatrixIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisnan)<br/>                                                   | Verifica se uno degli elementi di una matrice è NaN.<br/>                                                                      |
| [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)<br/>                                             | Crea una matrice di visualizzazione per un sistema di coordinate sinistrorso usando posizione della telecamera, direzione verso l'alto e punto focale.<br/>       |
| [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)<br/>                                             | Crea una matrice di visualizzazione per un sistema di coordinate destrorso usando posizione della telecamera, direzione verso l'alto e punto focale.<br/>      |
| [**XMMatrixLookToLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktolh)<br/>                                             | Crea una matrice di visualizzazione per un sistema di coordinate sinistrorso usando posizione della telecamera, direzione verso l'alto e direzione della telecamera.<br/>  |
| [**XMMatrixLookToRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktorh)<br/>                                             | Crea una matrice di visualizzazione per un sistema di coordinate destrorso usando posizione della telecamera, direzione verso l'alto e direzione della telecamera.<br/> |
| [**XMMatrixMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)<br/>                                             | Calcola il prodotto di due matrici.<br/>                                                                                       |
| [**XMMatrixMultiplyTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)<br/>                           | Calcola la trasposizione del prodotto di due matrici.<br/>                                                                      |
| [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)<br/>                                 | Crea una matrice di proiezione ortogonale per un sistema di coordinate sinistrorso.<br/>                                                 |
| [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)<br/>               | Crea una matrice di proiezione ortogonale personalizzata per un sistema di coordinate sinistrorso.<br/>                                           |
| [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)<br/>               | Crea una matrice di proiezione ortogonale personalizzata per un sistema di coordinate destrorso.<br/>                                          |
| [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)<br/>                                 | Crea una matrice di proiezione ortogonale per un sistema di coordinate destrorso.<br/>                                                |
| [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)<br/>                             | Crea una matrice di proiezione prospettica sinistrorsa basata su un campo visivo.<br/>                                                |
| [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)<br/>                             | Crea una matrice di proiezione prospettica destrorsa basata su un campo visivo.<br/>                                               |
| [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)<br/>                                   | Crea una matrice di proiezione prospettica sinistrorsa.<br/>                                                                         |
| [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)<br/>                 | Crea una versione personalizzata di una matrice di proiezione prospettica sinistrorsa.<br/>                                                     |
| [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)<br/>                 | Crea una versione personalizzata di una matrice di proiezione prospettica destrorsa.<br/>                                                    |
| [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)<br/>                                   | Crea una matrice di proiezione prospettica destrorsa.<br/>                                                                        |
| [**XMMatrixReflect**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)<br/>                                               | Compila una matrice di trasformazione progettata per riflettere i vettori attraverso un piano specificato.<br/>                                           |
| [**XMMatrixRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)<br/>                                     | Compila una matrice che ruota intorno a un asse arbitrario.<br/>                                                                      |
| [**XMMatrixRotationNormal**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationnormal)<br/>                                 | Compila una matrice che ruota intorno a un vettore normale arbitrario.<br/>                                                             |
| [**XMMatrixRotationQuaternion**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)<br/>                         | Compila una matrice di rotazione da un quaternione.<br/>                                                                                 |
| [**XMMatrixRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw)<br/>                     | Compila una matrice di rotazione in base a un passo, un yaw e un rollio (angoli Eulero).<br/>                                              |
| [**XMMatrixRotationRollPitchYawFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyawfromvector)<br/> | Compila una matrice di rotazione basata su un vettore contenente gli angoli eulero (passo, yaw e rollio).<br/>                              |
| [**XMMatrixRotationX**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)<br/>                                           | Compila una matrice che ruota intorno all'asse x.<br/>                                                                             |
| [**XMMatrixRotationY**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)<br/>                                           | Compila una matrice che ruota intorno all'asse y.<br/>                                                                             |
| [**XMMatrixRotationZ**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)<br/>                                           | Compila una matrice che ruota intorno all'asse z.<br/>                                                                             |
| [**XMMatrixScaling**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)<br/>                                               | Compila una matrice che viene ridimensionata lungo l'asse x, l'asse y e l'asse z.<br/>                                                           |
| [**XMMatrixScalingFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscalingfromvector)<br/>                           | Compila una matrice di ridimensionamento da un vettore 3D.<br/>                                                                                   |
| [**XMMatrixSet**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixset)<br/>                                                       | Crea una matrice con **valori float.**<br/>                                                                                     |
| [**XMMatrixShadow**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)<br/>                                                 | Compila una matrice di trasformazione che appiattise la geometria in un piano.<br/>                                                         |
| [**XMMatrixTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)<br/>                                 | Compila una matrice di trasformazione.<br/>                                                                                             |
| [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)<br/>                             | Compila una matrice di trasformazione 2D nel piano xy.<br/>                                                                          |
| [**XMMatrixTranslation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)<br/>                                       | Compila una matrice di traslazione dagli offset specificati.<br/>                                                                     |
| [**XMMatrixTranslationFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslationfromvector)<br/>                   | Compila una matrice di traslazione da un vettore.<br/>                                                                                  |
| [**XMMatrixTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)<br/>                                           | Calcola il trasposto di una matrice.<br/>                                                                                         |
| [**XMMatrixVectorTensorProduct**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixvectortensorproduct)<br/>                                           | Calcola il prodotto tensore esterno di 2 vettori.<br/>                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni della libreria DirectXMath](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
