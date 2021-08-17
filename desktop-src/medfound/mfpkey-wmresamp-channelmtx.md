---
description: Specifica la matrice di canali, usata per convertire i canali di origine nei canali di destinazione, ad esempio per convertire la versione 5.1 in stereo.
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: MFPKEY_WMRESAMP_CHANNELMTX proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326cfe27632204f2975ac8b7c3a605c666464f8f62846a5c622a469f2f6e104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689255"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a>Proprietà MFPKEY \_ WMRESAMP \_ CHANNELMTX

Specifica la matrice di canali, usata per convertire i canali di origine nei canali di destinazione, ad esempio per convertire la versione 5.1 in stereo.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo di dati

VT \_ I4 \| VT \_ ARRAY

## <a name="applies-to"></a>Si applica a

-   [Audio Resampler DSP](audioresampler.md)

## <a name="remarks"></a>Commenti

Il valore della proprietà è una matrice di coefficienti Ns x Nd, dove Ns è il numero di canali di origine e Nd è il numero di canali di destinazione. I coefficienti vengono specificati in decibel usando la formula seguente:

(int) (65536 \* 20 \* log10(dB))

La matrice viene archiviata come matrice nell'ordine principale della riga, dove il numero di riga è il canale di origine e il numero di colonna è il canale di destinazione.

Pertanto, se la matrice è la seguente:

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

specificare quindi la matrice come:

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

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

 

 
