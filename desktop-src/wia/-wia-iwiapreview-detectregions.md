---
description: "Richiama il filtro di segmentazione del driver e passa l'immagine non filtrata memorizzata nella cache dal metodo IWiaPreview:: GetNewPreview al filtro."
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: Metodo IWiaPreview::D etectRegions (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226150"
---
# <a name="iwiapreviewdetectregions-method"></a>IWiaPreview::D Metodo etectRegions

Richiama il filtro di segmentazione del driver e passa l'immagine non filtrata memorizzata nella cache dal metodo [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) al filtro.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Non usato. Impostato su zero (0).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                               | Descrizione                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | L'operazione è riuscita.<br/>              |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Il driver non supporta la segmentazione.<br/> |
| <dl> <dt>**in caso contrario**</dt> </dl>  | Codice di errore COM standard.<br/>                |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questa funzione, un'applicazione deve chiamare [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .

Quando il componente Windows Image Acquisition (WIA) 2,0 Preview chiama **IWiaPreview::D etectregions**, richiama il filtro di segmentazione del driver e passa l'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) passata in precedenza a [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Passa anche l'immagine memorizzata nella cache internamente al filtro. Il filtro di segmentazione usa l'immagine memorizzata nella cache per creare gli extent figlio.

Se un'applicazione modifica le proprietà dell'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dopo aver chiamato [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md), è necessario ripristinare le proprietà originali prima che l'applicazione chiami **IWiaPreview::D etectregions**. Usare [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) e [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) per ripristinare le proprietà originali.

**IWiaPreview::D etectregions** viene usato per determinare le "aree secondarie" dell'immagine memorizzata nella cache. Per ogni area secondaria rilevata, viene creato un nuovo elemento figlio WIA 2,0 sotto l'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) . Per ogni elemento figlio, il filtro di segmentazione deve impostare i valori per le seguenti proprietà WIA 2,0: WIA \_ IPS \_ XPos, WIA \_ IPS \_ YPos, WIA \_ IPS \_ stampa e WIA \_ IP \_ YEXTENT. Un filtro più avanzato Imposta altre proprietà WIA 2,0, ad esempio \_ gli indirizzi IP WIA \_ deasimmetria \_ X e WIA \_ IP \_ desfasamento \_ Y, se il driver supporta la deasimmetria. Le \_ Proprietà WIA IPS \_ XPos, WIA \_ IPS \_ YPos, WIA \_ IPS \_ stampa e WIA \_ IPS \_ YEXTENT rappresentano il rettangolo di delimitazione dell'area da analizzare.

Il driver potrebbe non supportare la segmentazione. Prima di chiamare **IWiaPreview::D etectregions**, un'applicazione in genere controlla se il driver supporta la \_ proprietà di segmentazione degli indirizzi IP WIA \_ . Se la proprietà non è implementata, la segmentazione non è supportata e **IWiaPreview::D etectregions** ha esito negativo E restituisce e \_ NOTIMPL.

L'applicazione deve pulire gli elementi figlio creati chiamando **IWiaPreview::D etectregions**. Se, ad esempio, un'applicazione effettua una chiamata aggiuntiva a **IWiaPreview::D etectregions** sullo stesso elemento, deve pulire gli elementi figlio precedenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




