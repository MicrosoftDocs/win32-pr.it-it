---
title: Effetto Atlas
description: È possibile usare questo effetto per restituire una parte di un'immagine ma mantenere l'area esterna alla parte da usare nelle operazioni successive.
ms.assetid: D35E32CB-4DF7-408F-A717-1E421DDC8763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f9e1d4c6df0698d47a35eb2cbdaf670b98ed125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478233"
---
# <a name="atlas-effect"></a>Effetto Atlas

È possibile usare questo effetto per restituire una parte di un'immagine ma mantenere l'area esterna alla parte da usare nelle operazioni successive.

Il CLSID per questo effetto è CLSID \_ D2D1Atlas.

L'effetto Atlas è utile se si desidera caricare un'immagine di grandi dimensioni costituita da molte immagini più piccole, ad esempio vari frame di uno sprite.

Per creare l'output, effettuare le operazioni seguenti:

1.  Ritaglia l'input nella proprietà *InputRect* specificata.
2.  Converte l'origine del risultato in (0,0).

> [!Note]  
> La proprietà *InputPaddingRect* deve essere maggiore solo se e solo se i pixel tra i due rettangoli sono di colore nero trasparente nell'input. Questo può comportare l'esecuzione di Direct2D del grafo in modo più ottimale.

 

Di seguito è riportato un esempio dell'effetto. Questa immagine è piccola e semplice a scopo illustrativo.

![immagine di input.](images/atlas.png)

L'immagine precedente è l'input dell'effetto. Il codice qui crea un effetto Atlas, imposta l'input, imposta il rettangolo di input, quindi disegna l'output.


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



Il codice precedente seleziona un rettangolo intorno al secondo triangolo. La spaziatura interna viene ignorata. Di seguito è illustrata l'immagine risultante.

![immagine di output.](images/atlas2.png)

> [!Note]  
> Si tratta di una situazione in cui è possibile scegliere di specificare un *InputPaddingRect* perché il riempimento è nero trasparente. Il rettangolo sarà `D2D1::Vector4F(size + (padding * 2), 0, size + padding, size + padding);` .

 

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                             | Descrizione                                                                                                                                                                  |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InputRect<br/> D2D1 \_ Atlas \_ prop \_ input \_ Rect<br/>                 | Parte dell'immagine passata all'effetto successivo.<br/> Il tipo è D2D1 \_ vector \_ 4F.<br/> Il valore predefinito è (-FLT \_ Max,-flt \_ Max, flt \_ Max, flt \_ max). <br/> |
| InputPaddingRect<br/> \_Rettangolo di \_ \_ riempimento input \_ d2d1 Atlas Prop \_<br/> | Dimensioni massime campionate per il rettangolo di output.<br/> Il tipo è D2D1 \_ vector \_ 4F.<br/> Il valore predefinito è (-FLT \_ Max,-flt \_ Max, flt \_ Max, flt \_ max).<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Intestazione                   | d2d1effects. h                                                                      |
| Libreria                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

