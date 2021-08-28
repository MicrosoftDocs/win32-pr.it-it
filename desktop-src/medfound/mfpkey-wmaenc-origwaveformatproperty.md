---
description: Specifica la struttura WAVEFORMATEX che descrive il contenuto audio di input.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: MFPKEY_WMAENC_ORIGWAVEFORMAT proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df477daa61e39eb6b2a86aa26c27de4088e943d41f40ac9b708a0201698088c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113141"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a>Proprietà MFPKEY \_ WMAENC \_ ORIGWAVEFORMAT

Specifica la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) che descrive il contenuto audio di input.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACOriginalWaveFormat

## <a name="data-type"></a>Tipo di dati

VT \_ ARRAY \| VT \_ UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) come matrice di byte)

## <a name="remarks"></a>Commenti

Quando si esegue Windows contenuto basato su Audio multimediale a una velocità in bit inferiore, è possibile passare la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) del contenuto al codec per consentire al codec di ottimizzare gli algoritmi. Questa funzionalità, denominata ricompressione intelligente, offre risultati migliori rispetto alla decompressione del contenuto e alla ricostinzione dei campioni PCM ricostruiti attraverso il codec.

Quando si passa la struttura [**WAVEFORMATEX,**](/previous-versions/dd757713(v=vs.85)) includere eventuali byte aggiuntivi alla fine della struttura specificata da **WAVEFORMATEX.cbSize**.

Il codificatore audio accetta solo input e output per i quali il numero di canali, i bit per campione e la frequenza di campionamento sono identici. È possibile transcodificare il contenuto solo a una velocità in bit inferiore all'interno di tali parametri. In ogni caso, è necessario decodificare il contenuto e passare gli esempi non compressi come input al codificatore. L'impostazione di questa proprietà fornisce al codificatore alcune informazioni sull'elaborazione già eseguita sul contenuto.

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

 

 
