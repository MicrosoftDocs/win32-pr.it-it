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
# <a name="implementing-iwicdevelopraw"></a>Implementazione di IWICDevelopRaw

## <a name="iwicdevelopraw"></a>IWICDevelopRaw

L'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) espone opzioni di elaborazione specifiche per l'elaborazione di immagini non elaborate. Tutti i codec RAW devono supportare l'interfaccia **IWICDevelopRaw** . Alcuni codec non elaborati potrebbero non essere in grado di supportare tutte le impostazioni esposte da questa interfaccia, ma è necessario supportare tutte le impostazioni che il codec è in grado di eseguire. Come minimo, ogni codec RAW deve implementare i metodi [**serotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) e [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) .

Inoltre, alcuni metodi e interfacce facoltativi per altri codec sono fortemente consigliati per i codec non elaborati. Sono inclusi i metodi [**getpreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) e [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) sulla classe decodificatore a livello di contenitore e l'interfaccia [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) nella classe Decode a livello di frame.

Le impostazioni impostate usando i metodi [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) devono essere rese persistenti dal codec in modo coerente con il modo in cui gli altri metadati sono persistenti, ma è consigliabile non sovrascrivere mai le impostazioni originali "come shot". Salvando in modo permanente i metadati e implementando [**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) e [**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), è possibile abilitare le applicazioni di elaborazione non elaborate per recuperare e applicare le impostazioni di elaborazione tra le sessioni.

Uno degli scopi principali dell'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) è consentire agli sviluppatori di applicazioni di creare un'interfaccia utente per la regolazione di parametri non elaborati che funzioneranno il più possibile in modo coerente tra diversi codec. Si supponga che un utente finale modifichi i parametri usando un controllo dispositivo di scorrimento, con i valori minimo e massimo di cui è stato eseguito il mapping agli intervalli minimo e massimo per il parametro. Per supportare questa operazione, è necessario eseguire ogni sforzo per considerare tutti gli intervalli di parametri come lineari. Per assicurarsi che i controlli dispositivo di scorrimento non siano eccessivamente sensibili, è necessario supportare anche un intervallo più ampio possibile per ogni parametro, coprendo almeno il 50% dell'intervallo massimo possibile. Ad esempio, se l'intervallo massimo possibile di contrasto è da grigio puro a puro nero e bianco, con il valore predefinito di cui viene eseguito il mapping a 0,0, l'intervallo minimo supportato da un codec è compreso tra almeno metà tra il valore predefinito e il grigio puro nell'estremità inferiore (-1,0), almeno a metà tra il valore predefinito e il nero puro e il bianco all'estremità superiore (+ 1,0)


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
-   [Set/GetCurrentParameterRGB, set/GetNamedWhitePoint, set/GetwhitePointKelvin](#setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin)
-   [Set/getcontrast](#setgetcontrast)
-   [Set/getgamma](#setgetgamma)
-   [Impostazione/getnitidezza](#setgetsharpness)
-   [Set/GetSaturation](#setgetsaturation)
-   [Imposta/gettinta](#setgettint)
-   [Set/GetNoiseReduction](#setgetnoisereduction)
-   [SetDestinationColorContext](#setdestinationcolorcontext)
-   [Set/GetToneCurve](#setgettonecurve)
-   [Set/getrotation](#setgetrotation)
-   [Set/GetRenderMode](#setgetrendermode)
-   [SetNotificationCallback](#setnotificationcallback)

### <a name="queryrawcapabilitiesinfo"></a>QueryRawCapabilitiesInfo

[**QueryRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-queryrawcapabilitiesinfo) restituisce il set di funzionalità supportate per questo file non elaborato. La struttura [**WICRawCapabilitiesInfo**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawcapabilitiesinfo) viene definita nel modo seguente:


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



L'enumerazione [**WICRawCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawcapabilities) utilizzata in questa struttura è definita come segue:


```C++
enum WICRawCapabilities 
{   
   WICRawCapabilityNotSupported,
   WICRawCapabilityGetSupported,
   WICRawCapabilityFullySupported
}
```



Il campo finale è un'enumerazione [**WICRawRotationCapabilities**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrotationcapabilities) , definita come segue:


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

[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) consente all'utente di specificare se usare come impostazioni di scatto, usare le impostazioni modificate dall'utente o richiedere al decodificatore di correggere automaticamente l'immagine.


```C++
enum WICRawParameterSet
{
   WICAsShotParameterSet,
   WICUserAdjustedParameterSet,
   WICAutoAdjustedParameterSet
}
```



### <a name="getcurrentparameterset"></a>GetCurrentParameterSet

[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset) restituisce un **IPropertyBag2** con il set di parametri corrente. Il chiamante può quindi passare il set di parametri al codificatore da usare come opzioni del codificatore.

### <a name="setgetexposurecompensation"></a>Set/GetExposureCompensation

[**GetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getexposurecompensation) e [**SetExposureCompensation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setexposurecompensation) indicano la compensazione dell'esposizione da applicare all'output finale. L'intervallo valido per EV è-5,0 a + 5,0 si arresta.

### <a name="setgetcurrentparameterrgb-setgetnamedwhitepoint-setgetwhitepointkelvin"></a>Set/GetCurrentParameterRGB, set/GetNamedWhitePoint, set/GetwhitePointKelvin

Queste funzioni forniscono tutti modi per ottenere e impostare il punto bianco, come un valore RGB, un set di impostazioni denominato o un valore Kelvin. L'intervallo accettabile per Kelvin è 1.500-30.000.

### <a name="setgetcontrast"></a>Set/getcontrast

[**Getcontrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcontrast) e [**secontrast**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setcontrast) indicano la quantità di contrasto da applicare all'output. L'intervallo valido per specificare il contrasto è da-1,0 a + 1,0, con il contrasto predefinito 0,0.

### <a name="setgetgamma"></a>Set/getgamma

[**Getgamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getgamma) e [**segamma**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setgamma) indicano la gamma da applicare. L'intervallo valido per gamma è compreso tra 0,2 e 5,0 e 1,0 è il valore predefinito. La gamma viene in genere implementata usando la funzione di alimentazione gamma tradizionale, ovvero una funzione di alimentazione lineare con guadagno Unity. La luminosità è aumentata con un aumento della gamma e diminuisce come la gamma si avvicina a zero. (Si noti che il valore minimo è diverso da zero, perché zero genera un errore di divisione per zero nei calcoli gamma tradizionali. Il limite minimo logico è 1/max, motivo per cui il valore minimo è 0,2.

### <a name="setgetsharpness"></a>Impostazione/getnitidezza

[**Getnitidity**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsharpness) e [**senettity**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsharpness) indicano la quantità di nitidezza da applicare. L'intervallo valido è compreso tra-1,0 e + 1,0, con 0,0 è la quantità predefinita di nitidezza e-1,0 che indica nessuna nitidezza.

### <a name="setgetsaturation"></a>Set/GetSaturation

[**GetSaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getsaturation) e [**sesaturation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setsaturation) indicano la quantità di saturazione da applicare. L'intervallo valido per specificare la saturazione è da-1,0 a + 1,0, con 0,0 come saturazione normale,-1,0 che rappresenta la desaturazione completa e + 1,0 che rappresenta la saturazione completa.

### <a name="setgettint"></a>Imposta/gettinta

[**Gettint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettint) e [**totint**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settint) indicano la tinta da applicare, su una polarizzazione verde/magenta. L'intervallo valido è compreso tra-1,0 e + 1,0, con il verde sul lato negativo della scala e il magenta sul positivo. La scala della tinta è definita ortogonale alla temperatura dei colori.

### <a name="setgetnoisereduction"></a>Set/GetNoiseReduction

[**GetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getnoisereduction) e [**SetNoiseReduction**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnoisereduction) indicano la quantità di riduzione del rumore da applicare. L'intervallo valido è compreso tra-1,0 e + 1,0, con 0,0 che indica la quantità predefinita di riduzione del rumore,-1,0 che indica nessuna riduzione del rumore e + 1,0 che indica la riduzione massima del rumore.

### <a name="setdestinationcolorcontext"></a>SetDestinationColorContext

[**SetDestinationColorContext**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setdestinationcolorcontext) specifica il profilo colori da applicare all'immagine. È possibile chiamare [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) per recuperare il profilo colori corrente.

### <a name="setgettonecurve"></a>Set/GetToneCurve

[**GetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-gettonecurve) e [**SetToneCurve**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-settonecurve) specificano la curva di tono da applicare. Si supponga che l'interpolazione lineare tra punti. **PToneCurve** è una struttura [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) che contiene una matrice di strutture [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) e un conteggio del numero di punti nella matrice.


```C++
struct WICRawToneCurve 
{
   UINT cPoints;
   WICRawToneCurvePoint aPoints[];
}
```



Un [**WICRawToneCurvePoint**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurvepoint) contiene un valore di input e un valore di output.


```C++
struct WICRawToneCurvePoint 
{
   double Input;
   double Output;
}
```



Quando il chiamante passa **null** nel parametro *pToneCurve* , è necessario passare di nuovo le dimensioni necessarie per [**WICRawToneCurve**](/windows/desktop/api/Wincodec/ns-wincodec-wicrawtonecurve) nel parametro *pcbActualToneCurveBufferSize* .

### <a name="setgetrotation"></a>Set/getrotation

[**Getrotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrotation) e [**serotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) indica il grado di rotazione da applicare. Una rotazione di 90,0 specifica una rotazione di 90 gradi in senso orario. La differenza tra l'uso della **rotazione e l'impostazione della rotazione usando** il metodo [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) è che l'angolo di rotazione impostato con la **serotazione** deve essere reso permanente dal codec, mentre l'impostazione della rotazione tramite **CopyPixels** ruota solo l'immagine in memoria.

### <a name="setgetrendermode"></a>Set/GetRenderMode

[**GetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getrendermode) e [**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) indicano il livello di qualità dell'output richiesto dal chiamante. Quando un utente sta modificando i parametri, l'applicazione deve visualizzare un'approssimazione molto rapida dell'aspetto dell'immagine effettiva in caso di applicazione delle modifiche. A questo scopo, l'immagine viene in genere visualizzata a risoluzione dello schermo o inferiore, invece della risoluzione effettiva dell'immagine, per fornire un feedback immediato all'utente. Questa situazione si verifica quando un'applicazione richiede la qualità della modalità bozza, quindi questa operazione dovrebbe essere molto rapida. Quando l'utente ha apportato tutte le modifiche, le Visualizza in anteprima in modalità bozza e ha deciso di decodificare l'immagine completa con le impostazioni correnti, l'applicazione richiede una decodifica di qualità migliore. Questa operazione viene in genere richiesta anche per la stampa. Quando è necessario un ragionevole compromesso tra la velocità di una qualità, l'applicazione richiede la qualità normale.


```C++
enum WICRawRenderMode
{
   WICRawRenderModeDraftMode,
   WICRawRenderModeNormalQuality ,
   WICRawRenderModeBestQuality
}
```



### <a name="setnotificationcallback"></a>SetNotificationCallback

[**SetNotificationCallback**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setnotificationcallback) registra una funzione di callback per il decodificatore da chiamare quando uno dei parametri di elaborazione non elaborati cambia. La firma per [**IWICDevelopRawNotificationCallback**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdeveloprawnotificationcallback) dispone di un solo metodo, denominato [**Notify**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdeveloprawnotificationcallback-notify). **Notify** presenta un solo parametro, ovvero una maschera che indica quale dei parametri di elaborazione non elaborati sono stati modificati.


```C++
HRESULT Notify ( UINT NotificationMask );
```



Viene eseguita un'operazione o sui valori seguenti per NotificationMask.


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

[Implementazione di un codificatore di WIC-Enabled](-wic-implementingwicencoder.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



