---
description: Specifica se il decodificatore audio deve fornire output ad alta risoluzione.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: MFPKEY_WMADEC_HIRESOUTPUT proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe5226babc8fd40875ec11cfa0b03345ba0b9c1a914b45b5ad79284f79d92130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872539"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a>Proprietà MFPKEY \_ WMADEC \_ HIRESOUTPUT

Specifica se il decodificatore audio deve fornire output ad alta risoluzione.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACHiResOutput

## <a name="data-type"></a>Tipo di dati

**VT \_ BOOL**

## <a name="default-value"></a>Valore predefinito

**VARIANT \_ FALSE**

## <a name="remarks"></a>Commenti

Impostare questa proprietà su VARIANT TRUE per decodificare contenuto audio multicanale o a 24 bit o audio con una frequenza di campionamento maggiore di \_ 48.000 Hz. Se il contenuto è codificato in alta risoluzione, ma questa proprietà è VARIANT \_ FALSE, si applicano i comportamenti seguenti:

-   L DMO output sarà limitato a stereo a 16 bit e 48 KHz.
-   MFT enumera le modalità di output limitate a 16 bit e non comporta modifiche nel numero di canali o nella frequenza di campionamento.

Le proprietà dell'audio ad alta risoluzione vengono passate in una [**struttura WAVEFORMATEXTENSIBLE,**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) non [**in WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85))

L'output ad alta risoluzione è disponibile solo se il decodificatore è in esecuzione Windows XP o versioni successive. È possibile impostare questa proprietà indipendentemente dal sistema operativo in cui è in esecuzione l'applicazione. Nelle versioni di Windows precedenti a Windows XP, il decodificatore ignorerà questa impostazione e fornisce l'output standard.

Molti lettori ,tra cui Windows Media Player serie 9 e versioni successive, impostano questo valore per tutto il contenuto.

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

 

 
