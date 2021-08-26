---
title: Effetto Atlas
description: È possibile usare questo effetto per l'output di una parte di un'immagine, ma mantenere l'area al di fuori della parte per l'uso nelle operazioni successive.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b0d55e7751ef73d8f6bdff65a6ae5d5933695600a1003b9c4a010231628019
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929052"
---
# <a name="atlas-effect"></a>Effetto Atlas

È possibile usare questo effetto per l'output di una parte di un'immagine, ma mantenere l'area al di fuori della parte per l'uso nelle operazioni successive.

Il CLSID per questo effetto è CLSID \_ D2D1Atlas.

L'effetto Atlas è utile se si vuole caricare un'immagine di grandi dimensioni che è costituito da molte immagini più piccole, ad esempio vari fotogrammi di uno sprite.

Per creare l'output, l'effetto è il seguente:

1.  Ritaglia l'input per la *proprietà InputRect* specificata.
2.  Converte l'origine del risultato in (0,0).

> [!Note]  
> La *proprietà InputPaddingRect* deve essere maggiore solo se e solo se i pixel tra i due rettangoli sono di colore nero trasparente nell'input. Ciò può comportare l'esecuzione ottimale del grafo da parte di Direct2D.

 

Di seguito è riportato un esempio dell'effetto. Questa immagine è piccola e semplice a scopo illustrativo.

![immagine di input.](images/atlas.png)

L'immagine precedente è l'input per l'effetto. Il codice crea un effetto Atlas, imposta l'input, imposta il rettangolo di input e quindi disegna l'output.


```C++
ComPtr<ID2D1Effect> atlasEffect;

// Create the Atlas Effect.
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Atlas, &atlasEffect));

// Set the input.
atlasEffect->SetInputEffect(0, inputImage.Get());

// The images here are 150 x 150 pixels.
float size = 150.0f;

// Compensate for the padding between images.
float padding = 10.0f;

// The input rectangle.  150 x 150 pixels with 10 pixel padding
D2D1_Vector_4F inputRect = D2D1::Vector4F(size + (padding * 2), padding, size, size);

DX::ThrowIfFailed(atlasEffect->SetValue(D2D1_ATLAS_PROP_INPUT_RECT, inputRect));

// Draw the image
m_d2dContext->DrawImage(atlasEffect.Get());
```



Il codice precedente seleziona un rettangolo intorno al secondo triangolo. La spaziatura interna intorno a esso viene ignorata. Ecco l'immagine risultante.

![immagine di output.](images/atlas2.png)

> [!Note]  
> Si tratta di una situazione in cui è possibile scegliere di specificare *un inputPaddingRect* perché il riempimento è nero trasparente. Il rettangolo sarebbe `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .

 

## <a name="effect-properties"></a>Proprietà degli effetti



| Enumerazione del nome visualizzato e dell'indice                                             | Descrizione                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InputRect<br/> D2D1 \_ ATLAS \_ PROP \_ INPUT \_ RECT<br/>                 | Parte dell'immagine passata all'effetto successivo.<br/> Il tipo è D2D1 \_ VECTOR \_ 4F.<br/> Il valore predefinito è (-FLT \_ MAX, -FLT \_ MAX, FLT \_ MAX, FLT \_ MAX). <br/> |
| InputPaddingRect<br/> D2D1 \_ ATLAS \_ PROP \_ INPUT \_ PADDING \_ RECT<br/> | Dimensione massima campionata per il rettangolo di output.<br/> Il tipo è D2D1 \_ VECTOR \_ 4F.<br/> Il valore predefinito è (-FLT \_ MAX, -FLT \_ MAX, FLT \_ MAX, FLT \_ MAX).<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

