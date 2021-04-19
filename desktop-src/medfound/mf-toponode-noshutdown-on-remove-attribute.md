---
description: Specifica il modo in cui la sessione multimediale arresta un oggetto nella topologia.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: Attributo MF_TOPONODE_NOSHUTDOWN_ON_REMOVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308442"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a>MF \_ TOPONODE \_ noshutdown \_ sull' \_ attributo Remove

Specifica il modo in cui la sessione multimediale arresta un oggetto nella topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Questo attributo si applica ai tipi di nodo di topologia seguenti:

-   Nodi di output
-   Qualsiasi nodo di trasformazione che contiene una trasformazione di Media Foundation *asincrona* (MFT).

L'attributo può avere i valori seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>TRUE</strong></td>
<td>Quando la sessione multimediale passa a una nuova topologia o cancella la topologia corrente, non arresta l'oggetto che appartiene a questo nodo di topologia.</td>
</tr>
<tr class="even">
<td><strong>FALSE</strong></td>
<td>Quando la sessione multimediale passa a una nuova topologia o cancella la topologia corrente, arresta l'oggetto nodo, come indicato di seguito:
<ul>
<li>Nodi di output: la sessione chiama <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink:: Shutdown</strong></a> sul sink multimediale.</li>
<li>Nodi di trasformazione: la sessione chiama <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown:: Shutdown</strong></a> sulla MFT.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Il valore predefinito è **true**.

Se l'applicazione Accoda più topologie, è consigliabile impostare questo attributo su **false**. In caso contrario, gli oggetti della topologia potrebbero non essere arrestati correttamente.

Questo attributo non si applica quando l'applicazione arresta la sessione multimediale chiamando [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Quando la sessione multimediale viene arrestata, arresta sempre i sink del supporto e i MFTs asincroni nella topologia corrente.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs asincrono](asynchronous-mfts.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




