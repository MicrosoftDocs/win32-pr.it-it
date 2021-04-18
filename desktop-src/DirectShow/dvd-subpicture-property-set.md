---
description: Le proprietà del sottoimmagine DVD controllano il colore, il contrasto e l'output della visualizzazione dell'immagine.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Set di proprietà della sottoimmagine DVD (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2706bd0a7f078fb7352e70e8f8eb62f5dea948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329263"
---
# <a name="dvd-subpicture-property-set"></a>Set di proprietà della sottoimmagine DVD

Le proprietà del sottoimmagine DVD controllano il colore, il contrasto e l'output della visualizzazione dell'immagine.

Le informazioni seguenti presentano le costanti e i tipi di dati necessari da usare per questa proprietà impostata nelle chiamate ai metodi [**IKsPropertySet**](ikspropertyset.md) . Fornisce valori per i parametri **GUID** (*GUIDPROPSET*), ID proprietà (*dwPropID*) e tipo di dati Property (*pPropData*).



|                   |                            |
|-------------------|----------------------------|
| GUID set di proprietà | \_DvdSubPic KSPROPSETID \_ |



 



| ID proprietà                           | Descrizione                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Proprietà am \_ DVDSUBPIC \_ composizione \_ su | Proprietà di sola impostazione che Abilita o Disabilita la visualizzazione dell'immagine. DirectShow definisce la **\_ Proprietà am \_ composita \_ sul** tipo di dati booleano per questa proprietà, nonché la \_ Proprietà PAM \_ composita \_ in come puntatore a questo tipo di dati. **True** indica che viene visualizzata la sottoimmagine, **false** indica che è disabilitata. Per ulteriori informazioni, vedere la parte WDM del DDK di Windows. |
| \_Proprietà am \_ DVDSUBPIC \_ HLI          | Proprietà set-only che specifica un rettangolo di subimmagine o schermata il cui colore o contrasto verrà modificato. Il tipo di dati è [**\_ \_ SPHLI Property**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli). Vedere la sezione Osservazioni.                                                                                                                                                                                |
| \_ \_ tavolozza DVDSUBPIC della proprietà am \_      | Imposta la tavolozza per un'immagine. Il tipo di dati è [**\_ \_ SPPAL Property**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Commenti

La **proprietà \_ am \_ DVDSUBPIC \_ HLI** è impostata su Only. Specifica un rettangolo di subimmagine o schermata il cui colore o contrasto verrà modificato. Questo comportamento è diverso da quello della specifica DVD-Video, in quanto il navigatore DVD di Microsoft analizza tutte le informazioni sul pulsante e sulla tastiera e passa un solo rettangolo di evidenziazione al decodificatore dell'immagine in un determinato momento. Di conseguenza, le informazioni sull'evidenziazione vengono inviate al decodificatore più spesso di quanto sia presente nel flusso di DVD.

Le informazioni di evidenziazione arrivano in modo asincrono al flusso di dati. Il decodificatore usa i timestamp di inizio e fine dell'evidenziazione per correlare le informazioni di evidenziazione alle informazioni relative all'immagine, se presenti. Se il decodificatore non ha ricevuto informazioni sul flusso di sottoimmagine per i timestamp richiesti, il decodificatore presuppone che le informazioni di evidenziazione siano autonome e non si applichino a un'immagine. In questo caso, il decodificatore presuppone che il colore e le informazioni sul contrasto siano tutti dello stesso colore.

I dati non sono interamente in formato DVD. Microsoft fornisce una struttura aggiuntiva di tipo [**am \_ Property \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) che viene passata come parametro a questa proprietà. Questa struttura descrive il pulsante attualmente selezionato dalle informazioni di evidenziazione del DVD.

Il navigatore DVD elabora tutte le informazioni sulla sequenza di tasti e invia nuove informazioni di evidenziazione ogni volta che viene modificato lo stato di un pulsante. Le informazioni descrivono solo una modalità di un pulsante alla volta. Include un rettangolo di visualizzazione nelle coordinate dei pixel dello schermo o una visualizzazione dell'immagine, se presente. La struttura contiene anche informazioni sul colore e sul contrasto, ma solo per lo stato attuale del pulsante attualmente selezionato. Il formato è definito nella specifica DVD.

Le informazioni relative all'evidenziazione contengono timestamp di inizio e di fine. Si trovano nelle stesse unità di altri timestamp, con due eccezioni: un timestamp di inizio di 0xFFFFFFFF indica che la proprietà Highlight è valida al momento della ricezione e un timestamp di fine 0xFFFFFFFF indica che la proprietà Highlight è valida fino a quando non viene ricevuta l'evidenziazione successiva.

Il campo HLISS è definito nella specifica DVD. Un valore pari a zero indica che tutte le evidenziazioni non sono valide e che il decodificatore deve disabilitare tutte le evidenziazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




