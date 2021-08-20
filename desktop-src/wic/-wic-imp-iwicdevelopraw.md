---
description: Implementazione di IWICDevelopRaw
ms.assetid: 08371790-b23b-4d2e-9aea-b2c95c854401
title: Implementazione di IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68a78705fcfb53651d1099d01d17d9ddff554df9632a5cc322db229bc04d38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965010"
---
# <a name="implementing-iwicdevelopraw"></a>Implementazione di IWICDevelopRaw

## <a name="iwicdevelopraw"></a>IWICDevelopRaw

[**L'interfaccia IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) espone le opzioni di elaborazione specifiche per l'elaborazione di immagini non elaborate. Tutti i codec non elaborati devono supportare **l'interfaccia IWICDevelopRaw.** Alcuni codec non elaborati potrebbero non essere in grado di supportare tutte le impostazioni esposte da questa interfaccia, ma è consigliabile supportare tutte le impostazioni che il codec è in grado di eseguire. Come minimo, ogni codec non elaborato deve implementare i [**metodi SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) e [**SetRenderMode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode)

Inoltre, alcuni metodi e interfacce facoltativi per altri codec sono fortemente consigliati per i codec non elaborati. Questi includono i [**metodi GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) e [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) nella classe del decodificatore a livello di contenitore e l'interfaccia [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) nella classe di decodifica a livello di frame.

Impostazioni impostati usando i metodi [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) devono essere resi persistenti dal codec in modo coerente con il modo in cui vengono resi persistenti gli altri metadati, ma non sovrascrivere mai le impostazioni originali di "As Shot". Tramite la persistenza dei metadati e l'implementazione [**di LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) e [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), è possibile abilitare le applicazioni di elaborazione non elaborata per recuperare e applicare le impostazioni di elaborazione tra le sessioni.

Uno scopo principale [**dell'interfaccia IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) è consentire agli sviluppatori di applicazioni di creare un'interfaccia utente per modificare i parametri non elaborati che funzioneranno nel modo più coerente possibile tra codec diversi. Si supponga che un utente finale regola i parametri usando un controllo dispositivo di scorrimento, con i relativi valori minimo e massimo mappati agli intervalli minimo e massimo per il parametro. Per supportare questa operazione, è consigliabile considerare tutti gli intervalli di parametri come lineari. Per assicurarsi che i controlli dispositivo di scorrimento non siano troppo sensibili, è necessario supportare anche un intervallo il più ampio possibile per ogni parametro, coprendo almeno il 50% dell'intervallo massimo possibile. Ad esempio, se l'intervallo massimo possibile di contrasto è da grigio puro a bianco e nero puro, con il valore predefinito mappato a 0,0, l'intervallo minimo supportato da un codec è compreso almeno a metà tra il valore predefinito e il grigio puro nell'estremità inferiore (-1,0), a almeno a metà tra il valore predefinito e il bianco e nero puro nell'estremità alta (+1,0).


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



-   [QueryRawCapabilitiesInfo](#queryrawcapabilitiesinfo)
-   [LoadParameterSet](#loadparameterset)
-   [GetCurrentParameterSet](#getcurrentparameterset)
-   [Set/GetExposureCompensation](#setgetexposurecompensation)
-   [Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [Set/GetContrast](#setgetcontrast)
-   [Set/GetGamma](#setgetgamma)
-   [Set/GetSharpness](#setgetsharpness)
-   [Set/GetSaturation](#setgetsaturation)
-   [Set/GetTint](#setgettint)
-   [Set/GetNoiseReduction](#setgetnoisereduction)
-   [SetDestinationColorContext](#setdestinationcolorcontext)
-   [Set/GetToneCurve](#setgettonecurve)
-   [Set/GetRotation](#setgetrotation)
-   [Set/GetRenderMode](#setgetrendermode)
-   [SetNotificationCallback](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a>QueryRawCapabilitiesInfo

[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) restituisce il set di funzionalità supportate per questo file non elaborato. La [**struttura WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) è definita come segue:


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



[**L'enumerazione WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) usata in questa struttura è definita come:


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



Il campo finale è [**un'enumerazione WICRawRotationCapabilities,**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) definita come:


```C++
enum WICRawRotationCapabilities                    
{
   WICRawRotationCapabilityNotSupported,
   WICRawRotationCapabilityGetSupported,
   WICRawRotationCapabilityNinetyDegreesSupported
   WICRawRotationCapabilityFullySupported
}
```



### <a name="loadparameterset"></a>LoadParameterSet

[**LoadParameterSet consente**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) all'utente di specificare se usare le impostazioni as shot, usare le impostazioni regolate dall'utente o richiedere al decodificatore di correggere automaticamente l'immagine.


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a>GetCurrentParameterSet

[**GetCurrentParameterSet restituisce**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) un **oggetto IPropertyBag2** con il set di parametri corrente. Il chiamante può quindi passare questo set di parametri al codificatore da usare come opzioni del codificatore.

### <a name="setgetexposurecompensation"></a>Set/GetExposureCompensation

[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) e [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicano la compensazione dell'esposizione da applicare all'output finale. L'intervallo valido per EV è compreso tra -5,0 e +5,0 arresti.

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a>Set/GetCurrentParameterRGB, Set/GetNamedWhitePoint, Set/GetwhitePointKelvin

Tutte queste funzioni consentono di ottenere e impostare il punto bianco, come valore RGB, set di impostazioni denominato o come valore Kelvin. L'intervallo accettabile per Kelvin è 1.500 - 30.000.

### <a name="setgetcontrast"></a>Set/GetContrast

[**GetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) e [**SetContrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicano la quantità di contrasto da applicare all'output. L'intervallo valido per specificare il contrasto è compreso tra -1,0 e +1,0, con il contrasto predefinito 0,0.

### <a name="setgetgamma"></a>Set/GetGamma

[**GetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) e [**SetGamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicano la gamma da applicare. L'intervallo valido per Gamma è compreso tra 0,2 e 5,0, con 1,0 come valore predefinito. Gamma viene in genere implementata usando la funzione di alimentazione Gamma tradizionale (una funzione di potenza lineare con guadagno unity). La luminosità aumenta con l'aumento di Gamma e diminuisce quando Gamma si avvicina a zero. Si noti che il valore minimo è diverso da zero, perché zero restituirebbe un errore di divisione per zero nei calcoli Gamma tradizionali. Il limite minimo logico è 1/max, motivo per cui il valore minimo è 0,2.

### <a name="setgetsharpness"></a>Set/GetSharpness

[**GetSharpness e**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) [**SetSharpness**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicano la quantità di affilatura da applicare. L'intervallo valido è compreso tra -1,0 e +1,0, con 0,0 come quantità predefinita di affilatura e -1,0 che indica nessuna affilatura.

### <a name="setgetsaturation"></a>Set/GetSaturation

[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) e [**SetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicano la quantità di saturazione da applicare. L'intervallo valido per specificare la saturazione è compreso tra -1,0 e +1,0, con 0,0 come saturazione normale, –1,0 che rappresenta la desaturazione completa e +1,0 che rappresenta la saturazione completa.

### <a name="setgettint"></a>Set/GetTint

[**GetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) e [**SetTint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicano la tinta da applicare, in base a una distorsione verde/magenta. L'intervallo valido è compreso tra -1,0 e +1,0, con il verde sul lato negativo della scala e magenta sul positivo. La scala della tinta è definita come temperatura ortogonale a colore.

### <a name="setgetnoisereduction"></a>Set/GetNoiseReduction

[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) e [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicano la quantità di riduzione del rumore da applicare. L'intervallo valido per è compreso tra -1,0 e +1,0, con 0,0 che indica la quantità predefinita di riduzione del rumore, -1,0 che indica nessuna riduzione del rumore e +1,0 che indica la riduzione massima del rumore.

### <a name="setdestinationcolorcontext"></a>SetDestinationColorContext

[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) specifica il profilo colori da applicare all'immagine. È possibile chiamare [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) per recuperare il profilo colori corrente.

### <a name="setgettonecurve"></a>Set/GetToneCurve

[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) e [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) specificano la curva tonale da applicare. Si supponga l'interpolazione lineare tra i punti. **pToneCurve** è una struttura [**WICRawToneCurve,**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) che contiene una matrice di [**strutture WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) e un conteggio del numero di punti nella matrice.


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



[**WiCRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contiene un valore di input e un valore di output.


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



Quando il chiamante passa **NULL** nel *parametro pToneCurve,* è necessario passare nuovamente le dimensioni necessarie per [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) nel *parametro pcbActualToneCurveBufferSize.*

### <a name="setgetrotation"></a>Set/GetRotation

[**GetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) e [**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indicano il grado di rotazione da applicare. Una rotazione di 90,0 specifica una rotazione di 90 gradi in senso orario. La differenza tra l'uso di **SetRotation** e l'impostazione della rotazione tramite il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) è che l'angolo di rotazione impostato con **SetRotation** deve essere mantenuto dal codec, mentre l'impostazione della rotazione **tramite CopyPixels** ruota solo l'immagine in memoria.

### <a name="setgetrendermode"></a>Set/GetRenderMode

[**GetRenderMode e**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicano il livello di qualità dell'output richiesto dal chiamante. Quando un utente modifica i parametri, l'applicazione deve visualizzare un'approssimazione molto veloce dell'aspetto dell'immagine effettiva se vengono applicate le modifiche. A questo scopo, l'immagine viene in genere visualizzata con risoluzione dello schermo o inferiore, anziché con la risoluzione effettiva dell'immagine, per fornire un feedback immediato all'utente. Questo è il momento in cui un'applicazione richiede la qualità della modalità bozza, quindi dovrebbe essere molto veloce. Quando l'utente ha apportato tutte le modifiche, le ha visualizzate in anteprima in modalità bozza e ha deciso di decodificare l'immagine completa con le impostazioni correnti, l'applicazione richiede una decodifica best quality. Questa operazione viene in genere richiesta anche per la stampa. Se è necessario un compromesso ragionevole tra velocità e qualità, l'applicazione richiede qualità normale.


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a>SetNotificationCallback

[**SetNotificationCallback registra**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) una funzione di callback per il decodificatore da chiamare quando viene modificato uno dei parametri di elaborazione non elaborati. La firma per [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) ha un solo metodo, denominato [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify). **Notify** ha un singolo parametro, ovvero una maschera che indica quale dei parametri di elaborazione non elaborati è stato modificato.


```C++
HRESULT Notify ( UINT NotificationMask );
```



Viene eseguita un'operazione OR sui valori seguenti per NotificationMask.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Implementazione di IWICBitmapSourceTransform](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[Implementazione di un WIC-Enabled codificatore](-wic-implementingwicencoder.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



