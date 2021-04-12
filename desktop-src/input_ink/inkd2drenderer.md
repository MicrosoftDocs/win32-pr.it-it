---
description: Implementa l'interfaccia IInkD2DRenderer.
ms.assetid: d1bd910d-ce64-4424-a0e1-4f55110b0265
title: Classe InkD2DRenderer
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkD2DRenderer
api_type:
- COM
api_location:
- Inkrenderer.idl
ms.openlocfilehash: 1649d52c2e9098513c115daaf295c4005e890b8e
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104234459"
---
# <a name="inkd2drenderer-class"></a>Classe InkD2DRenderer

Implementa l'interfaccia [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) .

Un oggetto [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) consente il rendering dei tratti di input penna nel contesto di periferica Direct2D designato di un'app di Windows universale, anziché il controllo [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) predefinito.

## <a name="members"></a>Membri

La classe **InkD2DRenderer** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **InkD2DRenderer** dispone anche di questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

La classe **InkD2DRenderer** dispone di questi metodi.

| Metodo                              | Descrizione                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [**Disegna**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | Esegue il rendering del tratto dell'input penna nel contesto di periferica Direct2D designato dell'app.<br/> |

## <a name="creationaccess-functions"></a>Funzioni di accesso per la creazione \\

Chiamare [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con l'identificatore di classe <strong>InkD2DRenderer</strong> per recuperare un riferimento all'oggetto.

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a>Esempio

Questo frammento di codice del file "SceneComposer. cpp" dell' [esempio di Inking complesso](/samples/microsoft/windows-universal-samples/complexink/) illustra il rendering di una raccolta di tratti di input penna in un contesto di dispositivo Direct2D.

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

Questo frammento di codice del file "InkRenderer. cpp" dell' [esempio di Inking complesso](/samples/microsoft/windows-universal-samples/complexink/) illustra il metodo Render (chiamato nel frammento di codice precedente) che chiama il metodo di [**traccia**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) per il rendering dei tratti.

```C++
void InkRenderer::Render(
    Platform::Collections::Vector<
        Windows::UI::Input::Inking::InkStroke^>^ strokes,
        Microsoft::WRL::ComPtr<ID2D1DeviceContext> d2dContext)
{
    HRESULT hr = S_OK;
    if (_spInkD2DRenderer != nullptr)
    {
        if (strokes != nullptr && strokes->Size > 0)
        {
            // Cast the stroke collection into IUnknown to call Inkd2dRenderer
            ComPtr<IUnknown> spUnkStrokes = 
                reinterpret_cast<IUnknown*>(reinterpret_cast<__abi_IUnknown*>(strokes));
            hr = _spInkD2DRenderer->Draw(d2dContext.Get(), spUnkStrokes.Get(), false);
            if (FAILED(hr))
            {
                DX::ThrowIfFailed(hr);
            }
        }
    }
}
```

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>InkRenderer. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>InkRenderer. idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkD2DRenderer è definito come 4044e60c-7B01-4671-a97c-04e0210a07a5<br/>         |

## <a name="related-topics"></a>Argomenti correlati

[Renderer di input](ink-renderer.md)penna, [interazioni di penna e stilo](/windows/uwp/design/input/pen-and-stylus-interactions), [esempio di analisi dell'input penna](/samples/microsoft/windows-universal-samples/inkanalysis/), esempio di [Inking semplice](/samples/microsoft/windows-universal-samples/simpleink/), [esempio di Inking complesso](/samples/microsoft/windows-universal-samples/complexink/)
