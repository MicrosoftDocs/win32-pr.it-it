---
description: Specifica i coefficienti di riduzione forniti dall'autore per la decodifica dell'audio multicanale per un numero di canali inferiore rispetto al contenuto del flusso codificato.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: Proprietà MFPKEY_WMADEC_FOLDDOWN_MATRIX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309112"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a>MFPKEY \_ WMADEC \_ - \_ Proprietà matrice FOLDDOWN

Specifica i coefficienti di riduzione forniti dall'autore per la decodifica dell'audio multicanale per un numero di canali inferiore rispetto al contenuto del flusso codificato.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACFoldDownXToYChannels

g \_ wszWMACFoldXToYChannelsZ

## <a name="data-type"></a>Tipo di dati

**\_VT array \| VT \_ I4**

## <a name="remarks"></a>Commenti

Un decodificatore audio può fungere da oggetto DMO (DirectX Media Object) o come trasformazione Media Foundation (MFT). Per informazioni su quando un decodificatore funge da DMO o da un MFT, vedere le pagine di riferimento del singolo codec in [oggetti codec](codecobjects.md).

Quando si utilizza un decodificatore come DMO, il decodificatore è in grado di eseguire la riduzione del canale ed è possibile enumerare i tipi di supporti di output ridotti chiamando [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).

Quando si usa un decodificatore come MFT, per impostazione predefinita il decodificatore non esegue alcuna riduzione e non offre i tipi di supporti di output ridotti. Un decodificatore che funge da MFT eseguirà la riduzione solo se vengono impostati coefficienti di riduzioni personalizzati usando la proprietà **MFPKEY \_ WMADEC \_ FOLDDOWN \_ Matrix** .

Se la proprietà della **\_ \_ \_ matrice MFPKEY WMADEC FOLDDOWN** non è impostata sul decodificatore audio MFT e si vuole eseguire una riduzione, è possibile usare (come MFT) il processore del segnale digitale del ricampionatore audio.

Il valore di questa proprietà è una stringa che contiene i coefficienti di riduzione in un elenco delimitato da virgole di valori interi. L'elenco deve contenere un numero di numeri interi per ogni canale nel contenuto codificato uguale al numero di canali nel contenuto decodificato.

Se il coefficiente è zero, il valore da utilizzare nella stringa deve essere "-2147483648". in caso contrario, il valore viene calcolato utilizzando l'equazione: 20 \* 65536 \* log10 (x).

I coefficienti sono elencati nell'ordine della maschera del canale, come definito dalle costanti della maschera di canale incluse nel file di intestazione mmreg. h. Pertanto, i primi due valori di un canale da 6 a 2 rivolte verso il basso rappresentano le parti del canale di output sinistro e il canale di output destro costituito dal canale sinistro centrale nel flusso del canale 6.

È necessario impostare questa proprietà solo se i valori di riduzioni specificati dall'autore sono mantenuti con il contenuto codificato. In caso contrario, lasciare che il decodificatore effettui calcoli.

Il codec Windows Media Audio 10 Professional attualmente supporta solo la riduzione a due canali.

Se la proprietà [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) è impostata su **DSSPEAKER \_ surround**, il codec ignorerà i coefficienti di riduzioni forniti dall'autore e ridurrà a un segnale a 2 canali che può essere elaborato dal decodificatore della matrice del destinatario. Ciò consente alle apparecchiature surround di fornire quattro canali. Questa modalità è supportata solo se l'origine è 5,1. Il codec può ridurre solo 8 canali a 2 canali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
