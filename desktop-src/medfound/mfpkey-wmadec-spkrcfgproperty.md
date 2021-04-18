---
description: Specifica la configurazione dell'altoparlante nel computer client.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: Proprietà MFPKEY_WMADEC_SPKRCFG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528567"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a>MFPKEY \_ WMADEC- \_ Proprietà SPKRCFG

Specifica la configurazione dell'altoparlante nel computer client.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMACSpeakerConfig

## <a name="data-type"></a>Tipo di dati

**\_UI4 VT**

## <a name="default-value"></a>Valore predefinito

Non viene presupposta alcuna configurazione specifica del altoparlante.

## <a name="remarks"></a>Commenti

È necessario impostare questo valore su una delle costanti o i valori indicati nella tabella seguente. Le costanti sono definite in Microsoft DirectSound e sono elencate di seguito per praticità. Per risolvere questi nomi costanti per il compilatore, è necessario includere DSOUND. h.



| Costante             | Valore      | Descrizione                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ diretto | 0x00000000 | L'audio viene passato direttamente, senza essere configurato per gli speaker. |
| \_cuffia DSSPEAKER | 0x00000001 | Il computer client è dotato di cuffie.                             |
| \_mono DSSPEAKER      | 0x00000002 | Il computer client è dotato di un altoparlante Monoaural.                    |
| DSSPEAKER \_ quad      | 0x00000003 | Il computer client è dotato di altoparlanti quadrifonica.                  |
| DSSPEAKER \_ stereo    | 0x00000004 | Il computer client è dotato di altoparlanti stereo.                        |
| DSSPEAKER \_ surround  | 0x00000005 | Il computer client è dotato di altoparlanti con audio surround a quattro canali.   |
| \_5POINT1 DSSPEAKER   | 0x00000006 | Il computer client è dotato di cinque altoparlanti e un subwoofer.          |
| \_7POINT1 DSSPEAKER   | 0x00000007 | Il computer client è dotato di sette altoparlanti e un subwoofer.         |



 

Il valore impostato per questa proprietà determina i formati di output enumerati dal codec per l'audio multicanale.

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

 

 




