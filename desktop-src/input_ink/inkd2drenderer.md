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
# <a name="inkd2drenderer-class"></a><span data-ttu-id="05497-103">Classe InkD2DRenderer</span><span class="sxs-lookup"><span data-stu-id="05497-103">InkD2DRenderer class</span></span>

<span data-ttu-id="05497-104">Implementa l'interfaccia [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) .</span><span class="sxs-lookup"><span data-stu-id="05497-104">Implements the [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) interface.</span></span>

<span data-ttu-id="05497-105">Un oggetto [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) consente il rendering dei tratti di input penna nel contesto di periferica Direct2D designato di un'app di Windows universale, anziché il controllo [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) predefinito.</span><span class="sxs-lookup"><span data-stu-id="05497-105">An [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span>

## <a name="members"></a><span data-ttu-id="05497-106">Membri</span><span class="sxs-lookup"><span data-stu-id="05497-106">Members</span></span>

<span data-ttu-id="05497-107">La classe **InkD2DRenderer** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="05497-107">The **InkD2DRenderer** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="05497-108">**InkD2DRenderer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="05497-108">**InkD2DRenderer** also has these types of members:</span></span>

- [<span data-ttu-id="05497-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="05497-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="05497-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="05497-110">Methods</span></span>

<span data-ttu-id="05497-111">La classe **InkD2DRenderer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="05497-111">The **InkD2DRenderer** class has these methods.</span></span>

| <span data-ttu-id="05497-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="05497-112">Method</span></span>                              | <span data-ttu-id="05497-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05497-113">Description</span></span>                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="05497-114">**Disegna**</span><span class="sxs-lookup"><span data-stu-id="05497-114">**Draw**</span></span>](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | <span data-ttu-id="05497-115">Esegue il rendering del tratto dell'input penna nel contesto di periferica Direct2D designato dell'app.</span><span class="sxs-lookup"><span data-stu-id="05497-115">Renders the ink stroke to the designated Direct2D device context of the app.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="05497-116">Funzioni di accesso per la creazione \\</span><span class="sxs-lookup"><span data-stu-id="05497-116">Creation\\Access Functions</span></span>

<span data-ttu-id="05497-117">Chiamare [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con l'identificatore di classe <strong>InkD2DRenderer</strong> per recuperare un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="05497-117">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkD2DRenderer</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a><span data-ttu-id="05497-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="05497-118">Examples</span></span>

<span data-ttu-id="05497-119">Questo frammento di codice del file "SceneComposer. cpp" dell' [esempio di Inking complesso](/samples/microsoft/windows-universal-samples/complexink/) illustra il rendering di una raccolta di tratti di input penna in un contesto di dispositivo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="05497-119">This snippet from the "SceneComposer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) demonstrates the rendering of a collection of ink strokes to a Direct2D device context.</span></span>

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

<span data-ttu-id="05497-120">Questo frammento di codice del file "InkRenderer. cpp" dell' [esempio di Inking complesso](/samples/microsoft/windows-universal-samples/complexink/) illustra il metodo Render (chiamato nel frammento di codice precedente) che chiama il metodo di [**traccia**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) per il rendering dei tratti.</span><span class="sxs-lookup"><span data-stu-id="05497-120">This snippet from the "InkRenderer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) shows the Render method (called in the previous snippet) that calls the [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) method for rendering the strokes.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="05497-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05497-121">Requirements</span></span>

| <span data-ttu-id="05497-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="05497-122">Requirement</span></span> | <span data-ttu-id="05497-123">Valore</span><span class="sxs-lookup"><span data-stu-id="05497-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="05497-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05497-124">Minimum supported client</span></span><br/> | <span data-ttu-id="05497-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="05497-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="05497-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05497-126">Minimum supported server</span></span><br/> | <span data-ttu-id="05497-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="05497-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="05497-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05497-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="05497-129"><dt>InkRenderer. h</dt></span><span class="sxs-lookup"><span data-stu-id="05497-129"><dt>Inkrenderer.h</dt></span></span> </dl>   |
| <span data-ttu-id="05497-130">IDL</span><span class="sxs-lookup"><span data-stu-id="05497-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="05497-131"><dt>InkRenderer. idl</dt></span><span class="sxs-lookup"><span data-stu-id="05497-131"><dt>Inkrenderer.idl</dt></span></span> </dl> |
| <span data-ttu-id="05497-132">IID</span><span class="sxs-lookup"><span data-stu-id="05497-132">IID</span></span><br/>                      | <span data-ttu-id="05497-133">IID \_ IInkD2DRenderer è definito come 4044e60c-7B01-4671-a97c-04e0210a07a5</span><span class="sxs-lookup"><span data-stu-id="05497-133">IID\_IInkD2DRenderer is defined as 4044e60c-7b01-4671-a97c-04e0210a07a5</span></span><br/>         |

## <a name="related-topics"></a><span data-ttu-id="05497-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="05497-134">Related topics</span></span>

<span data-ttu-id="05497-135">[Renderer di input](ink-renderer.md)penna, [interazioni di penna e stilo](/windows/uwp/design/input/pen-and-stylus-interactions), [esempio di analisi dell'input penna](/samples/microsoft/windows-universal-samples/inkanalysis/), esempio di [Inking semplice](/samples/microsoft/windows-universal-samples/simpleink/), [esempio di Inking complesso](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="05497-135">[Ink renderer](ink-renderer.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
