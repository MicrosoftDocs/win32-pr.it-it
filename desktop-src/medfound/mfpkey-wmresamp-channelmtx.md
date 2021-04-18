---
description: Specifica la matrice del canale utilizzata per convertire i canali di origine nei canali di destinazione (ad esempio, per convertire 5,1 in stereo).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: Proprietà MFPKEY_WMRESAMP_CHANNELMTX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310258"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a>MFPKEY \_ WMRESAMP- \_ Proprietà CHANNELMTX

Specifica la matrice del canale utilizzata per convertire i canali di origine nei canali di destinazione (ad esempio, per convertire 5,1 in stereo).

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo di dati

\_Array VT I4 VT \| \_

## <a name="applies-to"></a>Si applica a

-   [DSP ricampionatore audio](audioresampler.md)

## <a name="remarks"></a>Commenti

Il valore della proprietà è una matrice di coefficienti NS x ND, dove NS è il numero di canali di origine e ND è il numero di canali di destinazione. I coefficienti vengono specificati in decibel usando la formula seguente:

int (65536 \* 20 \* log10 (DB))

La matrice viene archiviata come matrice nell'ordine principale della riga in cui il numero di riga è il canale di origine e il numero di colonna è il canale di destinazione.

Quindi, se la matrice è la seguente:

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

Specificare quindi la matrice come:

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

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

 

 
