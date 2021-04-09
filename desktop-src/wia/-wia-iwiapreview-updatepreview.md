---
description: "Ottiene l'immagine non filtrata memorizzata nella cache dal metodo IWiaPreview:: GetNewPreview."
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'Metodo IWiaPreview:: UpdatePreview (WIA. h)'
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
ms.openlocfilehash: 4a5d469179f341f3bad5d2b9b5ed25a5715be694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129418"
---
# <a name="iwiapreviewupdatepreview-method"></a>Metodo IWiaPreview:: UpdatePreview

Ottiene l'immagine non filtrata memorizzata nella cache dal metodo [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lOptions* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica se l'applicazione richiede il componente WIA 2,0 Preview per passare un'area secondaria dell'immagine memorizzata nella cache o l'intera immagine memorizzata nella cache al filtro di elaborazione delle immagini.

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**


</dt> <dd>

Passa l'intera immagine memorizzata nella cache al filtro di elaborazione delle immagini.

</dd> </dl> </dd> <dt>

*pChildWiaItem* \[ in\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Specifica un puntatore all'elemento [_ *IWiaItem2* *](-wia-iwiaitem2.md) , che è un elemento figlio dell'elemento **IWiaItem2** specificato dal parametro *pWiaItem2* del metodo [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . In alternativa, se l'applicazione richiede un'anteprima dell'intero piano, specifica un puntatore al parametro *pWiaItem2* del metodo **IWiaPreview:: GetNewPreview** . Quando *pChildWiaItem* è figlio del parametro *pWiaItem2* di **IWiaPreview:: GetNewPreview**, questo elemento figlio viene in genere creato dal filtro di segmentazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo passa l'immagine memorizzata nella cache e non filtrata tramite il filtro di elaborazione dell'immagine, che quindi scrive i dati filtrati nel flusso fornito dall'applicazione. Il componente WIA 2,0 Preview recupera questo flusso chiamando il metodo [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) del filtro di elaborazione dell'immagine, che quindi chiama l'implementazione **GetNextStream** del callback dell'applicazione. Prima di chiamare **IWiaPreview:: UpdatePreview**, un'applicazione deve prima chiamare [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) per acquisire l'immagine dallo scanner; in caso contrario, il metodo restituisce un errore.

Il componente WIA 2,0 Preview archivia l'immagine non filtrata scaricata dal driver. È possibile che l'elemento WIA 2,0 passato in **IWiaPreview:: UpdatePreview** rappresenti solo una piccola area dell'immagine scaricata dal driver. Se questo è il caso, il componente WIA 2,0 Preview interrompe effettivamente questa area dall'immagine memorizzata nella cache prima di passarla al filtro di elaborazione dell'immagine, che a sua volta passa i dati dell'immagine filtrata all'applicazione.

Affinché un'applicazione passi l'intera immagine memorizzata nella cache al filtro di elaborazione dell'immagine, che a sua volta lo passa all'applicazione, deve impostare *lOptions* su **WiaPreviewReturnOriginalImage** quando si chiama **IWiaPreview:: UpdatePreview**. Quando si imposta *lOptions* su **WiaPreviewReturnOriginalImage**, l'applicazione deve garantire che le impostazioni dell'extent ([**WIA \_ IPS \_ stampa**](-wia-wiaitempropscanneritem.md) e **WIA \_ IPS \_ YEXTENT**) dell'elemento passato a **IWiaPreview:: UpdatePreview** corrispondano all'immagine memorizzata nella cache completa. Il filtro di elaborazione delle immagini non deve eseguire alcuna operazione diversa in questo caso. Filtra semplicemente l'immagine, in base alle proprietà di *pChildWiaItem* , in genere in questo caso *pChildWiaItem* è lo stesso elemento passato a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Le diverse aree secondarie vengono ignorate e l'intera immagine viene filtrata utilizzando le stesse impostazioni. Ci sono due motivi per cui un'applicazione esegue questa operazione.

1.  L'applicazione potrebbe non supportare la modifica delle impostazioni, ad esempio la [**\_ \_ luminosità degli indirizzi IP**](-wia-wiaitempropscanneritem.md) WIA e il **\_ \_ contrasto degli indirizzi IP WIA**, singolarmente per ogni area rilevata dal filtro di segmentazione (oppure potrebbe non voler usare anche il filtro di segmentazione). È più semplice per l'applicazione chiamare **IWiaPreview:: UpdatePreview** con **WiaPreviewReturnOriginalImage** in modo che riceva sempre l'immagine completa dal componente WIA 2,0 Preview.
2.  Il componente WIA 2,0 Preview non supporta il formato di immagine dell'immagine di anteprima, nel qual caso non può eseguire le azioni per tagliare l'area desiderata. Il supporto del formato immagine del componente WIA 2,0 Preview è limitato ai formati per i quali sono presenti codificatori e decodificatori di Windows GDI+ 1,1. Questi formati sono bitmap (BMP) (bitmap che include BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) e Tagged Image File Format (TIFF).

Si noti che se l'applicazione passa **WiaPreviewReturnOriginalImage** a **IWiaPreview:: UpdatePreview**, il componente di anteprima WIA 2,0 può supportare qualsiasi formato immagine o pixel.

**IWiaPreview:: UpdatePreview** imposta la proprietà di [**\_ \_ Anteprima WIA DPS**](-wia-wiaitempropscannerdevice.md) (e la Reimposta prima della restituzione, a meno che non sia stata impostata in precedenza). In questo modo, il driver (e l'hardware) e il filtro di elaborazione delle immagini sanno che l'elemento è un'analisi di anteprima.

Un'applicazione deve garantire che *pChildWiaItem* abbia lo stesso formato di immagine [**( \_ \_ formato ipa WIA**](-wia-wiaitempropcommonitem.md)) e la risoluzione ([**WIA \_ IPS \_ XRES**](-wia-wiaitempropscanneritem.md) e **WIA \_ IPS \_ YRES**) come *pWiaItem* aveva quando è stato passato a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Il formato dell'elemento figlio deve corrispondere al formato dell'immagine memorizzata nella cache del componente WIA 2,0 Preview (il componente di anteprima WIA 2,0 non esegue alcuna conversione dell'immagine).

## <a name="examples"></a>Esempio

UpdateRegion deve essere chiamato ogni volta che un utente cambia, ad esempio, la luminosità o il contrasto per l'elemento figlio rappresentato da `dwRegionNumber` . Questo elemento figlio è stato precedentemente creato dal filtro di segmentazione ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md). L'immagine scritta in [IStream](/windows/win32/api/objidl/nn-objidl-istream) viene restituita dal metodo [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) dell'interfaccia di callback di trasferimento. Il codice per GetSubRegionItem viene omesso in questo esempio.

Dopo che questa funzione è stata chiamata, un'applicazione in genere ridisegni l'area sullo schermo.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
