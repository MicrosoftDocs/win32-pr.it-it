---
description: In Direct3D, i vertici descrivono la posizione e l'orientamento. Ogni vertice in una primitiva viene descritto da un vettore che fornisce la posizione, il colore, le coordinate della trama e un vettore normale che ne fornisce l'orientamento.
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: Vettori, vertici e quaternioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601b6a71dcb00356d4de4637a6aabb1eba5c02e49c62380b32732351d15bfcb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290443"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a>Vettori, vertici e quaternioni (Direct3D 9)

In Direct3D, i vertici descrivono la posizione e l'orientamento. Ogni vertice in una primitiva viene descritto da un vettore che fornisce la posizione, il colore, le coordinate della trama e un vettore normale che ne fornisce l'orientamento.

I quaternioni aggiungono un quarto elemento ai valori \[ x, y, z \] che definiscono un vettore a tre componenti. I quaternioni sono un'alternativa ai metodi matrice che vengono in genere usati per le rotazioni 3D. Un quaternione rappresenta un asse nello spazio 3D e una rotazione intorno a tale asse. Ad esempio, un quaternione potrebbe rappresentare un asse (1,1,2) e una rotazione di 1 radiante. I quaternioni trasportano informazioni preziose, ma la loro vera potenza deriva dalle due operazioni che è possibile eseguire su di essi: composizione e interpolazione.

L'esecuzione della composizione sui quaternioni è simile alla combinazione. La composizione di due quaternioni è illustrata come nell'illustrazione seguente.

![illustrazione della notazione quaternione](images/quateq.png)

La composizione di due quaternioni applicati a una geometria significa "ruotare la geometria intorno all'asse Y per rotazione, quindi ruotarla intorno all'asse₁ per rotazione₁". In questo caso, Q rappresenta una rotazione intorno a un singolo asse che è il risultato dell'applicazione di q₁ alla geometria.

Usando l'interpolazione quaternione, un'applicazione può calcolare un percorso uniforme e ragionevole da un asse e un orientamento a un altro. Di conseguenza, l'interpolazione tra q₁ e qazioni offre un modo semplice per aggiungere un'animazione da un orientamento a un altro.

Quando si usano la composizione e l'interpolazione insieme, offrono un modo semplice per modificare una geometria in modo che sia complessa. Si supponga, ad esempio, di avere una geometria che si vuole ruotare in base a un determinato orientamento. Si sa che si vuole ruotare il quaternione in gradi r rispetto all'asse, quindi ruotarlo r₁ gradi intorno all'asse₁ ma non si conosce il quaternione finale. Usando la composizione, è possibile combinare le due rotazioni sulla geometria per ottenere un singolo quaternione che rappresenta il risultato. È quindi possibile eseguire l'interpolazione dal quaternione originale al quaternione composto per ottenere una transizione uniforme da un quaternione all'altro.

La libreria di utilità D3DX include funzioni che consentono di lavorare con i quaternioni. Ad esempio, la funzione [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) aggiunge un valore di rotazione a un vettore che definisce un asse di rotazione e restituisce il risultato in un quaternione definito da una [**struttura D3DXQUATERNION.**](d3dxquaternion.md) Inoltre, la funzione [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) compone quaternioni e [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) esegue l'interpolazione lineare sferica tra due quaternioni.

Le applicazioni Direct3D possono usare le funzioni seguenti per semplificare l'attività di utilizzo dei quaternioni.

-   [**D3DXQuaternionBaryCentric**](d3dxquaternionbarycentric.md)
-   [**D3DXQuaternionConjugate**](d3dxquaternionconjugate.md)
-   [**D3DXQuaternionDot**](d3dxquaterniondot.md)
-   [**D3DXQuaternionExp**](d3dxquaternionexp.md)
-   [**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
-   [**D3DXQuaternionInverse**](d3dxquaternioninverse.md)
-   [**D3DXQuaternionIsIdentity**](d3dxquaternionisidentity.md)
-   [**D3DXQuaternionLength**](d3dxquaternionlength.md)
-   [**D3DXQuaternionLengthSq**](d3dxquaternionlengthsq.md)
-   [**D3DXQuaternionLn**](d3dxquaternionln.md)
-   [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
-   [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md)
-   [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
-   [**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
-   [**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
-   [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md)
-   [**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
-   [**D3DXQuaternionToAxisAngle**](d3dxquaterniontoaxisangle.md)

Le applicazioni Direct3D possono usare le funzioni seguenti per semplificare l'attività di utilizzo di vettori a tre componenti.

-   [**D3DXVec3Add**](d3dxvec3add.md)
-   [**D3DXVec3BaryCentric**](d3dxvec3barycentric.md)
-   [**D3DXVec3CatmullRom**](d3dxvec3catmullrom.md)
-   [**D3DXVec3Cross**](d3dxvec3cross.md)
-   [**D3DXVec3Dot**](d3dxvec3dot.md)
-   [**D3DXVec3Hermite**](d3dxvec3hermite.md)
-   [**D3DXVec3Length**](d3dxvec3length.md)
-   [**D3DXVec3LengthSq**](d3dxvec3lengthsq.md)
-   [**D3DXVec3Lerp**](d3dxvec3lerp.md)
-   [**D3DXVec3Maximize**](d3dxvec3maximize.md)
-   [**D3DXVec3Minimize**](d3dxvec3minimize.md)
-   [**D3DXVec3Normalize**](d3dxvec3normalize.md)
-   [**D3DXVec3Project**](d3dxvec3project.md)
-   [**D3DXVec3Scale**](d3dxvec3scale.md)
-   [**D3DXVec3Subtract**](d3dxvec3subtract.md)
-   [**D3DXVec3Transform**](d3dxvec3transform.md)
-   [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md)
-   [**D3DXVec3TransformNormal**](d3dxvec3transformnormal.md)
-   [**D3DXVec3Unproject**](d3dxvec3unproject.md)

Molte funzioni aggiuntive che semplificano le attività usando vettori a [](dx9-graphics-reference-d3dx-functions-math.md) due e quattro componenti sono incluse tra le funzioni matematiche fornite dalla libreria di utilità D3DX.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistemi di coordinate e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



