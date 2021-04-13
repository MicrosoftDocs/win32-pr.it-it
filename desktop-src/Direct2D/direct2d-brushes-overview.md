---
title: 'Panoramica dei pennelli '
description: Vengono descritti i diversi tipi di pennelli forniti da Direct2D.
ms.assetid: 7a31d9e7-0521-40ee-b2c1-592dfaf5301e
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 7c8b4c4762a03650f150a74d3207d12767e1fb4e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104399896"
---
# <a name="brushes-overview"></a><span data-ttu-id="d7289-103">Panoramica dei pennelli </span><span class="sxs-lookup"><span data-stu-id="d7289-103">Brushes overview</span></span>

<span data-ttu-id="d7289-104">In questa panoramica viene descritto come creare e utilizzare oggetti [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)e [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) per disegnare aree con colori a tinta unita, sfumature e bitmap.</span><span class="sxs-lookup"><span data-stu-id="d7289-104">This overview describes how to create and use [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) objects to paint areas with solid colors, gradients, and bitmaps.</span></span> <span data-ttu-id="d7289-105">Include le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7289-105">It contains the following sections.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d7289-106">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="d7289-106">Prerequisites</span></span>

<span data-ttu-id="d7289-107">In questa panoramica si presuppone che l'utente abbia familiarità con la struttura di un'applicazione Direct2D di base, come descritto in [creazione di una semplice applicazione Direct2D](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="d7289-107">This overview assumes that you are familiar with the structure of a basic Direct2D application, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="brush-types"></a><span data-ttu-id="d7289-108">Tipi di pennello</span><span class="sxs-lookup"><span data-stu-id="d7289-108">Brush types</span></span>

<span data-ttu-id="d7289-109">Un pennello "disegna" un'area con l'output.</span><span class="sxs-lookup"><span data-stu-id="d7289-109">A brush "paints" an area with its output.</span></span> <span data-ttu-id="d7289-110">Pennelli diversi hanno diversi tipi di output.</span><span class="sxs-lookup"><span data-stu-id="d7289-110">Different brushes have different types of output.</span></span> <span data-ttu-id="d7289-111">Direct2D fornisce quattro tipi di pennello: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) disegna un'area con un colore a tinta unita, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) con una sfumatura lineare, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) con una sfumatura radiale e [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) con una bitmap.</span><span class="sxs-lookup"><span data-stu-id="d7289-111">Direct2D provides four brush types: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints an area with a solid color, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) with a linear gradient, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) with a radial gradient, and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with a bitmap.</span></span>

> [!NOTE]  
> <span data-ttu-id="d7289-112">A partire da Windows 8, è anche possibile usare [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), che è simile a un pennello bitmap, ma è anche possibile usare le primitive.</span><span class="sxs-lookup"><span data-stu-id="d7289-112">Starting with Windows 8, you can also use [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), which is similar to a bitmap brush, but you can use primitives, too.</span></span>

<span data-ttu-id="d7289-113">Tutti i pennelli ereditano da [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) e condividono un set di funzionalità comuni (impostazione e recupero dell'opacità e trasformazione dei pennelli); vengono creati da [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) e sono risorse dipendenti dal dispositivo: l'applicazione deve creare pennelli dopo avere inizializzato la destinazione di rendering con cui verranno usati i pennelli e ricreare i pennelli ogni volta che la destinazione di rendering deve essere ricreata.</span><span class="sxs-lookup"><span data-stu-id="d7289-113">All brushes inherit from [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) and share a set of common features (setting and getting opacity, and transforming brushes); they are created by [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) and are device-dependent resources: your application should create brushes after it initializes the render target with which the brushes will be used, and recreate the brushes whenever the render target needs recreated.</span></span> <span data-ttu-id="d7289-114">Per ulteriori informazioni sulle risorse, vedere [Cenni preliminari sulle risorse](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="d7289-114">(For more information about resources, see [Resources Overview](resources-and-resource-domains.md).)</span></span>

<span data-ttu-id="d7289-115">Nella figura seguente vengono illustrati esempi di ognuno dei diversi tipi di pennelli.</span><span class="sxs-lookup"><span data-stu-id="d7289-115">The following illustration shows examples of each of the different brush types.</span></span>

![illustrazione degli effetti visivi da pennelli a tinta unita, pennelli sfumati lineari, pennelli sfumatura radiali e pennelli bitmap](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a><span data-ttu-id="d7289-117">Nozioni di base sui colori</span><span class="sxs-lookup"><span data-stu-id="d7289-117">Color basics</span></span>

<span data-ttu-id="d7289-118">Prima di disegnare con un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) o un pennello sfumato, è necessario scegliere i colori.</span><span class="sxs-lookup"><span data-stu-id="d7289-118">Before you paint with an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or a gradient brush, you need to choose colors.</span></span> <span data-ttu-id="d7289-119">In Direct2D i colori sono rappresentati dalla struttura [**d2d1 \_ Color \_ F**](d2d1-color-f.md) (che è in realtà un nuovo nome per la struttura usata da Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span><span class="sxs-lookup"><span data-stu-id="d7289-119">In Direct2D, colors are represented by the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure (which is actually just a new name for the structure that is used by Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span></span>

<span data-ttu-id="d7289-120">Prima di Windows 8, [**d2d1 \_ Color \_ F**](d2d1-color-f.md) usa la codifica sRGB.</span><span class="sxs-lookup"><span data-stu-id="d7289-120">Prior to Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) uses sRGB encoding.</span></span> <span data-ttu-id="d7289-121">la codifica sRGB divide i colori in quattro componenti: rosso, verde, blu e alfa.</span><span class="sxs-lookup"><span data-stu-id="d7289-121">sRGB encoding divides colors into four components: red, green, blue, and alpha.</span></span> <span data-ttu-id="d7289-122">Ogni componente è rappresentato da un valore a virgola mobile con un intervallo normale compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7289-122">Each component is represented by a floating point value with a normal range of 0.0 to 1.0.</span></span> <span data-ttu-id="d7289-123">Il valore 0,0 indica l'assenza completa del colore specifico, mentre il valore 1,0 indica che il colore è completamente presente.</span><span class="sxs-lookup"><span data-stu-id="d7289-123">A value of 0.0 indicates the complete absence of that color, while a value of 1.0 indicates that the color is fully present.</span></span> <span data-ttu-id="d7289-124">Per il componente alfa, 0,0 rappresenta un colore completamente trasparente e 1,0 rappresenta un colore completamente opaco.</span><span class="sxs-lookup"><span data-stu-id="d7289-124">For the alpha component, 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span>

<span data-ttu-id="d7289-125">A partire da Windows 8, [**d2d1 \_ Color \_ F**](d2d1-color-f.md) accetta anche la codifica di ScRGB.</span><span class="sxs-lookup"><span data-stu-id="d7289-125">Starting in Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) also accepts scRGB encoding.</span></span> <span data-ttu-id="d7289-126">scRGB è un superset di che consente valori di colore superiori a 1,0 e inferiori a 0,0.</span><span class="sxs-lookup"><span data-stu-id="d7289-126">scRGB is a superset of that allows color values above 1.0 and below 0.0.</span></span>

<span data-ttu-id="d7289-127">Per definire un colore, è possibile usare la struttura [**d2d1 \_ Color \_ F**](d2d1-color-f.md) e inizializzare i campi manualmente oppure è possibile usare la classe [**D2D1:: ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) per creare il colore.</span><span class="sxs-lookup"><span data-stu-id="d7289-127">To define a color, you can use the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure and initialize its fields yourself, or you can use the [**D2D1::ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to help you create the color.</span></span> <span data-ttu-id="d7289-128">La classe **ColorF** fornisce diversi costruttori per la definizione dei colori.</span><span class="sxs-lookup"><span data-stu-id="d7289-128">The **ColorF** class provides several constructors for defining colors.</span></span> <span data-ttu-id="d7289-129">Se il valore alfa non è specificato nei costruttori, il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7289-129">If the alpha value is not specified in the constructors, it defaults to 1.0.</span></span>

-   <span data-ttu-id="d7289-130">Usare il costruttore [**ColorF (enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) per specificare un colore predefinito e un valore di canale alfa.</span><span class="sxs-lookup"><span data-stu-id="d7289-130">Use the [**ColorF(Enum, FLOAT)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) constructor to specify a predefined color and an alpha channel value.</span></span> <span data-ttu-id="d7289-131">Un valore di canale alfa è compreso tra 0,0 e 1,0, dove 0,0 rappresenta un colore completamente trasparente e 1,0 rappresenta un colore completamente opaco.</span><span class="sxs-lookup"><span data-stu-id="d7289-131">An alpha channel value ranges from 0.0 to 1.0, where 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span> <span data-ttu-id="d7289-132">Nella figura seguente vengono illustrati diversi colori predefiniti e i rispettivi equivalenti esadecimali.</span><span class="sxs-lookup"><span data-stu-id="d7289-132">The following illustration shows several predefined colors and their hexadecimal equivalents.</span></span> <span data-ttu-id="d7289-133">Per un elenco completo dei colori predefiniti, vedere la sezione relativa alle costanti colore della classe [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="d7289-133">For a complete list of predefined colors, see the Color constants section of the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span>

    ![illustrazione dei colori predefiniti](images/brushes-ovw-colors.png)

    <span data-ttu-id="d7289-135">Nell'esempio seguente viene creato un colore predefinito che viene utilizzato per specificare il colore di un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="d7289-135">The following example creates a predefined color and uses it to specify the color of an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   <span data-ttu-id="d7289-136">Usare il costruttore [**ColorF (float, float, float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) per specificare un colore nella sequenza di rosso, verde, blu e alfa, dove ogni elemento ha un valore compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7289-136">Use the [**ColorF(FLOAT, FLOAT, FLOAT, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) constructor to specify a color in the sequence of a red, green, blue, and alpha, where each element has a value between 0.0 and 1.0.</span></span>

    <span data-ttu-id="d7289-137">Nell'esempio seguente vengono specificati i valori rosso, verde, blu e alfa per un colore.</span><span class="sxs-lookup"><span data-stu-id="d7289-137">The following example specifies the red, green, blue, and alpha values for a color.</span></span>

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   <span data-ttu-id="d7289-138">Usare il costruttore [**ColorF (UInt32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) per specificare il valore esadecimale di un colore e un valore alfa, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="d7289-138">Use the [**ColorF(UINT32, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) constructor to specify the hexadecimal value of a color and an alpha value, as shown in the following example.</span></span>
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a><span data-ttu-id="d7289-139">Modalità Alpha</span><span class="sxs-lookup"><span data-stu-id="d7289-139">Alpha modes</span></span>

<span data-ttu-id="d7289-140">Indipendentemente dalla modalità Alpha della destinazione di rendering con cui si usa un pennello, i [**valori \_ \_ F dei colori d2d1**](d2d1-color-f.md) vengono sempre interpretati come caratteri alfa dritti.</span><span class="sxs-lookup"><span data-stu-id="d7289-140">Regardless of the alpha mode of the render target with which you use a brush, [**D2D1\_COLOR\_F**](d2d1-color-f.md) values are always interpreted as straight alpha.</span></span>

## <a name="using-solid-color-brushes"></a><span data-ttu-id="d7289-141">Uso di pennelli a tinta unita</span><span class="sxs-lookup"><span data-stu-id="d7289-141">Using solid color brushes</span></span>

<span data-ttu-id="d7289-142">Per creare un pennello tinta unita, chiamare il metodo [**ID2D1RenderTarget:: CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) , che restituisce un valore HRESULT e un oggetto [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) .</span><span class="sxs-lookup"><span data-stu-id="d7289-142">To create a solid color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method, which returns an HRESULT and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) object.</span></span> <span data-ttu-id="d7289-143">La figura seguente mostra un quadrato tracciato con un pennello di colore nero e disegnato con un pennello tinta unita con il valore di colore 0x9ACD32.</span><span class="sxs-lookup"><span data-stu-id="d7289-143">The following illustration shows a square that is stroked with a black color brush and painted with a solid color brush that has the color value of 0x9ACD32.</span></span>

![illustrazione di un quadrato disegnato con un pennello tinta unita](images/brushes-ovw-solidcolor.png)

<span data-ttu-id="d7289-145">Il codice seguente illustra come creare e usare un pennello di colore nero e un pennello con un valore di colore 0x9ACD32 per riempire e creare il quadrato.</span><span class="sxs-lookup"><span data-stu-id="d7289-145">The following code shows how to create and use a black color brush and a brush with a color value of 0x9ACD32 to fill and draw this square.</span></span>


```C++
    ID2D1SolidColorBrush *m_pBlackBrush;
    ID2D1SolidColorBrush *m_pYellowGreenBrush;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}
```




```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
```



<span data-ttu-id="d7289-146">A differenza di altri pennelli, la creazione di un [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) è un'operazione relativamente economica.</span><span class="sxs-lookup"><span data-stu-id="d7289-146">Unlike other brushes, creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is a relatively inexpensive operation.</span></span> <span data-ttu-id="d7289-147">È possibile creare oggetti **ID2D1SolidColorBrush** ogni volta che viene eseguito il rendering con un effetto minimo sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d7289-147">You may create **ID2D1SolidColorBrush** objects each time you render with little to no performance impact.</span></span> <span data-ttu-id="d7289-148">Questo approccio non è consigliato per i pennelli sfumatura o bitmap.</span><span class="sxs-lookup"><span data-stu-id="d7289-148">This approach is not recommended for gradient or bitmap brushes.</span></span>

## <a name="using-linear-gradient-brushes"></a><span data-ttu-id="d7289-149">Uso di pennelli sfumati lineari</span><span class="sxs-lookup"><span data-stu-id="d7289-149">Using linear gradient brushes</span></span>

<span data-ttu-id="d7289-150">Un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) disegna un'area con una sfumatura lineare definita lungo una riga, l'asse delle sfumature.</span><span class="sxs-lookup"><span data-stu-id="d7289-150">An [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) paints an area with a linear gradient defined along a line, the gradient axis.</span></span> <span data-ttu-id="d7289-151">È possibile specificare i colori della sfumatura e la relativa posizione lungo l'asse delle sfumature usando gli oggetti [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) .</span><span class="sxs-lookup"><span data-stu-id="d7289-151">You specify the gradient's colors and their location along the gradient axis using [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) objects.</span></span> <span data-ttu-id="d7289-152">È anche possibile modificare l'asse delle sfumature, che consente di creare sfumature orizzontali e verticali e invertire la direzione della sfumatura.</span><span class="sxs-lookup"><span data-stu-id="d7289-152">You may also modify the gradient axis, which enables you to create horizontal and vertical gradient and to reverse the gradient direction.</span></span> <span data-ttu-id="d7289-153">Per creare un pennello sfumato lineare, chiamare il metodo [**ID2D1RenderTarget:: CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) .</span><span class="sxs-lookup"><span data-stu-id="d7289-153">To create a linear gradient brush, call the [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method.</span></span>

<span data-ttu-id="d7289-154">Nella figura seguente viene illustrato un quadrato disegnato con un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) con due colori predefiniti, "Yellow" e "ForestGreen".</span><span class="sxs-lookup"><span data-stu-id="d7289-154">The following illustration shows a square that is painted with an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that has two predefined colors, "Yellow" and "ForestGreen".</span></span>

![illustrazione di un quadrato disegnato con un pennello sfumato lineare di colore giallo e verde della foresta](images/brushes-ovw-lineargradient.png)

<span data-ttu-id="d7289-156">Per creare la sfumatura mostrata nell'illustrazione precedente, completare i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7289-156">To create the gradient shown in the preceding illustration, complete these steps:</span></span>

1.  <span data-ttu-id="d7289-157">Dichiarare due oggetti di [**\_ \_ interruzione sfumatura d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="d7289-157">Declare two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="d7289-158">Ogni cursore sfumatura specifica un colore e una posizione.</span><span class="sxs-lookup"><span data-stu-id="d7289-158">Each gradient stop specifies a color and a position.</span></span> <span data-ttu-id="d7289-159">La posizione 0,0 indica l'inizio della sfumatura, mentre la posizione 1,0 indica la fine della sfumatura.</span><span class="sxs-lookup"><span data-stu-id="d7289-159">A position of 0.0 indicates the beginning of the gradient, while a position of 1.0 indicates the end of the gradient.</span></span>

    <span data-ttu-id="d7289-160">Il codice seguente crea una matrice di due oggetti di [**\_ \_ interruzione sfumatura d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .</span><span class="sxs-lookup"><span data-stu-id="d7289-160">The following code creates an array of two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="d7289-161">Il primo arresto specifica il colore "Yellow" nella posizione 0, mentre il secondo stop specifica il colore "ForestGreen" nella posizione 1.</span><span class="sxs-lookup"><span data-stu-id="d7289-161">The first stop specifies the color "Yellow" at a position 0, and the second stop specifies the color "ForestGreen" at position 1.</span></span>

```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
```

    

2.  <span data-ttu-id="d7289-162">Creare un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span><span class="sxs-lookup"><span data-stu-id="d7289-162">Create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span> <span data-ttu-id="d7289-163">Nell'esempio seguente viene chiamato [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), passando la matrice di oggetti di [**\_ \_ interruzione della sfumatura d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) , il numero di cursori sfumatura (2), [**d2d1 \_ gamma \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) per l'interpolazione e il [**\_ \_ \_ morsetto della modalità Extend d2d1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) per la modalità di estensione.</span><span class="sxs-lookup"><span data-stu-id="d7289-163">The following example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), passing in the array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects, the number of gradient stops (2), [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) for interpolation, and [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) for the extend mode.</span></span>

```C++
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
```

    

3.  <span data-ttu-id="d7289-164">Creare il [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="d7289-164">Create the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="d7289-165">Nell'esempio successivo viene chiamato il metodo [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) e vengono passate le proprietà del pennello sfumatura lineare che contengono il punto iniziale in (0,0) e il punto finale in (150, 150) e i cursori sfumatura creati nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="d7289-165">The next example calls the [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method and passes it the linear gradient brush properties that contain the start point at (0, 0) and the end point at (150, 150), and the gradient stops created in the previous step.</span></span>
```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
```

    

4.  <span data-ttu-id="d7289-166">Usare [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="d7289-166">Use the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="d7289-167">Nell'esempio di codice successivo viene usato il pennello per eseguire la filleina di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="d7289-167">The next code example uses the brush to fille a rectangle.</span></span>
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a><span data-ttu-id="d7289-168">Altre informazioni sui cursori sfumatura</span><span class="sxs-lookup"><span data-stu-id="d7289-168">More about gradient stops</span></span>

<span data-ttu-id="d7289-169">Il [**\_ cursore sfumatura \_ d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) è il blocco predefinito di base di un pennello sfumatura.</span><span class="sxs-lookup"><span data-stu-id="d7289-169">The [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) is the basic building block of a gradient brush.</span></span> <span data-ttu-id="d7289-170">Un cursore sfumatura specifica il colore e la posizione lungo l'asse delle sfumature.</span><span class="sxs-lookup"><span data-stu-id="d7289-170">A gradient stop specifies the color and the position along the gradient axis.</span></span> <span data-ttu-id="d7289-171">Il valore della posizione della sfumatura è compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7289-171">The value of the gradient position ranges between 0.0 and 1.0.</span></span> <span data-ttu-id="d7289-172">Più è vicino a 0,0, più il colore è vicino all'inizio della sfumatura. più è vicino a 1,0, più il colore è vicino alla fine della sfumatura.</span><span class="sxs-lookup"><span data-stu-id="d7289-172">The closer it is to 0.0, the closer the color is to the start of the gradient; the closer it is to 1.0, the closer the color is to the end of the gradient.</span></span>

<span data-ttu-id="d7289-173">Nell'illustrazione seguente vengono evidenziati i cursori sfumatura.</span><span class="sxs-lookup"><span data-stu-id="d7289-173">The following illustration highlights the gradient stops.</span></span> <span data-ttu-id="d7289-174">Il cerchio contrassegna la posizione dei cursori sfumatura e una linea tratteggiata mostra l'asse delle sfumature.</span><span class="sxs-lookup"><span data-stu-id="d7289-174">The circle marks the position of gradient stops and a dashed line shows the gradient axis.</span></span>

![illustrazione di un pennello sfumato lineare con quattro interruzioni lungo l'asse](images/4stoplineargradient.png)

<span data-ttu-id="d7289-176">Il primo cursore sfumatura specifica il colore giallo alla posizione 0,0.</span><span class="sxs-lookup"><span data-stu-id="d7289-176">The first gradient stop specifies the color yellow at a position of 0.0.</span></span> <span data-ttu-id="d7289-177">Il secondo cursore sfumatura specifica il colore rosso in corrispondenza della posizione 0,25.</span><span class="sxs-lookup"><span data-stu-id="d7289-177">The second gradient stop specifies red color at a position of 0.25.</span></span> <span data-ttu-id="d7289-178">Da sinistra a destra lungo l'asse delle sfumature, i colori tra queste due interruzioni cambiano gradualmente da giallo a rosso.</span><span class="sxs-lookup"><span data-stu-id="d7289-178">From left to right along the gradient axis, the colors between these two stops gradually change from yellow to red.</span></span> <span data-ttu-id="d7289-179">Il terzo cursore sfumatura specifica il colore blu nella posizione 0,75.</span><span class="sxs-lookup"><span data-stu-id="d7289-179">The third gradient stop specifies blue color at a position of 0.75.</span></span> <span data-ttu-id="d7289-180">I colori tra il secondo e il terzo interruzioni della sfumatura cambiano gradualmente da rosso a blu.</span><span class="sxs-lookup"><span data-stu-id="d7289-180">The colors between the second and third gradient stops gradually change from red to blue.</span></span> <span data-ttu-id="d7289-181">Il quarto cursore sfumatura specifica verde limone alla posizione 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7289-181">The fourth gradient stop specifies lime green at a position of 1.0.</span></span> <span data-ttu-id="d7289-182">I colori tra il terzo e il quarto cursore sfumatura cambiano gradualmente da blu a verde limone.</span><span class="sxs-lookup"><span data-stu-id="d7289-182">The colors between the third and fourth gradient stops gradually change from blue to lime green.</span></span>

## <a name="the-gradient-axis"></a><span data-ttu-id="d7289-183">Asse delle sfumature</span><span class="sxs-lookup"><span data-stu-id="d7289-183">The gradient axis</span></span>

<span data-ttu-id="d7289-184">Come indicato in precedenza, i cursori sfumatura di un pennello sfumato lineare sono posizionati lungo una riga, l'asse delle sfumature.</span><span class="sxs-lookup"><span data-stu-id="d7289-184">As mentioned previously, gradient stops of a linear gradient brush are positioned along a line, the gradient axis.</span></span> <span data-ttu-id="d7289-185">È possibile specificare l'orientamento e la dimensione della linea usando i campi **StartPoint** ed **endpoint** della struttura [**delle \_ \_ proprietà del \_ pennello \_ sfumatura lineare d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) quando si crea un pennello sfumatura lineare.</span><span class="sxs-lookup"><span data-stu-id="d7289-185">You can specify the orientation and size of the line using the **startPoint** and **endPoint** fields of the [**D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) structure when you create a linear gradient brush.</span></span> <span data-ttu-id="d7289-186">Dopo aver creato un pennello, è possibile modificare l'asse delle sfumature chiamando i metodi [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) e [**seendpoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) del pennello.</span><span class="sxs-lookup"><span data-stu-id="d7289-186">After you've created a brush, you can adjust the gradient axis by calling the brush's [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) and [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) methods.</span></span> <span data-ttu-id="d7289-187">Modificando il punto iniziale e il punto finale del pennello, è possibile creare sfumature orizzontali e verticali, invertire la direzione della sfumatura e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="d7289-187">By manipulating the brush's start point and end point, you can create horizontal and vertical gradients, reverse the gradient direction, and more.</span></span>

<span data-ttu-id="d7289-188">Nella figura seguente, ad esempio, il punto iniziale è impostato su (0,0) e il punto finale a (150, 50); viene creata una sfumatura diagonale che inizia dall'angolo superiore sinistro e si estende all'angolo inferiore destro dell'area da disegnare.</span><span class="sxs-lookup"><span data-stu-id="d7289-188">For example, in the following illustration, the start point is set to (0,0) and the end point to (150, 50); this creates a diagonal gradient that starts at the upper-left corner and extends to the lower-right corner of the area being painted.</span></span> <span data-ttu-id="d7289-189">Quando si imposta il punto iniziale su (0, 25) e il punto finale su (150, 25), viene creata una sfumatura orizzontale.</span><span class="sxs-lookup"><span data-stu-id="d7289-189">When you set the start point to (0, 25) and the end point to (150, 25), a horizontal gradient is created.</span></span> <span data-ttu-id="d7289-190">Analogamente, impostando il punto iniziale su (75, 0) e il punto finale su (75, 50) viene creata una sfumatura verticale.</span><span class="sxs-lookup"><span data-stu-id="d7289-190">Similarly, setting the start point to (75, 0) and the end point to (75, 50) creates a vertical gradient.</span></span> <span data-ttu-id="d7289-191">Impostando il punto iniziale su (0, 50) e il punto finale su (150, 0) viene creata una sfumatura diagonale che inizia dall'angolo inferiore sinistro e si estende all'angolo superiore destro dell'area da disegnare.</span><span class="sxs-lookup"><span data-stu-id="d7289-191">Setting the start point to (0, 50) and the end point to (150, 0) creates a diagonal gradient that starts at the lower-left corner and extends to the upper-right corner of the area being painted.</span></span>

![illustrazione di quattro diversi assi sfumatura sullo stesso rettangolo](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a><span data-ttu-id="d7289-193">Uso di pennelli con sfumatura radiale</span><span class="sxs-lookup"><span data-stu-id="d7289-193">Using radial gradient brushes</span></span>

<span data-ttu-id="d7289-194">A differenza di un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), che combina due o più colori lungo un asse di sfumatura, un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) disegna un'area con una sfumatura radiale che combina due o più colori in un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="d7289-194">Unlike an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), which blends two or more colors along a gradient axis, an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) paints an area with a radial gradient that blends two or more colors across an ellipse.</span></span> <span data-ttu-id="d7289-195">Mentre un **ID2D1LinearGradientBrush** definisce l'asse delle sfumature con un punto iniziale e un punto finale, un **ID2D1RadialGradientBrush** definisce l'ellisse sfumatura specificando un raggio centrale, orizzontale e verticale e un offset di origine sfumatura.</span><span class="sxs-lookup"><span data-stu-id="d7289-195">While a **ID2D1LinearGradientBrush** defines its gradient axis with a start point and an end point, a **ID2D1RadialGradientBrush** defines its gradient ellipse by specifying a center, horizontal and vertical radii, and a gradient origin offset.</span></span>

<span data-ttu-id="d7289-196">Analogamente a [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) usa un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) per specificare i colori e le posizioni nella sfumatura.</span><span class="sxs-lookup"><span data-stu-id="d7289-196">Like an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) uses an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to specify the colors and positions in the gradient.</span></span>

<span data-ttu-id="d7289-197">Nella figura seguente viene illustrato un cerchio disegnato con un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="d7289-197">The following illustration shows a circle painted with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span> <span data-ttu-id="d7289-198">Il cerchio presenta due cursori sfumatura: il primo specifica un colore predefinito "Yellow" nella posizione 0,0 e il secondo specifica un colore predefinito "ForestGreen" nella posizione 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7289-198">The circle has two gradient stops: the first specifies a predefined color "Yellow" at a position of 0.0, and the second specifies a predefined color "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="d7289-199">La sfumatura ha un centro di (75, 75), un offset di origine sfumatura pari a (0,0) e un raggio x e y di 75.</span><span class="sxs-lookup"><span data-stu-id="d7289-199">The gradient has a center of (75, 75), a gradient origin offset of (0, 0), and an x- and y-radius of 75.</span></span>

![illustrazione di un cerchio disegnato con un pennello a sfumatura radiale](images/brushes-ovw-radials.png)

<span data-ttu-id="d7289-201">Negli esempi di codice seguenti viene illustrato come disegnare questo cerchio con un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) con due interruzioni di colore: "Yellow" nella posizione 0,0 e "ForestGreen" nella posizione 1,0.</span><span class="sxs-lookup"><span data-stu-id="d7289-201">The following code examples shows how to paint this circle with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that has two color stops: "Yellow" at a position of 0.0, and "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="d7289-202">Analogamente alla creazione di un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), l'esempio chiama [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) per creare un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) da una matrice di cursori sfumatura.</span><span class="sxs-lookup"><span data-stu-id="d7289-202">Similar to creating an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), the example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from an array of gradient stops.</span></span>


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



<span data-ttu-id="d7289-203">Per creare un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), usare il metodo [**ID2D1RenderTarget:: CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) .</span><span class="sxs-lookup"><span data-stu-id="d7289-203">To create an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), use the [**ID2D1RenderTarget::CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) method.</span></span> <span data-ttu-id="d7289-204">**CreateRadialGradientBrush** accetta tre parametri.</span><span class="sxs-lookup"><span data-stu-id="d7289-204">The **CreateRadialGradientBrush** takes three parameters.</span></span> <span data-ttu-id="d7289-205">Il primo parametro, una [**\_ proprietà del \_ \_ pennello \_ sfumatura radiale d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) , specifica il centro, l'offset di origine sfumatura e i raggi orizzontali e verticali della sfumatura.</span><span class="sxs-lookup"><span data-stu-id="d7289-205">The first parameter, a [**D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) specifies the center, gradient origin offset, and the horizontal and vertical radii of the gradient.</span></span> <span data-ttu-id="d7289-206">Il secondo parametro è un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) che descrive i colori e le rispettive posizioni nella sfumatura e il terzo parametro è l'indirizzo del puntatore che riceve il nuovo riferimento **ID2D1RadialGradientBrush** .</span><span class="sxs-lookup"><span data-stu-id="d7289-206">The second parameter is an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) that describes the colors and their positions in the gradient, and the third parameter is the address of the pointer that receive the new **ID2D1RadialGradientBrush** reference.</span></span> <span data-ttu-id="d7289-207">Alcuni overload accettano un parametro aggiuntivo, una struttura di [**\_ \_ proprietà del pennello d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) che specifica un valore di opacità e una trasformazione da applicare al nuovo pennello.</span><span class="sxs-lookup"><span data-stu-id="d7289-207">Some overloads take an additional parameter, a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) structure that specifies an opacity value and a transform to apply to the new brush.</span></span>

<span data-ttu-id="d7289-208">Nell'esempio seguente viene chiamato [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), passando la matrice di cursori sfumatura e le proprietà del pennello sfumatura radiale con il valore *Center* impostato su (75, 75), *gradientOriginOffset* impostato su (0, 0) e *radiusX* e *RadiusY* entrambi impostati su 75.</span><span class="sxs-lookup"><span data-stu-id="d7289-208">The next example calls [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), passing in the array of gradient stops, and the radial gradient brush properties that have the *center* value set to (75, 75), the *gradientOriginOffset* set to (0, 0), and *radiusX* and *radiusY* both set to 75.</span></span>


```C++
// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &m_pRadialGradientBrush
        );
}
```



<span data-ttu-id="d7289-209">Nell'esempio finale viene usato il pennello per riempire un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="d7289-209">The final example uses the brush to fill an ellipse.</span></span>


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a><span data-ttu-id="d7289-210">Configurazione di una sfumatura radiale</span><span class="sxs-lookup"><span data-stu-id="d7289-210">Configuring a radial gradient</span></span>

<span data-ttu-id="d7289-211">Valori diversi per *Center*, *gradientOriginOffset*, *RadiusX* e/o *RadiusY* producono gradienti diversi.</span><span class="sxs-lookup"><span data-stu-id="d7289-211">Different values for *center*, *gradientOriginOffset*, *radiusX* and/or *radiusY* produce different gradients.</span></span> <span data-ttu-id="d7289-212">Nella figura seguente sono illustrate diverse sfumature radiali con offset di origine sfumatura diversi, creando l'aspetto della luce che illumina i cerchi da angoli diversi.</span><span class="sxs-lookup"><span data-stu-id="d7289-212">The following illustration shows several radial gradients that have different gradient origin offsets, creating the appearance of the light illuminating the circles from different angles.</span></span>

![illustrazione dello stesso cerchio disegnato con pennelli con sfumature radiali con offset di origine diversi](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a><span data-ttu-id="d7289-214">Uso di pennelli bitmap</span><span class="sxs-lookup"><span data-stu-id="d7289-214">Using bitmap brushes</span></span>

<span data-ttu-id="d7289-215">Un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) disegna un'area con una bitmap (rappresentata da un oggetto [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) ).</span><span class="sxs-lookup"><span data-stu-id="d7289-215">An [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) paints an area with a bitmap (represented by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object).</span></span>

<span data-ttu-id="d7289-216">Nella figura seguente viene illustrato un quadrato disegnato con una bitmap di un impianto.</span><span class="sxs-lookup"><span data-stu-id="d7289-216">The following illustration shows a square painted with a bitmap of a plant.</span></span>

![illustrazione di un quadrato disegnato con una bitmap Plant](images/brushes-ovw-bitmap.png)

<span data-ttu-id="d7289-218">Negli esempi seguenti viene illustrato come disegnare questo quadrato con un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="d7289-218">The examples that follow shows how to paint this square with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>

<span data-ttu-id="d7289-219">Nel primo esempio viene inizializzato un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) per l'utilizzo con il pennello.</span><span class="sxs-lookup"><span data-stu-id="d7289-219">The first example initializes an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) for use with the brush.</span></span> <span data-ttu-id="d7289-220">**ID2D1Bitmap** viene fornito da un metodo helper, LoadResourceBitmap, definito altrove nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="d7289-220">The **ID2D1Bitmap** is provided by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
}
```



<span data-ttu-id="d7289-221">Per creare il pennello bitmap, chiamare il metodo [**ID2D1RenderTarget:: CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) e specificare [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) con cui disegnare.</span><span class="sxs-lookup"><span data-stu-id="d7289-221">To create the bitmap brush, call the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with which to paint.</span></span> <span data-ttu-id="d7289-222">Il metodo restituisce un valore **HRESULT** e un oggetto [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) .</span><span class="sxs-lookup"><span data-stu-id="d7289-222">The method returns an **HRESULT** and an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) object.</span></span> <span data-ttu-id="d7289-223">Alcuni overload di **CreateBitmapBrush** consentono di specificare opzioni aggiuntive accettando una proprietà del [**\_ pennello d2d1 \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) e una struttura delle [**\_ \_ \_ proprietà del pennello bitmap d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) .</span><span class="sxs-lookup"><span data-stu-id="d7289-223">Some **CreateBitmapBrush** overloads enable you to specify additional options by accepting a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) and a [**D2D1\_BITMAP\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) structure.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



<span data-ttu-id="d7289-224">Nell'esempio seguente viene usato il pennello per riempire un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="d7289-224">The next example uses the brush to fill a rectangle.</span></span>


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a><span data-ttu-id="d7289-225">Configurazione delle modalità di estensione</span><span class="sxs-lookup"><span data-stu-id="d7289-225">Configuring extend modes</span></span>

<span data-ttu-id="d7289-226">In alcuni casi, la sfumatura di un pennello sfumatura o della bitmap per un pennello bitmap non riempie completamente l'area disegnata.</span><span class="sxs-lookup"><span data-stu-id="d7289-226">Sometimes, the gradient of a gradient brush or the bitmap for a bitmap brush doesn't completely fill the area being painted.</span></span>

-   <span data-ttu-id="d7289-227">Quando si verifica questa situazione per un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D usa le impostazioni della modalità di estensione orizzontale ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) e verticale ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) del pennello per determinare come riempire l'area rimanente.</span><span class="sxs-lookup"><span data-stu-id="d7289-227">When this happens for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D uses the brush's horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) and vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) extend mode settings to determine how to fill the remaining area.</span></span>

-   <span data-ttu-id="d7289-228">Quando si verifica questa situazione per un pennello sfumatura, Direct2D determina come riempire l'area rimanente usando il valore del parametro della [**\_ \_ modalità di estensione d2d1**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) specificato quando è stato chiamato il [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) per creare il [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)del pennello sfumatura.</span><span class="sxs-lookup"><span data-stu-id="d7289-228">When this happens for a gradient brush, Direct2D determines how to fill the remaining area by using the value of the [**D2D1\_EXTEND\_MODE**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) parameter that you specified when you called the [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create the gradient brush's [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>

<span data-ttu-id="d7289-229">Nella figura seguente sono illustrati i risultati di ogni possibile combinazione di modalità di estensione per un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**d2d1 \_ extend \_ mode \_ Clamp**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (clamp), **d2d1 \_ extend \_ mode \_ Wrap** (wrap) e **d2d1 \_ extend \_ mirror** (mirror).</span><span class="sxs-lookup"><span data-stu-id="d7289-229">The following illustration shows the results from every possible combination of the extend modes for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (CLAMP), **D2D1\_EXTEND\_MODE\_WRAP** (WRAP), and **D2D1\_EXTEND\_MIRROR** (MIRROR).</span></span>

![illustrazione di un'immagine originale e delle immagini risultanti da varie modalità di estensione](images/bitmapwrap-clamp-mirror.png)

<span data-ttu-id="d7289-231">Nell'esempio seguente viene illustrato come impostare le modalità di estensione x e y del pennello bitmap su [**d2d1 \_ extend \_ mirror**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span><span class="sxs-lookup"><span data-stu-id="d7289-231">The following example shows how to set the bitmap brush's x- and y-extend modes to [**D2D1\_EXTEND\_MIRROR**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span> <span data-ttu-id="d7289-232">Disegna quindi il rettangolo con [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span><span class="sxs-lookup"><span data-stu-id="d7289-232">It then paints the rectangle with the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



<span data-ttu-id="d7289-233">Produce l'output come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="d7289-233">It produces output as shown in the following illustration.</span></span>

![illustrazione di un'immagine originale e dell'immagine risultante dopo il mirroring della direzione x e della direzione y](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a><span data-ttu-id="d7289-235">Trasformazione di pennelli</span><span class="sxs-lookup"><span data-stu-id="d7289-235">Transforming brushes</span></span>

<span data-ttu-id="d7289-236">Quando si disegna con un pennello, dipinge nello spazio delle coordinate della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="d7289-236">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="d7289-237">I pennelli non si posizionano automaticamente per allinearsi all'oggetto da disegnare; per impostazione predefinita, iniziano a disegnare nell'origine (0,0) della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="d7289-237">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="d7289-238">È possibile "spostare" la sfumatura definita da un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) in un'area di destinazione impostando il punto iniziale e il punto finale.</span><span class="sxs-lookup"><span data-stu-id="d7289-238">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="d7289-239">Analogamente, è possibile spostare la sfumatura definita da un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) cambiando il relativo centro e i raggi.</span><span class="sxs-lookup"><span data-stu-id="d7289-239">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="d7289-240">Per allineare il contenuto di un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) all'area da disegnare, è possibile usare il metodo [**setransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) per convertire la bitmap nella posizione desiderata.</span><span class="sxs-lookup"><span data-stu-id="d7289-240">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="d7289-241">Questa trasformazione influisca solo sul pennello. non influisce sugli altri contenuti creati dalla destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="d7289-241">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="d7289-242">Nelle illustrazioni seguenti viene illustrato l'effetto dell'utilizzo di un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) per riempire un rettangolo situato in (100, 100).</span><span class="sxs-lookup"><span data-stu-id="d7289-242">The following illustrations shows the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="d7289-243">L'illustrazione nell'illustrazione a sinistra mostra il risultato del riempimento del rettangolo senza trasformare il pennello: la bitmap viene disegnata in corrispondenza dell'origine della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="d7289-243">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="d7289-244">Di conseguenza, nel rettangolo viene visualizzata solo una parte della bitmap.</span><span class="sxs-lookup"><span data-stu-id="d7289-244">As a result, only a portion of the bitmap appears in the rectangle.</span></span> <span data-ttu-id="d7289-245">L'illustrazione a destra mostra il risultato della trasformazione del **ID2D1BitmapBrush** in modo che il relativo contenuto venga spostato 50 pixel a destra e 50 pixel in basso.</span><span class="sxs-lookup"><span data-stu-id="d7289-245">The illustration on the right shows the result of transforming the **ID2D1BitmapBrush** so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="d7289-246">La bitmap riempie ora il rettangolo.</span><span class="sxs-lookup"><span data-stu-id="d7289-246">The bitmap now fills the rectangle.</span></span>

![illustrazione di un quadrato disegnato con un pennello bitmap senza trasformazione del pennello e trasformazione del pennello](images/brushes-ovw-transform.png)

<span data-ttu-id="d7289-248">Il codice seguente illustra come eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="d7289-248">The following code shows how to accomplish this.</span></span> <span data-ttu-id="d7289-249">Per prima cosa applicare una traduzione al [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), spostandolo il pennello 50 pixel lungo l'asse x e 50 pixel lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="d7289-249">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="d7289-250">Usare quindi **ID2D1BitmapBrush** per riempire il rettangolo con angolo superiore sinistro in (100, 100) e l'angolo inferiore destro in (200, 200).</span><span class="sxs-lookup"><span data-stu-id="d7289-250">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


```cpp
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
   
}

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}

D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);

// Demonstrate the effect of transforming a bitmap brush.
m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

// To see the content of the rcTransformedBrushRect, comment
// out this statement.
m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

m_pRenderTarget->DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```

## <a name="related-topics"></a><span data-ttu-id="d7289-251">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7289-251">Related topics</span></span>

* [<span data-ttu-id="d7289-252">Riferimento Direct2D</span><span class="sxs-lookup"><span data-stu-id="d7289-252">Direct2D reference</span></span>](reference.md)
* [<span data-ttu-id="d7289-253">Come creare un pennello tinta unita</span><span class="sxs-lookup"><span data-stu-id="d7289-253">How to create a solid color brush</span></span>](how-to-create-a-solid-color-brush.md)
* [<span data-ttu-id="d7289-254">Come creare un pennello sfumato lineare</span><span class="sxs-lookup"><span data-stu-id="d7289-254">How to create a linear gradient brush</span></span>](how-to-create-a-linear-gradient-brush.md)
* [<span data-ttu-id="d7289-255">Come creare un pennello sfumatura radiale</span><span class="sxs-lookup"><span data-stu-id="d7289-255">How to create a radial gradient brush</span></span>](how-to-create-a-radial-gradient-brush.md)
* [<span data-ttu-id="d7289-256">Come creare un pennello bitmap</span><span class="sxs-lookup"><span data-stu-id="d7289-256">How to create a bitmap brush</span></span>](how-to-create-a-bitmap-brush.md)
