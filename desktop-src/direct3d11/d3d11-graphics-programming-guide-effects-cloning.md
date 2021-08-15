---
title: Clonazione di un effetto
description: La clonazione di un effetto crea una seconda copia quasi identica dell'effetto.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195b4e9a42e595558acc4c512f8662c11b2acde7873e123b242ee272eeea7e8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538005"
---
# <a name="cloning-an-effect"></a>Clonazione di un effetto

La clonazione di un effetto crea una seconda copia quasi identica dell'effetto. Per una spiegazione del motivo per cui non è esatto, vedere il qualificatore singolo seguente. Una seconda copia di un effetto è utile quando si vuole usare il framework effetti su più thread, poiché il runtime dell'effetto non è thread-safe per mantenere prestazioni elevate.

Poiché anche i contesti di dispositivo sono non thread-safe, thread diversi devono passare contesti di dispositivo diversi al metodo ID3DX11EffectPass::Apply.

Un effetto può essere clonato con la sintassi seguente:


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



Nell'esempio precedente la copia clonata incapsula lo stesso stato dell'effetto originale, indipendentemente dallo stato in cui si trova l'effetto originale. In particolare:

1.  Se pEffect è ottimizzato, l'effetto pCloned è ottimizzato
2.  Se pEffect include alcune variabili gestite dall'utente, l'effetto pCloned avrà le stesse variabili gestite dall'utente (vedere la singola descrizione seguente)
3.  Tutti gli aggiornamenti delle variabili in sospeso (fino a quando non viene applicato lo stato del dispositivo Apply call updates) in pEffect saranno in sospeso in pClonedEffect

Gli oggetti dispositivo Direct3D 11 seguenti non sono modificabili o non sono mai aggiornati dal framework degli effetti, quindi l'effetto clonato punti agli stessi oggetti dell'effetto originale:

1.  Oggetti blocco di stato (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)
2.  Shader
3.  Istanze di classe
4.  Trame (senza includere buffer di trama)
5.  Viste di accesso non ordinate

Gli oggetti dispositivo Direct3D 11 seguenti non sono modificabili e modificati dal runtime dell'effetto (a meno che non siano gestiti dall'utente o singoli in un effetto clonato); le nuove copie di questi oggetti vengono create quando non sono singole:

1.  Buffer costanti
2.  Buffer di trama

## <a name="single-constant-buffers-and-texture-buffers"></a>Buffer costanti singoli e buffer di trama

Si noti che questa discussione si applica sia ai buffer costanti che alle trame, ma si presuppone che i buffer costanti siano facili da leggere.

In alcuni casi un buffer costante viene aggiornato solo da un thread, ma lo stato del dispositivo impostato dagli effetti clonati userà questi dati. Ad esempio, l'effetto principale può aggiornare le matrici world e view a cui fanno riferimento gli shader negli effetti clonati che non modificano il mondo e visualizzano le matrici. In questi casi, gli effetti clonati devono fare riferimento al buffer costante corrente anziché ricrearlo.

Esistono due modi per ottenere questo risultato desiderato:

1.  Usare ID3DX11EffectConstantBuffer::SetConstantBuffer sull'effetto clonato per renderlo gestito dall'utente
2.  Contrassegnare il buffer costante come "singolo" nel codice HLSL, forzando il runtime dell'effetto a considerare come gestito dall'utente dopo la clonazione

Esistono due differenze tra i due metodi precedenti. In primo luogo, nel metodo 1 verrà creato un nuovo OGGETTO ID3D11Buffer e l'utente prima della chiamata a SetConstantBuffer. Inoltre, dopo aver chiamato UndoSetConstantBuffer nell'effetto clonato, la variabile nel metodo 1 farà riferimento al buffer appena creato (gli effetti verranno aggiornati su Apply), mentre la variabile nel metodo 2 continuerà a puntare al buffer originale (non aggiornandolo in Apply).

Vedere l'esempio seguente in HLSL:


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



Durante la clonazione, l'effetto clonato creerà un nuovo OGGETTO ID3D11Buffer per ObjectData e ne riempirà il contenuto in Applica, ma farà riferimento all'ID3D11Buffer originale per ViewData. Il singolo qualificatore può essere ignorato nel processo di clonazione impostando il flag D3DX11 \_ EFFECT \_ CLONE FORCE \_ \_ NONSINGLE.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




