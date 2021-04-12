---
description: La discussione sulla trasformazione globale introduce i concetti di base e fornisce informazioni dettagliate su come configurare una trasformazione globale.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: Trasformazione globale (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e192f8ce4350c767122ef60f3cd36777753d2e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401106"
---
# <a name="world-transform-direct3d-9"></a>Trasformazione globale (Direct3D 9)

La discussione sulla trasformazione globale introduce i concetti di base e fornisce informazioni dettagliate su come configurare una trasformazione globale.

## <a name="what-is-a-world-transform"></a>Che cos'è una trasformazione globale?

Una trasformazione globale modifica le coordinate dallo spazio del modello, in cui i vertici vengono definiti in relazione all'origine locale di un modello, allo spazio globale, in cui i vertici vengono definiti in relazione a un'origine comune a tutti gli oggetti in una scena. In sostanza, la trasformazione mondiale inserisce un modello nel mondo; quindi il nome. Nel diagramma seguente viene illustrata la relazione tra il sistema di coordinate globale e il sistema di coordinate locale di un modello.

![diagramma del modo in cui le coordinate globali e le coordinate locali sono correlate](images/worldcrd.png)

La trasformazione mondiale può includere qualsiasi combinazione di traslazioni, rotazioni e scalabilità.

## <a name="setting-up-a-world-matrix"></a>Configurazione di una matrice globale

Come per qualsiasi altra trasformazione, creare la trasformazione globale concatenando una serie di matrici in un'unica matrice che contiene la somma totale degli effetti. Nel caso più semplice, quando un modello si trova all'origine mondiale e gli assi delle coordinate locali sono orientati allo stesso modo dello spazio globale, la matrice globale è la matrice di identità. Più comunemente, la matrice globale è una combinazione di una traduzione nello spazio globale e possibilmente una o più rotazioni per trasformare il modello in base alle esigenze.

Nell'esempio seguente, da una classe di modello 3D fittizia scritta in C++, USA le funzioni di supporto incluse nella libreria di utilità D3DX per creare una matrice globale che include tre rotazioni per orientare un modello e una traduzione per rilocarlo rispetto alla relativa posizione nello spazio globale.


```
/*
 * For the purposes of this example, the following variables
 * are assumed to be valid and initialized.
 *
 * The m_xPos, m_yPos, m_zPos variables contain the model's
 * location in world coordinates.
 *
 * The m_fPitch, m_fYaw, and m_fRoll variables are floats that 
 * contain the model's orientation in terms of pitch, yaw, and roll
 * angles, in radians.
 */
 
void C3DModel::MakeWorldMatrix( D3DXMATRIX* pMatWorld )
{
    D3DXMATRIX MatTemp;  // Temp matrix for rotations.
    D3DXMATRIX MatRot;   // Final rotation matrix, applied to 
                         // pMatWorld.
 
    // Using the left-to-right order of matrix concatenation,
    // apply the translation to the object's world position
    // before applying the rotations.
    D3DXMatrixTranslation(pMatWorld, m_xPos, m_yPos, m_zPos);
    D3DXMatrixIdentity(&MatRot);

    // Now, apply the orientation variables to the world matrix
    if(m_fPitch || m_fYaw || m_fRoll) {
        // Produce and combine the rotation matrices.
        D3DXMatrixRotationX(&MatTemp, m_fPitch);         // Pitch
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationY(&MatTemp, m_fYaw);           // Yaw
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationZ(&MatTemp, m_fRoll);          // Roll
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
 
        // Apply the rotation matrices to complete the world matrix.
        D3DXMatrixMultiply(pMatWorld, &MatRot, pMatWorld);
    }
}
```



Dopo aver preparato la matrice globale, chiamare il metodo [**IDirect3DDevice9:: setransform**](/windows/desktop/api) per impostarlo, specificando la macro [**D3DTS \_ World**](d3dts-world.md) per il primo parametro.

> [!Note]  
> Direct3D usa le matrici World e View impostate per configurare diverse strutture di dati interne. Ogni volta che si imposta una nuova matrice World o View, il sistema ricalcola le strutture interne associate. L'impostazione frequente di queste matrici, ad esempio migliaia di volte per fotogramma, richiede molto tempo. È possibile ridurre al minimo il numero di calcoli necessari concatenando il mondo e visualizzare le matrici in una matrice di visualizzazione globale impostata come matrice globale e quindi impostando la matrice di visualizzazione sull'identità. Conserva le copie memorizzate nella cache di singole matrici e visualizza le matrici in modo che sia possibile modificare, concatenare e reimpostare la matrice globale in base alle esigenze. Per maggiore chiarezza, in questa documentazione gli esempi di Direct3D utilizzano raramente questa ottimizzazione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trasformazioni](transforms.md)
</dt> </dl>

 

 



