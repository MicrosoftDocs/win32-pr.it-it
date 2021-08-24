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
ms.openlocfilehash: 51383770b8eb0c5dca5efbb5f1756bee81ece506c0e92337e9df9a60eb0a8aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726731"
---
# <a name="inkd2drenderer-class"></a>Classe InkD2DRenderer

Implementa [**l'interfaccia IInkD2DRenderer.**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer)

Un oggetto [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) consente il rendering dei tratti input penna nel contesto di dispositivo Direct2D designato di un'app Universal Windows, anziché nel controllo [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) predefinito.

## <a name="members"></a>Membri

La **classe InkD2DRenderer** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **InkD2DRenderer** include anche questi tipi di membri:

- [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe InkD2DRenderer** include questi metodi.

| Metodo                              | Descrizione                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [**Disegna**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | Esegue il rendering del tratto input penna nel contesto di dispositivo Direct2D designato dell'app.<br/> |

## <a name="creationaccess-functions"></a>Creazione di \\ funzioni di accesso

Chiamare [<strong>CoCreateInstance con</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) l'identificatore <strong>di classe InkD2DRenderer</strong> per recuperare un riferimento all'oggetto.

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a>Esempio

Questo frammento di codice del file "SceneComposer.cpp" dell'esempio di input penna complesso illustra il rendering di una raccolta di tratti input penna in un contesto di dispositivo Direct2D. [](/samples/microsoft/windows-universal-samples/complexink/)

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

Questo frammento di codice del file "InkRenderer.cpp" dell'esempio di input penna complesso mostra il metodo Render (chiamato nel frammento precedente) che chiama il metodo [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) per il rendering dei tratti. [](/samples/microsoft/windows-universal-samples/complexink/)

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
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>Inkrenderer.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Inkrenderer.idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkD2DRenderer è definito come 4044e60c-7b01-4671-a97c-04e0210a07a5<br/>         |

## <a name="related-topics"></a>Argomenti correlati

[Renderer input penna,](ink-renderer.md) [interazioni con penna e stilo,](/windows/uwp/design/input/pen-and-stylus-interactions)esempio di analisi dell'input [penna,](/samples/microsoft/windows-universal-samples/inkanalysis/) [esempio di input penna semplice,](/samples/microsoft/windows-universal-samples/simpleink/) [esempio di input penna complesso](/samples/microsoft/windows-universal-samples/complexink/)
