---
description: Ottiene l'immagine non filtrata memorizzata nella cache dal metodo IWiaPreview::GetNewPreview.
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: Metodo IWiaPreview::UpdatePreview (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b5f48462d926d96acebf4a74f0a843d82f9cd97190585b954565d5da649ff9f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549691"
---
# <a name="iwiapreviewupdatepreview-method"></a>Metodo IWiaPreview::UpdatePreview

Ottiene l'immagine non filtrata memorizzata nella cache dal [**metodo IWiaPreview::GetNewPreview.**](-wia-iwiapreview-getnewpreview.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lOptions* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Specifica se l'applicazione richiede al componente di anteprima di WIA 2.0 di passare un'area secondaria dell'immagine memorizzata nella cache o l'intera immagine memorizzata nella cache al filtro di elaborazione delle immagini.

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**


</dt> <dd>

Passare l'intera immagine memorizzata nella cache al filtro di elaborazione delle immagini.

</dd> </dl> </dd> <dt>

*pChildWiaItem* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Specifica un puntatore all'elemento [**IWiaItem2,**](-wia-iwiaitem2.md) che è un elemento figlio dell'elemento **IWiaItem2** specificato dal *parametro pWiaItem2* del [**metodo IWiaPreview::GetNewPreview.**](-wia-iwiapreview-getnewpreview.md) In caso contrario, se l'applicazione richiede un'anteprima dell'intero oggetto flat, specifica un puntatore al parametro *pWiaItem2* del **metodo IWiaPreview::GetNewPreview.** Quando *pChildWiaItem* è un elemento figlio del parametro *pWiaItem2* di **IWiaPreview::GetNewPreview,** questo elemento figlio viene in genere creato dal filtro di segmentazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo passa l'immagine non filtrata memorizzata nella cache tramite il filtro di elaborazione delle immagini, che quindi scrive i dati filtrati nel flusso fornito dall'applicazione. Il componente di anteprima di WIA 2.0 recupera questo flusso chiamando il metodo [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) del filtro di elaborazione delle immagini, che quindi chiama l'implementazione **GetNextStream** del callback dell'applicazione. Prima di **chiamare IWiaPreview::UpdatePreview**, un'applicazione deve chiamare [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) per acquisire l'immagine dallo scanner. In caso contrario, il metodo restituisce un errore.

Il componente di anteprima di WIA 2.0 archivia l'immagine non filtrata scaricata dal driver. È possibile che l'elemento WIA 2.0 passato a **IWiaPreview::UpdatePreview** rappresenti solo una piccola area dell'immagine scaricata dal driver. In questo caso, il componente di anteprima di WIA 2.0 taglia effettivamente questa area dall'immagine memorizzata nella cache prima di passarla al filtro di elaborazione delle immagini, che a sua volta passa i dati dell'immagine filtrati all'applicazione.

Perché un'applicazione passi l'intera immagine memorizzata nella cache al filtro di elaborazione delle immagini (che a sua volta la passa all'applicazione), deve impostare *lOptions* su **WiaPreviewReturnOriginalImage** quando chiama **IWiaPreview::UpdatePreview**. Quando si imposta *lOptions* su **WiaPreviewReturnOriginalImage**, l'applicazione deve assicurarsi che le impostazioni degli extent ([**WIA \_ IPS \_ XEXTENT**](-wia-wiaitempropscanneritem.md) e **WIA \_ IPS \_ YEXTENT**) dell'elemento passato in **IWiaPreview::UpdatePreview** corrispondano all'immagine full-cache. In questo caso, il filtro di elaborazione delle immagini non deve eseguire operazioni diverse. filtra semplicemente l'immagine, in base alle proprietà di *pChildWiaItem* (in genere in questo caso *pChildWiaItem* è lo stesso elemento passato a [**IWiaPreview::GetNewPreview).**](-wia-iwiapreview-getnewpreview.md) Le diverse aree secondarie vengono ignorate e l'intera immagine viene filtrata usando le stesse impostazioni. Esistono due motivi per cui un'applicazione può eseguire questa operazione.

1.  L'applicazione potrebbe non supportare la modifica delle impostazioni (ad esempio [**WIA \_ IPS \_ BRIGHTNESS**](-wia-wiaitempropscanneritem.md) e **WIA \_ IPS \_ CONTRAST)** singolarmente per ogni area rilevata dal filtro di segmentazione (o potrebbe anche non voler usare il filtro di segmentazione). È più semplice per l'applicazione chiamare **IWiaPreview::UpdatePreview** con **WiaPreviewReturnOriginalImage** in modo che riceva sempre l'immagine completa dal componente di anteprima di WIA 2.0.
2.  Il componente di anteprima di WIA 2.0 non supporta il formato di immagine dell'immagine di anteprima, nel qual caso non può eseguire le azioni per tagliare l'area desiderata. Il supporto del formato immagine del componente di anteprima di WIA 2.0 è limitato ai formati per i quali sono disponibili codificatori e decodificatori Windows GDI+ 1.1. Questi formati sono bitmap (BMP) (una bitmap che include BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) e Tagged Image File Format (TIFF).

Si noti che se l'applicazione passa **WiaPreviewReturnOriginalImage** a **IWiaPreview::UpdatePreview,** il componente di anteprima di WIA 2.0 può supportare qualsiasi formato di immagine o pixel.

**IWiaPreview::UpdatePreview** imposta la proprietà [**\_ \_ WIA DPS PREVIEW**](-wia-wiaitempropscannerdevice.md) (e la reimposta prima che venga restituita, a meno che non sia stata impostata in precedenza). Ciò consente al driver (e all'hardware) e al filtro di elaborazione delle immagini di sapere che l'elemento è un'analisi di anteprima.

Un'applicazione deve garantire che *pChildWiaItem* abbia lo stesso formato di immagine ([**WIA \_ IPA \_ FORMAT**](-wia-wiaitempropcommonitem.md)) e la stessa risoluzione ([**WIA \_ IPS \_ XRES**](-wia-wiaitempropscanneritem.md) e **WIA \_ IPS \_ YRES**) di *pWiaItem* quando è stato passato a [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Il formato dell'elemento figlio deve corrispondere al formato dell'immagine memorizzata nella cache del componente DI WINDOWS 2.0 Preview (il componente di anteprima di WIA 2.0 non esegue alcuna conversione di immagine).

## <a name="examples"></a>Esempio

UpdateRegion deve essere chiamato ogni volta che un utente modifica, ad esempio la luminosità o il contrasto per l'elemento figlio rappresentato da `dwRegionNumber` . Questo elemento figlio è stato creato in precedenza dal filtro di segmentazione ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md). L'immagine scritta in [IStream viene](/windows/win32/api/objidl/nn-objidl-istream) restituita dal metodo [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) dell'interfaccia di callback di trasferimento. Il codice per GetSubRegionItem viene omesso in questo esempio.

Dopo la chiamata a questa funzione, un'applicazione ridisegna in genere l'area sullo schermo.


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
