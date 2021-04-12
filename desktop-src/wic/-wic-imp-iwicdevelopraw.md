---
description: Implementazione di IWICDevelopRaw
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Implementazione di IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 683dc2baf0496694943b7640d3f3ed521dc477a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234075"
---
# <a name="implementing-iwicdevelopraw"></a><span data-ttu-id="18e02-103">Implementazione di IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="18e02-103">Implementing IWICDevelopRaw</span></span>

## <a name="iwicdevelopraw"></a><span data-ttu-id="18e02-104">IWICDevelopRaw</span><span class="sxs-lookup"><span data-stu-id="18e02-104">IWICDevelopRaw</span></span>

<span data-ttu-id="18e02-105">L'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) espone opzioni di elaborazione specifiche per l'elaborazione di immagini non elaborate.</span><span class="sxs-lookup"><span data-stu-id="18e02-105">The [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface exposes processing options specific to raw image processing.</span></span> <span data-ttu-id="18e02-106">Tutti i codec RAW devono supportare l'interfaccia **IWICDevelopRaw** .</span><span class="sxs-lookup"><span data-stu-id="18e02-106">All raw codecs must support the **IWICDevelopRaw** interface.</span></span> <span data-ttu-id="18e02-107">Alcuni codec non elaborati potrebbero non essere in grado di supportare tutte le impostazioni esposte da questa interfaccia, ma è necessario supportare tutte le impostazioni che il codec è in grado di eseguire.</span><span class="sxs-lookup"><span data-stu-id="18e02-107">Some raw codecs may not be able to support every setting exposed by this interface, but you should support all the settings that your codec is capable of performing.</span></span> <span data-ttu-id="18e02-108">Come minimo, ogni codec RAW deve implementare i metodi [**serotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) e [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) .</span><span class="sxs-lookup"><span data-stu-id="18e02-108">At minimum, every raw codec must implement the [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) methods.</span></span>

<span data-ttu-id="18e02-109">Inoltre, alcuni metodi e interfacce facoltativi per altri codec sono fortemente consigliati per i codec non elaborati.</span><span class="sxs-lookup"><span data-stu-id="18e02-109">Additionally, some methods and interfaces that are optional for other codecs are strongly recommended for raw codecs.</span></span> <span data-ttu-id="18e02-110">Sono inclusi i metodi [**getpreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) e [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) sulla classe decodificatore a livello di contenitore e l'interfaccia [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) nella classe Decode a livello di frame.</span><span class="sxs-lookup"><span data-stu-id="18e02-110">These include the [**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) and [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) methods on the container-level decoder class, and the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface on the frame-level decode class.</span></span>

<span data-ttu-id="18e02-111">Le impostazioni impostate usando i metodi [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) devono essere rese persistenti dal codec in modo coerente con il modo in cui gli altri metadati sono persistenti, ma è consigliabile non sovrascrivere mai le impostazioni originali "come shot".</span><span class="sxs-lookup"><span data-stu-id="18e02-111">Settings set by using the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) methods should be persisted by the codec in a way that’s consistent with the way other metadata is persisted, but you should never overwrite the original "As Shot" settings.</span></span> <span data-ttu-id="18e02-112">Salvando in modo permanente i metadati e implementando [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) e [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), è possibile abilitare le applicazioni di elaborazione non elaborate per recuperare e applicare le impostazioni di elaborazione tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="18e02-112">By persisting the metadata and implementing [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) and [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), you enable raw processing applications to retrieve and apply processing settings across sessions.</span></span>

<span data-ttu-id="18e02-113">Uno degli scopi principali dell'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) è consentire agli sviluppatori di applicazioni di creare un'interfaccia utente per la regolazione di parametri non elaborati che funzioneranno il più possibile in modo coerente tra diversi codec.</span><span class="sxs-lookup"><span data-stu-id="18e02-113">A main purpose of the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface is to enable application developers to build a user interface for adjusting raw parameters that will work as consistently as possible across different codecs.</span></span> <span data-ttu-id="18e02-114">Si supponga che un utente finale modifichi i parametri usando un controllo dispositivo di scorrimento, con i valori minimo e massimo di cui è stato eseguito il mapping agli intervalli minimo e massimo per il parametro.</span><span class="sxs-lookup"><span data-stu-id="18e02-114">Assume that an end user will adjust the parameters by using a slider control, with its minimum and maximum values mapped to the minimum and maximum ranges for the parameter.</span></span> <span data-ttu-id="18e02-115">Per supportare questa operazione, è necessario eseguire ogni sforzo per considerare tutti gli intervalli di parametri come lineari.</span><span class="sxs-lookup"><span data-stu-id="18e02-115">To support this, you should make every effort to treat all parameter ranges as linear.</span></span> <span data-ttu-id="18e02-116">Per assicurarsi che i controlli dispositivo di scorrimento non siano eccessivamente sensibili, è necessario supportare anche un intervallo più ampio possibile per ogni parametro, coprendo almeno il 50% dell'intervallo massimo possibile.</span><span class="sxs-lookup"><span data-stu-id="18e02-116">To ensure that the slider controls aren’t overly sensitive, you should also support as broad a range as possible for each parameter, covering at least 50 percent of the maximum possible range.</span></span> <span data-ttu-id="18e02-117">Ad esempio, se l'intervallo massimo possibile di contrasto è da grigio puro a puro nero e bianco, con il valore predefinito di cui viene eseguito il mapping a 0,0, l'intervallo minimo supportato da un codec è compreso tra almeno metà tra il valore predefinito e il grigio puro nell'estremità inferiore (-1,0), almeno a metà tra il valore predefinito e il nero puro e il bianco all'estremità superiore (+ 1,0)</span><span class="sxs-lookup"><span data-stu-id="18e02-117">For example, if the maximum possible range of contrast is from pure gray to pure black and white, with the default value being mapped to 0.0, the minimum range supported by a codec would be from at least halfway between the default value and pure gray on the low end (–1.0), to at least halfway between the default value and pure black and white on the high end (+1.0).</span></span>


```C++
interface IWICDevelopRaw : IWICBitmapFrameDecode
{
   HRESULT QueryRawCapabilitiesInfo ( WICRawCapabilitiesInfo *pInfo );
   HRESULT LoadParameterSet ( WICRawParameterSet ParameterSet );
   HRESULT GetCurrentParameterSet ( IPropertyBag2 **ppCurrentParameterSet );
   HRESULT SetExposureCompensation ( double ev );
   HRESULT GetExposureCompensation ( double *pEV );
   HRESULT SetWhitePointRGB ( UINT Red, UINT Green, UINT Blue );
   HRESULT GetWhitePointRGB ( UINT *pRed, UINT *pGreen, UINT *pBlue );
   HRESULT SetNamedWhitePoint ( WICNamedWhitePoint WhitePoint );
   HRESULT GetNamedWhitePoint ( WICNamedWhitePoint *pWhitePoint );
   HRESULT SetWhitePointKelvin ( UINT WhitePointKelvin );
   HRESULT GetWhitePointKelvin ( UINT *pWhitePointKelvin );
   HRESULT GetKelvinRangeInfo ( UINT *pMinKelvinTemp,
               UINT *pMaxKelvinTemp,
               UINT *pKelvinTempStepValue );
   HRESULT SetContrast ( double Contrast );
   HRESULT GetContrast ( double *pContrast );
   HRESULT SetGamma ( double Gamma );
   HRESULT GetGamma ( double *pGamma );
   HRESULT SetSharpness ( double Sharpness );
   HRESULT GetSharpness ( double *pSharpness );
   HRESULT SetSaturation ( double Saturation );
   HRESULT GetSaturation ( double *pSaturation );
   HRESULT SetTint ( double Tint );
   HRESULT GetTint ( double *pTint );
   HRESULT SetNoiseReduction ( double NoiseReduction );
   HRESULT GetNoiseReduction ( double *pNoiseReduction );
   HRESULT SetDestinationColorContext (const IWICColorContext *pColorContext );
   HRESULT SetToneCurve ( UINT cbToneCurveSize,
               const WICRawToneCurve *pToneCurve );
   HRESULT GetToneCurve ( UINT cbToneCurveBufferSize,
               WICRawToneCurve *pToneCurve,
               UINT *pcbActualToneCurveBufferSize );
   HRESULT SetRotation ( double Rotation );
   HRESULT GetRotation ( double *pRotation );
   HRESULT SetRenderMode ( WICRawRenderMode RenderMode );
   HRESULT GetRenderMode ( WICRawRenderMode *pRenderMode ); 
   HRESULT SetNotificationCallback ( IWICDevelopRawNotificationCallback 
               *pCallback );
}
```



-   [<span data-ttu-id="18e02-118">QueryRawCapabilitiesInfo</span><span class="sxs-lookup"><span data-stu-id="18e02-118">QueryRawCapabilitiesInfo</span></span>](#queryrawcapabilitiesinfo)
-   [<span data-ttu-id="18e02-119">LoadParameterSet</span><span class="sxs-lookup"><span data-stu-id="18e02-119">LoadParameterSet</span></span>](#loadparameterset)
-   [<span data-ttu-id="18e02-120">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="18e02-120">GetCurrentParameterSet</span></span>](#getcurrentparameterset)
-   [<span data-ttu-id="18e02-121">Set/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="18e02-121">Set/GetExposureCompensation</span></span>](#setgetexposurecompensation)
-   [<span data-ttu-id="18e02-122">Set/GetCurrentParameterRGB, set/GetNamedWhitePoint, set/GetwhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="18e02-122">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [<span data-ttu-id="18e02-123">Set/getcontrast</span><span class="sxs-lookup"><span data-stu-id="18e02-123">Set/GetContrast</span></span>](#setgetcontrast)
-   [<span data-ttu-id="18e02-124">Set/getgamma</span><span class="sxs-lookup"><span data-stu-id="18e02-124">Set/GetGamma</span></span>](#setgetgamma)
-   [<span data-ttu-id="18e02-125">Impostazione/getnitidezza</span><span class="sxs-lookup"><span data-stu-id="18e02-125">Set/GetSharpness</span></span>](#setgetsharpness)
-   [<span data-ttu-id="18e02-126">Set/GetSaturation</span><span class="sxs-lookup"><span data-stu-id="18e02-126">Set/GetSaturation</span></span>](#setgetsaturation)
-   [<span data-ttu-id="18e02-127">Imposta/gettinta</span><span class="sxs-lookup"><span data-stu-id="18e02-127">Set/GetTint</span></span>](#setgettint)
-   [<span data-ttu-id="18e02-128">Set/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="18e02-128">Set/GetNoiseReduction</span></span>](#setgetnoisereduction)
-   [<span data-ttu-id="18e02-129">SetDestinationColorContext</span><span class="sxs-lookup"><span data-stu-id="18e02-129">SetDestinationColorContext</span></span>](#setdestinationcolorcontext)
-   [<span data-ttu-id="18e02-130">Set/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="18e02-130">Set/GetToneCurve</span></span>](#setgettonecurve)
-   [<span data-ttu-id="18e02-131">Set/getrotation</span><span class="sxs-lookup"><span data-stu-id="18e02-131">Set/GetRotation</span></span>](#setgetrotation)
-   [<span data-ttu-id="18e02-132">Set/GetRenderMode</span><span class="sxs-lookup"><span data-stu-id="18e02-132">Set/GetRenderMode</span></span>](#setgetrendermode)
-   [<span data-ttu-id="18e02-133">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="18e02-133">SetNotificationCallback</span></span>](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a><span data-ttu-id="18e02-134">QueryRawCapabilitiesInfo</span><span class="sxs-lookup"><span data-stu-id="18e02-134">QueryRawCapabilitiesInfo</span></span>

<span data-ttu-id="18e02-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) restituisce il set di funzionalità supportate per questo file non elaborato.</span><span class="sxs-lookup"><span data-stu-id="18e02-135">[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) returns the set of supported capabilities for this raw file.</span></span> <span data-ttu-id="18e02-136">La struttura [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="18e02-136">The [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) structure is defined as follows:</span></span>


```C++
struct WICRawCapabilitiesInfo
{
   UINT cbSize;
   UINT CodecMajorVersion;
   UINT CodecMinorVersion;
   WICRawCapabilities ExposureCompensationSupport;
   WICRawCapabilities ContrastSupport;
   WICRawCapabilities RGBWhitePointSupport;
   WICRawCapabilities NamedWhitePointSupport;
   UINT NamedWhitePointSupportMask;
   WICRawCapabilities KelvinWhitePointSupport;
   WICRawCapabilities GammaSupport;
   WICRawCapabilities TintSupport;
   WICRawCapabilities SaturationSupport;
   WICRawCapabilities SharpnessSupport;
   WICRawCapabilities NoiseReductionSupport;
   WICRawCapabilities DestinationColorProfileSupport;
   WICRawCapabilities ToneCurveSupport;
   WICRawRotationCapabilities RotationSupport;              
}
```



<span data-ttu-id="18e02-137">L'enumerazione [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) utilizzata in questa struttura è definita come segue:</span><span class="sxs-lookup"><span data-stu-id="18e02-137">The [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) enumeration used in this structure is defined as:</span></span>


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



<span data-ttu-id="18e02-138">Il campo finale è un'enumerazione [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) , definita come segue:</span><span class="sxs-lookup"><span data-stu-id="18e02-138">The final field is a [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) enumeration, defined as:</span></span>


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a><span data-ttu-id="18e02-139">LoadParameterSet</span><span class="sxs-lookup"><span data-stu-id="18e02-139">LoadParameterSet</span></span>

<span data-ttu-id="18e02-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) consente all'utente di specificare se usare come impostazioni di scatto, usare le impostazioni modificate dall'utente o richiedere al decodificatore di correggere automaticamente l'immagine.</span><span class="sxs-lookup"><span data-stu-id="18e02-140">[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) enables the user to specify whether to use As Shot settings, use user-adjusted settings, or request the decoder to auto-correct the image.</span></span>


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a><span data-ttu-id="18e02-141">GetCurrentParameterSet</span><span class="sxs-lookup"><span data-stu-id="18e02-141">GetCurrentParameterSet</span></span>

<span data-ttu-id="18e02-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) restituisce un **IPropertyBag2** con il set di parametri corrente.</span><span class="sxs-lookup"><span data-stu-id="18e02-142">[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) returns an **IPropertyBag2** with the current parameter set.</span></span> <span data-ttu-id="18e02-143">Il chiamante può quindi passare il set di parametri al codificatore da usare come opzioni del codificatore.</span><span class="sxs-lookup"><span data-stu-id="18e02-143">The caller can then pass this parameter set to the encoder to use as the encoder options.</span></span>

### <a name="setgetexposurecompensation"></a><span data-ttu-id="18e02-144">Set/GetExposureCompensation</span><span class="sxs-lookup"><span data-stu-id="18e02-144">Set/GetExposureCompensation</span></span>

<span data-ttu-id="18e02-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) e [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicano la compensazione dell'esposizione da applicare all'output finale.</span><span class="sxs-lookup"><span data-stu-id="18e02-145">[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) and [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicate the exposure compensation to apply to the final output.</span></span> <span data-ttu-id="18e02-146">L'intervallo valido per EV è-5,0 a + 5,0 si arresta.</span><span class="sxs-lookup"><span data-stu-id="18e02-146">The valid range for EV is –5.0 to +5.0 stops.</span></span>

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a><span data-ttu-id="18e02-147">Set/GetCurrentParameterRGB, set/GetNamedWhitePoint, set/GetwhitePointKelvin</span><span class="sxs-lookup"><span data-stu-id="18e02-147">Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin</span></span>

<span data-ttu-id="18e02-148">Queste funzioni forniscono tutti modi per ottenere e impostare il punto bianco, come un valore RGB, un set di impostazioni denominato o un valore Kelvin.</span><span class="sxs-lookup"><span data-stu-id="18e02-148">These functions all provide ways to get and set the white point, either as an RGB value, a preset named value, or as a Kelvin value.</span></span> <span data-ttu-id="18e02-149">L'intervallo accettabile per Kelvin è 1.500-30.000.</span><span class="sxs-lookup"><span data-stu-id="18e02-149">The acceptable range for Kelvin is 1,500 – 30,000.</span></span>

### <a name="setgetcontrast"></a><span data-ttu-id="18e02-150">Set/getcontrast</span><span class="sxs-lookup"><span data-stu-id="18e02-150">Set/GetContrast</span></span>

<span data-ttu-id="18e02-151">[**Getcontrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) e [**secontrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicano la quantità di contrasto da applicare all'output.</span><span class="sxs-lookup"><span data-stu-id="18e02-151">[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) and [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicate the amount of contrast to apply to the output.</span></span> <span data-ttu-id="18e02-152">L'intervallo valido per specificare il contrasto è da-1,0 a + 1,0, con il contrasto predefinito 0,0.</span><span class="sxs-lookup"><span data-stu-id="18e02-152">The valid range to specify contrast is –1.0 to +1.0, with the default contrast being 0.0.</span></span>

### <a name="setgetgamma"></a><span data-ttu-id="18e02-153">Set/getgamma</span><span class="sxs-lookup"><span data-stu-id="18e02-153">Set/GetGamma</span></span>

<span data-ttu-id="18e02-154">[**Getgamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) e [**segamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicano la gamma da applicare.</span><span class="sxs-lookup"><span data-stu-id="18e02-154">[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) and [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicate the Gamma to apply.</span></span> <span data-ttu-id="18e02-155">L'intervallo valido per gamma è compreso tra 0,2 e 5,0 e 1,0 è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="18e02-155">The valid range for Gamma is 0.2 to 5.0, with 1.0 being the default.</span></span> <span data-ttu-id="18e02-156">La gamma viene in genere implementata usando la funzione di alimentazione gamma tradizionale, ovvero una funzione di alimentazione lineare con guadagno Unity.</span><span class="sxs-lookup"><span data-stu-id="18e02-156">Gamma typically is implemented using the traditional Gamma power function (a linear power function with unity gain).</span></span> <span data-ttu-id="18e02-157">La luminosità è aumentata con un aumento della gamma e diminuisce come la gamma si avvicina a zero.</span><span class="sxs-lookup"><span data-stu-id="18e02-157">Brightness is increased with increasing Gamma and decreased as Gamma approaches zero.</span></span> <span data-ttu-id="18e02-158">(Si noti che il valore minimo è diverso da zero, perché zero genera un errore di divisione per zero nei calcoli gamma tradizionali.</span><span class="sxs-lookup"><span data-stu-id="18e02-158">(Note that the minimum value is non-zero, because zero would result in a divide-by-zero error in traditional Gamma calculations.</span></span> <span data-ttu-id="18e02-159">Il limite minimo logico è 1/max, motivo per cui il valore minimo è 0,2.</span><span class="sxs-lookup"><span data-stu-id="18e02-159">The logical minimum limit is 1/max, which is why the minimum is 0.2.)</span></span>

### <a name="setgetsharpness"></a><span data-ttu-id="18e02-160">Impostazione/getnitidezza</span><span class="sxs-lookup"><span data-stu-id="18e02-160">Set/GetSharpness</span></span>

<span data-ttu-id="18e02-161">[**Getnitidity**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) e [**senettity**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicano la quantità di nitidezza da applicare.</span><span class="sxs-lookup"><span data-stu-id="18e02-161">[**GetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) and [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicate the amount of sharpening to apply.</span></span> <span data-ttu-id="18e02-162">L'intervallo valido è compreso tra-1,0 e + 1,0, con 0,0 è la quantità predefinita di nitidezza e-1,0 che indica nessuna nitidezza.</span><span class="sxs-lookup"><span data-stu-id="18e02-162">The valid range is –1.0 to +1.0, with 0.0 being the default amount of sharpening, and –1.0 indicating no sharpening at all.</span></span>

### <a name="setgetsaturation"></a><span data-ttu-id="18e02-163">Set/GetSaturation</span><span class="sxs-lookup"><span data-stu-id="18e02-163">Set/GetSaturation</span></span>

<span data-ttu-id="18e02-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) e [**sesaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicano la quantità di saturazione da applicare.</span><span class="sxs-lookup"><span data-stu-id="18e02-164">[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) and [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicate the amount of saturation to apply.</span></span> <span data-ttu-id="18e02-165">L'intervallo valido per specificare la saturazione è da-1,0 a + 1,0, con 0,0 come saturazione normale,-1,0 che rappresenta la desaturazione completa e + 1,0 che rappresenta la saturazione completa.</span><span class="sxs-lookup"><span data-stu-id="18e02-165">The valid range to specify saturation is –1.0 to +1.0, with 0.0 being normal saturation, –1.0 representing complete desaturation, and +1.0 representing full saturation.</span></span>

### <a name="setgettint"></a><span data-ttu-id="18e02-166">Imposta/gettinta</span><span class="sxs-lookup"><span data-stu-id="18e02-166">Set/GetTint</span></span>

<span data-ttu-id="18e02-167">[**Gettint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) e [**totint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicano la tinta da applicare, su una polarizzazione verde/magenta.</span><span class="sxs-lookup"><span data-stu-id="18e02-167">[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) and [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicate the tint to apply, on a green/magenta bias.</span></span> <span data-ttu-id="18e02-168">L'intervallo valido è compreso tra-1,0 e + 1,0, con il verde sul lato negativo della scala e il magenta sul positivo.</span><span class="sxs-lookup"><span data-stu-id="18e02-168">The valid range is –1.0 to +1.0, with green being on the negative side of the scale and magenta on the positive.</span></span> <span data-ttu-id="18e02-169">La scala della tinta è definita ortogonale alla temperatura dei colori.</span><span class="sxs-lookup"><span data-stu-id="18e02-169">The tint scale is defined as orthogonal to color temperature.</span></span>

### <a name="setgetnoisereduction"></a><span data-ttu-id="18e02-170">Set/GetNoiseReduction</span><span class="sxs-lookup"><span data-stu-id="18e02-170">Set/GetNoiseReduction</span></span>

<span data-ttu-id="18e02-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) e [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicano la quantità di riduzione del rumore da applicare.</span><span class="sxs-lookup"><span data-stu-id="18e02-171">[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) and [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicate the amount of noise reduction to apply.</span></span> <span data-ttu-id="18e02-172">L'intervallo valido è compreso tra-1,0 e + 1,0, con 0,0 che indica la quantità predefinita di riduzione del rumore,-1,0 che indica nessuna riduzione del rumore e + 1,0 che indica la riduzione massima del rumore.</span><span class="sxs-lookup"><span data-stu-id="18e02-172">The valid range to is –1.0 to +1.0, with 0.0 indicating the default amount of noise reduction, –1.0 indicating no noise reduction and +1.0 indicating maximum noise reduction.</span></span>

### <a name="setdestinationcolorcontext"></a><span data-ttu-id="18e02-173">SetDestinationColorContext</span><span class="sxs-lookup"><span data-stu-id="18e02-173">SetDestinationColorContext</span></span>

<span data-ttu-id="18e02-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) specifica il profilo colori da applicare all'immagine.</span><span class="sxs-lookup"><span data-stu-id="18e02-174">[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) specifies the color profile to apply to the image.</span></span> <span data-ttu-id="18e02-175">È possibile chiamare [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) per recuperare il profilo colori corrente.</span><span class="sxs-lookup"><span data-stu-id="18e02-175">You can call [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) to retrieve the current color profile.</span></span>

### <a name="setgettonecurve"></a><span data-ttu-id="18e02-176">Set/GetToneCurve</span><span class="sxs-lookup"><span data-stu-id="18e02-176">Set/GetToneCurve</span></span>

<span data-ttu-id="18e02-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) e [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) specificano la curva di tono da applicare.</span><span class="sxs-lookup"><span data-stu-id="18e02-177">[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) and [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) specify the tone curve to apply.</span></span> <span data-ttu-id="18e02-178">Si supponga che l'interpolazione lineare tra punti.</span><span class="sxs-lookup"><span data-stu-id="18e02-178">Assume linear interpolation between points.</span></span> <span data-ttu-id="18e02-179">**PToneCurve** è una struttura [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) che contiene una matrice di strutture [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) e un conteggio del numero di punti nella matrice.</span><span class="sxs-lookup"><span data-stu-id="18e02-179">The **pToneCurve** is a [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) structure, which contains an array of [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) structures, and a count of the number of points in the array.</span></span>


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



<span data-ttu-id="18e02-180">Un [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contiene un valore di input e un valore di output.</span><span class="sxs-lookup"><span data-stu-id="18e02-180">A [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contains an input value and an output value.</span></span>


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



<span data-ttu-id="18e02-181">Quando il chiamante passa **null** nel parametro *pToneCurve* , è necessario passare di nuovo le dimensioni necessarie per [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) nel parametro *pcbActualToneCurveBufferSize* .</span><span class="sxs-lookup"><span data-stu-id="18e02-181">When the caller passes **NULL** in the *pToneCurve* parameter, you should pass back the required size for the [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) in the *pcbActualToneCurveBufferSize* parameter.</span></span>

### <a name="setgetrotation"></a><span data-ttu-id="18e02-182">Set/getrotation</span><span class="sxs-lookup"><span data-stu-id="18e02-182">Set/GetRotation</span></span>

<span data-ttu-id="18e02-183">[**Getrotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) e [**serotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indica il grado di rotazione da applicare.</span><span class="sxs-lookup"><span data-stu-id="18e02-183">[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) and [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indicate the degree of rotation to apply.</span></span> <span data-ttu-id="18e02-184">Una rotazione di 90,0 specifica una rotazione di 90 gradi in senso orario.</span><span class="sxs-lookup"><span data-stu-id="18e02-184">A rotation of 90.0 would specify a rotation of 90 degrees clockwise.</span></span> <span data-ttu-id="18e02-185">La differenza tra l'uso della **rotazione e l'impostazione della rotazione usando** il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) è che l'angolo di rotazione impostato con la **serotazione** deve essere reso permanente dal codec, mentre l'impostazione della rotazione tramite **CopyPixels** ruota solo l'immagine in memoria.</span><span class="sxs-lookup"><span data-stu-id="18e02-185">(The difference between using **SetRotation** and setting rotation using the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) method is that the rotation angle set using **SetRotation** should be persisted by the codec, while setting rotation through **CopyPixels** only rotates the image in memory.</span></span>

### <a name="setgetrendermode"></a><span data-ttu-id="18e02-186">Set/GetRenderMode</span><span class="sxs-lookup"><span data-stu-id="18e02-186">Set/GetRenderMode</span></span>

<span data-ttu-id="18e02-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) e [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicano il livello di qualità dell'output richiesto dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="18e02-187">[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) and [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicate the quality level of output the caller requires.</span></span> <span data-ttu-id="18e02-188">Quando un utente sta modificando i parametri, l'applicazione deve visualizzare un'approssimazione molto rapida dell'aspetto dell'immagine effettiva in caso di applicazione delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="18e02-188">When a user is adjusting parameters, the application should display a very fast approximation of what the actual image will look like if the changes are applied.</span></span> <span data-ttu-id="18e02-189">A questo scopo, l'immagine viene in genere visualizzata a risoluzione dello schermo o inferiore, invece della risoluzione effettiva dell'immagine, per fornire un feedback immediato all'utente.</span><span class="sxs-lookup"><span data-stu-id="18e02-189">For this purpose, the image is usually displayed at screen resolution or less, rather than the actual image resolution, to provide immediate feedback to the user.</span></span> <span data-ttu-id="18e02-190">Questa situazione si verifica quando un'applicazione richiede la qualità della modalità bozza, quindi questa operazione dovrebbe essere molto rapida.</span><span class="sxs-lookup"><span data-stu-id="18e02-190">This is when an application would request Draft Mode quality, so this should be very fast.</span></span> <span data-ttu-id="18e02-191">Quando l'utente ha apportato tutte le modifiche, le Visualizza in anteprima in modalità bozza e ha deciso di decodificare l'immagine completa con le impostazioni correnti, l'applicazione richiede una decodifica di qualità migliore.</span><span class="sxs-lookup"><span data-stu-id="18e02-191">When the user has made all changes, previewed them in draft mode, and decided to decode the full image with the current settings, the application requests a Best Quality decode.</span></span> <span data-ttu-id="18e02-192">Questa operazione viene in genere richiesta anche per la stampa.</span><span class="sxs-lookup"><span data-stu-id="18e02-192">This is usually also requested for printing.</span></span> <span data-ttu-id="18e02-193">Quando è necessario un ragionevole compromesso tra la velocità di una qualità, l'applicazione richiede la qualità normale.</span><span class="sxs-lookup"><span data-stu-id="18e02-193">Where a reasonable tradeoff between speed an quality is required, the application requests Normal Quality.</span></span>


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a><span data-ttu-id="18e02-194">SetNotificationCallback</span><span class="sxs-lookup"><span data-stu-id="18e02-194">SetNotificationCallback</span></span>

<span data-ttu-id="18e02-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registra una funzione di callback per il decodificatore da chiamare quando uno dei parametri di elaborazione non elaborati cambia.</span><span class="sxs-lookup"><span data-stu-id="18e02-195">[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registers a callback function for the decoder to call when any of the Raw processing parameters change.</span></span> <span data-ttu-id="18e02-196">La firma per [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) dispone di un solo metodo, denominato [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span><span class="sxs-lookup"><span data-stu-id="18e02-196">The signature for the [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) has only one method, called [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify).</span></span> <span data-ttu-id="18e02-197">**Notify** presenta un solo parametro, ovvero una maschera che indica quale dei parametri di elaborazione non elaborati sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="18e02-197">**Notify** has a single parameter, which is a mask that indicates which of the raw processing parameters have changed.</span></span>


```C++
HRESULT Notify ( UINT NotificationMask );
```



<span data-ttu-id="18e02-198">Viene eseguita un'operazione o sui valori seguenti per NotificationMask.</span><span class="sxs-lookup"><span data-stu-id="18e02-198">An OR operation is performed on the following values for the NotificationMask.</span></span>


```C++
WICRawChangeNotification_ExposureCompensation
WICRawChangeNotification_NamedWhitePoint
WICRawChangeNotification_KelvinWhitePoint
WICRawChangeNotification_RGBWhitePoint
WICRawChangeNotification_Contrast
WICRawChangeNotification_Gamma
WICRawChangeNotification_Sharpness
WICRawChangeNotification_Saturation
WICRawChangeNotification_Tint
WICRawChangeNotification_NoiseReduction
WICRawChangeNotification_DestinationColorContext
WICRawChangeNotification_ToneCurve
WICRawChangeNotification_Rotation
WICRawChangeNotification_RenderMode
```



## <a name="related-topics"></a><span data-ttu-id="18e02-199">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18e02-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="18e02-200">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="18e02-200">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="18e02-201">**IWICDevelopRaw**</span><span class="sxs-lookup"><span data-stu-id="18e02-201">**IWICDevelopRaw**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

<span data-ttu-id="18e02-202">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="18e02-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="18e02-203">Implementazione di IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="18e02-203">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="18e02-204">Implementazione di un codificatore di WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="18e02-204">Implementing a WIC-Enabled Encoder</span></span>](-wic-implementingwicencoder.md)
</dt> <dt>

[<span data-ttu-id="18e02-205">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="18e02-205">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="18e02-206">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="18e02-206">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



