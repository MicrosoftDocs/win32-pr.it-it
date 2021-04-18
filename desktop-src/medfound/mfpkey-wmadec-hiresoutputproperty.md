---
description: Specifica se il decodificatore audio deve fornire un output a risoluzione elevata.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: Proprietà MFPKEY_WMADEC_HIRESOUTPUT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310266"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a>MFPKEY \_ WMADEC- \_ Proprietà HIRESOUTPUT

Specifica se il decodificatore audio deve fornire un output a risoluzione elevata.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACHiResOutput

## <a name="data-type"></a>Tipo di dati

**\_bool VT**

## <a name="default-value"></a>Valore predefinito

**VARIANTE \_ false**

## <a name="remarks"></a>Commenti

Impostare questa proprietà su VARIANT \_ true per decodificare il contenuto audio multicanale o a 24 bit oppure audio con una frequenza di campionamento superiore a 48.000 Hz. Se il contenuto è codificato in alta risoluzione, ma questa proprietà è VARIANT \_ false, si applicano i comportamenti seguenti:

-   L'output DMO sarà limitato a 16 bit, 48-KHz stereo.
-   Il MFT enumera le modalità di output limitate a 16 bit e non implicano modifiche al numero di canali o alla frequenza di campionamento.

Le proprietà dell'audio ad alta risoluzione vengono passate in una struttura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) , non in [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).

L'output a risoluzione elevata è disponibile solo se il decodificatore è in esecuzione in Windows XP o versione successiva. È possibile impostare questa proprietà indipendentemente dal sistema operativo in cui è in esecuzione l'applicazione. Nelle versioni di Windows precedenti a Windows XP, il decodificatore ignorerà questa impostazione e consegnerà l'output standard.

Molti lettori (incluso Windows Media Player 9 e versioni successive) impostano questo valore per tutto il contenuto.

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

 

 
