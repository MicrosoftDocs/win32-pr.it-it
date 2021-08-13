---
description: Specifica i coefficienti di riduzione forniti dall'autore per decodificare l'audio multicanale per un numero di canali inferiore a quello contenuto nel flusso codificato.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: MFPKEY_WMADEC_FOLDDOWN_MATRIX proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb1b9eb1259c2a8c23f7b993699e1c51f17c09636afd7d19de23ce033fd269fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463161"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a>Proprietà MFPKEY \_ WMADEC \_ FOLDDOWN \_ MATRIX

Specifica i coefficienti di riduzione forniti dall'autore per decodificare l'audio multicanale per un numero di canali inferiore a quello contenuto nel flusso codificato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACFoldDownXToYChannels

g \_ wszWMACFoldXToYChannelsZ

## <a name="data-type"></a>Tipo di dati

**VT \_ ARRAY \| VT \_ I4**

## <a name="remarks"></a>Commenti

Un decodificatore audio può fungere da oggetto multimediale DirectX (DMO) o da Media Foundation transform (MFT). Per informazioni su quando un decodificatore funge da DMO o MFT, vedere le singole pagine di riferimento del codec in [Codec Objects (Oggetti codec).](codecobjects.md)

Quando si usa un decodificatore come DMO, il decodificatore può eseguire la fold down del canale ed è possibile enumerare i tipi di supporti di output rilevati chiamando [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).

Quando si usa un decodificatore come MFT, per impostazione predefinita il decodificatore non eseguirà alcuna operazione di fold down e non offrirà tipi di supporti di output folded down. Un decodificatore che funge da MFT eseguirà l'operazione di fold down solo se vengono impostati coefficienti di fold-down personalizzati usando la proprietà **MFPKEY \_ WMADEC \_ FOLDDOWN \_ MATRIX.**

Se la proprietà **MFPKEY \_ WMADEC \_ FOLDDOWN \_ MATRIX** non è impostata sul decodificatore audio MFT e si vuole eseguire una ripiegamento, è possibile usare (come MFT) il processore del segnale digitale del resampler audio.

Il valore di questa proprietà è una stringa contenente coefficienti di tipo fold-down in un elenco delimitato da virgole di valori interi. L'elenco deve contenere un numero di numeri interi per ogni canale nel contenuto codificato uguale al numero di canali nel contenuto decodificato.

Se il coefficiente è zero, il valore da usare nella stringa deve essere "-2147483648"; in caso contrario, il valore viene calcolato usando l'equazione: 20 \* 65536 \* log10(x).

I coefficienti sono elencati in ordine di maschera del canale, come definito dalle costanti channel mask incluse nel file di intestazione mmreg.h. Di conseguenza, i primi due valori in un'impostazione di 6-a-2 channel fold-down rappresentano le parti del canale di output sinistro e del canale di output destro che sono rappresentate dal canale centrale sinistro nel flusso a 6 canali.

È consigliabile impostare questa proprietà solo se i valori di tipo fold-down forniti dall'autore vengono resi persistenti con il contenuto codificato. In caso contrario, consentire al decodificatore di eseguire i propri calcoli.

Il codec Windows Media Audio 10 Professional attualmente supporta solo il fold-down a due canali.

Se la proprietà [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) è impostata su **DSSPEAKER \_ SURROUND,** il codec ignorerà i coefficienti di fold down forniti dall'autore e si rilascierà a un segnale a 2 canali che può essere elaborato dal decodificatore di matrice del ricevitore. In questo modo le apparecchiature di surround possono distribuire quattro canali. Questa modalità è supportata solo se l'origine è 5.1. Il codec può solo convertire da 8 canali a 2 canali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 
