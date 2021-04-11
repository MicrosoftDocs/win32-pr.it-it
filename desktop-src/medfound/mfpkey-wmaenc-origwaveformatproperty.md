---
description: Specifica la struttura WAVEFORMATEX che descrive il contenuto audio di input.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: Proprietà MFPKEY_WMAENC_ORIGWAVEFORMAT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226915"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a>MFPKEY \_ WMAENC- \_ Proprietà ORIGWAVEFORMAT

Specifica la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) che descrive il contenuto audio di input.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACOriginalWaveFormat

## <a name="data-type"></a>Tipo di dati

VT \_ array \| VT \_ Ui1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) come matrice di byte)

## <a name="remarks"></a>Commenti

Quando si esegue la transcodifica di contenuto basato su Windows Media Audio a una velocità in bit inferiore, è possibile passare la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) del contenuto al codec per consentire al codec di ottimizzare gli algoritmi. Questa funzionalità, denominata ricompressione intelligente, fornisce risultati migliori rispetto alla decompressione del contenuto e quindi all'inserimento dei campioni PCM ricostruiti tramite il codec.

Quando si passa la struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) , includere eventuali byte aggiuntivi alla fine della struttura specificata da **WAVEFORMATEX. cbSize**.

Il codificatore audio accetta solo gli input e gli output per i quali il numero di canali, i bit per campione e la frequenza di campionamento sono identici. È possibile transcodificare il contenuto solo a una velocità in bit inferiore all'interno di tali parametri. In ogni caso, è necessario decodificare il contenuto e passare gli esempi non compressi come input al codificatore. L'impostazione di questa proprietà fornisce al codificatore alcune informazioni sull'elaborazione già eseguita sul contenuto.

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

 

 
