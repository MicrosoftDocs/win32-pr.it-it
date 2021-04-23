---
description: Le proprietà dell'immagine secondaria DVD controllano il colore, il contrasto e l'output della visualizzazione dell'immagine secondaria.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Set di proprietà Dvd Subpicture (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a45b83595e8657ee0c60f39cd67f2d0e4c71511
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909089"
---
# <a name="dvd-subpicture-property-set"></a>DVD Subpicture Property Set

Le proprietà dell'immagine secondaria DVD controllano il colore, il contrasto e l'output della visualizzazione dell'immagine secondaria.

Le informazioni seguenti presentano le costanti e i tipi di dati necessari da usare per questo set di proprietà nelle chiamate ai [**metodi IKsPropertySet.**](ikspropertyset.md) Fornisce i valori per i **parametri GUID** (*guidPropSet*), ID proprietà (*dwPropID*) e tipo di dati della proprietà (*pPropData*).



| Label | Valore |
|-------------------|----------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ DvdSubPic |



 



| ID proprietà                           | Descrizione                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ PROPERTY \_ DVDSUBPIC \_ COMPOSIT \_ ON | Proprietà di sola impostazione che abilita o disabilita la visualizzazione delle immagini secondarie. DirectShow definisce il tipo di dati booleano **AM \_ PROPERTY COMPOSIT \_ \_ ON** per questa proprietà, nonché PAM PROPERTY COMPOSIT ON come puntatore \_ a questo tipo di \_ \_ dati. **TRUE** indica la visualizzazione dell'immagine secondaria, **FALSE** indica la disabilitazione. Per altre informazioni, vedere la parte WDM di Windows DDK. |
| PROPRIETÀ AM \_ \_ DVDSUBPIC \_ HLI          | Proprietà di sola impostazione che specifica un rettangolo di immagine secondaria o schermo il cui colore o contrasto verrà modificato. Il tipo di dati [**è AM \_ PROPERTY \_ SPHLI.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) Vedere la sezione Osservazioni.                                                                                                                                                                                |
| PROPRIETÀ AM \_ \_ DVDSUBPIC \_ PALETTE      | Imposta la tavolozza per un'immagine secondaria. Il tipo di dati [**è AM \_ PROPERTY \_ SPPAL.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal)                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Commenti

La **proprietà AM PROPERTY \_ \_ DVDSUBPIC \_ HLI** è di sola impostazione. Specifica un rettangolo di immagine secondaria o schermo il cui colore o contrasto verrà modificato. Ciò differisce dalla specifica DVD-Video, in cui lo strumento di navigazione DVD Microsoft analizza tutte le informazioni su pulsanti e tastiera e passa un solo rettangolo di evidenziazione al decodificatore di immagini secondarie in un determinato momento. Di conseguenza, le informazioni di evidenziazione vengono inviate al decodificatore più spesso di quanto non sia presente nel flusso DVD.

Le informazioni di evidenziazione arrivano in modo asincrono al flusso di dati. Il decodificatore usa gli indicatori di ora di inizio e fine evidenziati per correlare le informazioni di evidenziazione alle informazioni sull'immagine secondaria pertinente, se presenti. Se il decodificatore non ha ricevuto informazioni sul flusso di immagini secondarie per i timestamp richiesti, il decodificatore presuppone che le informazioni di evidenziazione siano autonome e non si applicano a un'immagine secondaria. In questo caso, il decodificatore presuppone che le informazioni sul colore e sul contrasto siano tutte dello stesso colore.

I dati non sono interamente in formato disco DVD. Microsoft fornisce una struttura aggiuntiva di [**tipo AM \_ PROPERTY \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) che viene passata come parametro a questa proprietà. Questa struttura descrive il pulsante attualmente selezionato dalle informazioni di evidenziazione dvd.

Lo strumento di spostamento DVD elabora tutte le informazioni sulla sequenza di tasti e invia nuove informazioni di evidenziazione ogni volta che cambia lo stato di un pulsante. Le informazioni descrivono una sola modalità di un pulsante alla volta. Include un rettangolo di visualizzazione in coordinate pixel dello schermo o una visualizzazione dell'immagine secondaria, se presente. La struttura contiene anche informazioni sul colore e sul contrasto, ma solo per lo stato corrente del pulsante attualmente selezionato. Il formato è definito nella specifica DVD.

Le informazioni di evidenziazione contengono timestamp di inizio e fine. Queste sono nelle stesse unità degli altri timestamp, con due eccezioni: un timestamp di inizio di 0xFFFFFFFF indica che la proprietà highlight è valida al momento della ricezione e un timestamp di fine di 0xFFFFFFFF indica che la proprietà highlight è valida fino all'evidenziazione successiva ricevuta.

Il campo HLISS è definito nella specifica DVD. Il valore zero indica che tutte le evidenziazioni non sono valide e che il decodificatore deve disabilitare tutte le evidenziazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




