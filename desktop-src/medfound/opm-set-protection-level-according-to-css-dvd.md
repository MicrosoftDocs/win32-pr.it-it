---
description: Imposta il livello di protezione HDCP per la riproduzione di DVD, seguendo le regole CSS (Dvd Content Scramble System).
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2290f8d0dd17e01d482c197a54448a3317b11f80840579c2ddd05f01b6103840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101906"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a>OPM \_ IMPOSTA IL LIVELLO DI PROTEZIONE IN BASE AL DVD \_ \_ \_ \_ \_ \_ CSS

Imposta il livello di protezione HDCP per la riproduzione di DVD, seguendo le regole CSS (Dvd Content Scramble System).



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID del comando | OPM \_ IMPOSTA IL LIVELLO DI PROTEZIONE IN BASE AL DVD \_ \_ \_ \_ \_ \_ CSS                                                |
| Dati di input   | Struttura [**PARAMETERS \_ OPM SET PROTECTION \_ \_ LEVEL \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Commenti

Questo comando viene usato per impostare High-Bandwidth hdcp (Digital protezione del contenuto) durante la riproduzione di DVD standard. A differenza [**del comando OPM \_ SET PROTECTION \_ \_ LEVEL,**](opm-set-protection-level.md) se HDCP non può essere impostato per qualche motivo, questo comando non arresta la riproduzione. Le regole CSS dvd contengono un provisioning "best effort" per i lettori. In caso contrario, questo comando è identico al **comando OPM \_ SET PROTECTION \_ \_ LEVEL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandi OPM](opm-commands.md)
</dt> </dl>

 

 




