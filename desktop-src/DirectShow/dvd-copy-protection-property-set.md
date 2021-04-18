---
description: Il set di proprietà di protezione copia DVD fornisce l'autenticazione delle informazioni di protezione copia da decrittografia hardware o software. Usare questa proprietà impostata per impedire la copia non autorizzata da DVD-video preregistrato.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Set di proprietà DVD Copy Protection (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14146ce0be19a4ed49c23517987a2c91a85da87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331637"
---
# <a name="dvd-copy-protection-property-set"></a>Set di proprietà di protezione copia DVD

Il set di proprietà di protezione copia DVD fornisce l'autenticazione delle informazioni di protezione copia da decrittografia hardware o software. Usare questa proprietà impostata per impedire la copia non autorizzata da DVD-video preregistrato.

Microsoft fornisce software che facilita il processo di autenticazione richiesto dallo schema di crittografia, consentendo in tal modo a un'unità DVD-ROM di autenticare e trasferire le chiavi con un DVD Decrypter. Microsoft non prevede alcun piano per la distribuzione di un DVD Decrypter e, al contrario, fornisce codice del sistema operativo che fungerà da agente per consentire l'autenticazione di decrittografia hardware o software.

Il navigatore DVD avvia e controlla il processo di scambio delle chiavi. Il minidriver DVD richiede solo l'implementazione delle proprietà seguenti. Altri componenti gestiscono il resto.

Ogni flusso di input DVD riceverà le proprietà di protezione della copia. Questo vale anche se lo stesso hardware controlla tutti i flussi DVD.

Le informazioni seguenti presentano le costanti e i tipi di dati necessari da usare per questa proprietà impostata nelle chiamate ai metodi [**IKsPropertySet**](ikspropertyset.md) . Fornisce valori per i parametri **GUID** (*GUIDPROPSET*), ID proprietà (*dwPropID*) e tipo di dati Property (*pPropData*).



|                   |                           |
|-------------------|---------------------------|
| GUID set di proprietà | \_CopyProt KSPROPSETID \_ |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>ID proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></td>
<td>Esegue una query per verificare se l'output del video è una definizione standard, ovvero un video componente analogico.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_COPY_MACROVISION</td>
<td>Si tratta di una proprietà di sola impostazione. Questa proprietà imposta il livello di protezione per la copia analogico per il codificatore NTSC nell'output finale del PIN di destinazione. USA <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_CHLG_KEY</td>
<td>In questa proprietà sono supportate entrambe le operazioni get e set. Un'operazione Get richiede al decodificatore di fornire la chiave di richiesta del bus. Un'operazione di impostazione fornisce al decodificatore la chiave della richiesta bus dall'unità DVD. I dati passati in questa proprietà saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DEC_KEY2</td>
<td>Si tratta di una proprietà di solo Get. Questa proprietà richiede che la chiave bus del decodificatore 2 venga trasferita all'unità DVD. I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_DISC_KEY</td>
<td>Proprietà di sola impostazione. Questa operazione fornisce la chiave del disco. La chiave è una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DVD_KEY1</td>
<td>Si tratta di una proprietà di sola impostazione. Questa proprietà fornisce la chiave del bus di unità DVD 1 al decodificatore. I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_REGION</td>
<td>Il codice dell'area richiede la definizione dell'area in cui è consentita la riproduzione del decodificatore come definito dal DVD Consortium. Questa area è definita come struttura di <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> .</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_SET_COPY_STATE</td>
<td>In questa proprietà sono supportati sia get che set. Get viene chiamato per primo per determinare se l'autenticazione è obbligatoria. Le proprietà del set sono indicazioni sulla fase di negoziazione della protezione da copia del filtro. I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</td>
<td>Se questa proprietà è <strong>true</strong>, il NAVIGAtore DVD non invia <strong>AM_UseNewCSSKey</strong> esempi prima di negoziare la chiave del disco. Vedere <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.<br/> Di sola lettura. I dati della proprietà sono un valore <strong>bool</strong> .<br/>
<blockquote>
[!Note]<br />
Si applica a Windows 7.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_TITLE_KEY</td>
<td>Si tratta di una proprietà di sola impostazione. Questa operazione fornisce la chiave del titolo del contenuto corrente. La chiave è una struttura di tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




