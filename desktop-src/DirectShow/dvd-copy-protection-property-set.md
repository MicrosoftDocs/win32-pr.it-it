---
description: Il set di proprietà Protezione copia DVD fornisce l'autenticazione delle informazioni di protezione della copia dai decrittografatori hardware o software. Usare questa proprietà impostata per impedire la copia non autorizzata da DVD-Video preregistrato.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Set di proprietà DVD Copy Protection (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382243a6071fa73361df13ae933d259979686a06
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909479"
---
# <a name="dvd-copy-protection-property-set"></a>Set di proprietà protezione copia DVD

Il set di proprietà Protezione copia DVD fornisce l'autenticazione delle informazioni di protezione della copia dai decrittografatori hardware o software. Usare questa proprietà impostata per impedire la copia non autorizzata da DVD-Video preregistrato.

Microsoft fornisce software che facilita il processo di autenticazione richiesto dallo schema di crittografia, consentendo così a un'unità DVD-ROM di autenticare e trasferire le chiavi con un decrittografatore DVD. Microsoft non prevede di fornire un decrittografatore DVD e, al contrario, fornisce il codice del sistema operativo che fungerà da agente per abilitare l'autenticazione dei decrittografatori hardware o software.

Lo strumento di spostamento DVD avvia e controlla il processo di scambio delle chiavi. Il minidriver DVD deve implementare solo le proprietà seguenti. Gli altri componenti gestiscono il resto.

Ogni flusso di input DVD riceverà le proprietà di protezione della copia. Questo vale anche se lo stesso hardware controlla tutti i flussi DVD.

Le informazioni seguenti illustrano le costanti e i tipi di dati necessari da usare per questo set di proprietà nelle chiamate ai [**metodi IKsPropertySet.**](ikspropertyset.md) Fornisce i valori per i **parametri GUID** (*guidPropSet*), ID proprietà (*dwPropID*) e tipo di dati della proprietà (*pPropData*).



| Label | Valore |
|-------------------|---------------------------|
| GUID set di proprietà | AM \_ KSPROPSETID \_ CopyProt |



 



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
<td>Esegue una query per determinare se l'output video è di definizione standard, video con componente analogico.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_COPY_MACROVISION</td>
<td>Si tratta di una proprietà di sola impostazione. Questa proprietà imposta il livello di protezione della copia analoga per il codificatore NTSC all'estremità di output del pin ricevente. Usa <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_CHLG_KEY</td>
<td>Entrambe le operazioni get e set sono supportate in questa proprietà. Un'operazione get richiede al decodificatore di fornire la chiave di richiesta del bus. Un'operazione set fornisce al decodificatore la chiave di richiesta del bus dall'unità DVD. I dati passati in questa proprietà saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DEC_KEY2</td>
<td>Si tratta di una proprietà di sola lettura. Questa proprietà richiede che la chiave bus 2 del decodificatore sia trasferita all'unità DVD. I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_DISC_KEY</td>
<td>Proprietà di sola impostazione. In questo modo viene fornita la chiave del disco. La chiave è una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DVD_KEY1</td>
<td>Si tratta di una proprietà di sola impostazione. Questa proprietà fornisce al decodificatore la chiave bus dell'unità DVD 1. I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_REGION</td>
<td>Il codice dell'area richiede la definizione dell'area in cui il decodificatore può riprodurre come definito dal consorzio DVD. Questa area è definita come <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> struttura.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_SET_COPY_STATE</td>
<td>Sia get che set sono supportati in questa proprietà. Get viene chiamato per primo per determinare se è necessaria l'autenticazione. Le proprietà del set indicano la fase di negoziazione della protezione della copia in cui viene immesso il filtro. I dati passati saranno una struttura di tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</td>
<td>Se questa proprietà è <strong>TRUE,</strong>lo strumento di navigazione DVD non invia AM_UseNewCSSKey <strong>esempi</strong> prima di negoziare la chiave del disco. Vedere <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.<br/> Di sola lettura. I dati della proprietà sono un <strong>valore BOOL.</strong><br/>
<blockquote>
[!Note]<br />
Si applica a Windows 7.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_TITLE_KEY</td>
<td>Si tratta di una proprietà di sola impostazione. In questo modo viene fornita la chiave del titolo dal contenuto corrente. La chiave è una struttura di tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Set di proprietà](property-sets.md)
</dt> </dl>

 

 




