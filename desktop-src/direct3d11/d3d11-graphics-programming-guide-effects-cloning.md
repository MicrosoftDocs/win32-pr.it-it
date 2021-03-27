---
title: Clonazione di un effetto
description: La clonazione di un effetto crea una seconda copia pressoché identica dell'effetto.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68607d3cc9f00a346fcfa65c255f3caa51dea384
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711704"
---
# <a name="cloning-an-effect"></a>Clonazione di un effetto

La clonazione di un effetto crea una seconda copia pressoché identica dell'effetto. Per una spiegazione del motivo per cui non è esatto, vedere il seguente qualificatore singolo. Una seconda copia di un effetto è utile quando si desidera utilizzare il Framework degli effetti su più thread, poiché il runtime di effetto non è thread-safe per garantire prestazioni elevate.

Poiché i contesti di dispositivo sono anche non thread-safe, i thread diversi devono passare contesti di dispositivo diversi al metodo ID3DX11EffectPass:: Apply.

È possibile clonare un effetto con la sintassi seguente:


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



Nell'esempio precedente, la copia clonata incapsula lo stesso stato dell'effetto originale, indipendentemente dallo stato in cui si trova l'effetto originale. In particolare:

1.  Se pEffect è ottimizzato, l'effetto pCloned è ottimizzato
2.  Se pEffect dispone di alcune variabili gestite dall'utente, l'effetto pCloned avrà le stesse variabili gestite dall'utente (vedere la descrizione singola riportata di seguito)
3.  Eventuali aggiornamenti di variabili in sospeso (fino a quando una chiamata Apply aggiorna lo stato del dispositivo) in pEffect sarà in sospeso in pClonedEffect

Gli oggetti dispositivo Direct3D 11 seguenti non sono modificabili o non vengono mai aggiornati dal framework degli effetti, quindi l'effetto clonato punterà sugli stessi oggetti dell'effetto originale:

1.  Oggetti Block di stato (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)
2.  Shader
3.  Istanze di classe
4.  Trame (esclusi i buffer di trama)
5.  Viste di accesso non ordinate

Gli oggetti dispositivo Direct3D 11 seguenti sono sia non modificabili che modificati dal runtime degli effetti (a meno che non sia gestito dall'utente o singolo in un effetto clonato); le nuove copie di questi oggetti vengono create quando non sono singole:

1.  Buffer costanti
2.  Buffer di trama

## <a name="single-constant-buffers-and-texture-buffers"></a>Buffer costanti singoli e buffer di trama

Si noti che questa discussione si applica sia ai buffer costanti che alle trame, ma si presuppone che i buffer costanti siano facilmente leggibili.

In alcuni casi è possibile che un buffer costante venga aggiornato da un solo thread, ma questi dati verranno utilizzati dallo stato del dispositivo impostato dagli effetti clonati. Ad esempio, l'effetto principale può aggiornare le matrici World e View a cui viene fatto riferimento dagli shader negli effetti clonati che non modificano le matrici World e View. In questi casi, è necessario che gli effetti clonati facciano riferimento al buffer costante corrente anziché ricrearne uno.

Esistono due modi per ottenere questo risultato desiderato:

1.  Usare ID3DX11EffectConstantBuffer:: SetConstantBuffer per l'effetto clonato per renderlo gestito dall'utente
2.  Contrassegnare il buffer costante come "singolo" nel codice HLSL, forzando il runtime di effetto a considerarlo come gestito dall'utente dopo la clonazione

Esistono due differenze tra i due metodi precedenti. Per prima cosa, nel metodo 1, viene creato un nuovo ID3D11Buffer e l'utente prima della chiamata a SetConstantBuffer. Inoltre, dopo aver chiamato UndoSetConstantBuffer nell'effetto clonato, la variabile nel metodo 1will punta al buffer appena creato (gli effetti verranno aggiornati su Apply), mentre la variabile nel metodo 2 continuerà a puntare al buffer originale (senza aggiornarlo all'applicazione).

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



Durante la clonazione, l'effetto clonato creerà un nuovo ID3D11Buffer per ObjectData e riempirà il relativo contenuto su Apply, ma fa riferimento al ID3D11Buffer originale per ViewData. Il qualificatore singolo può essere ignorato nel processo di clonazione impostando il \_ flag D3DX11 Effect \_ Clone \_ Force \_ unsingle flag.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Effetti (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




