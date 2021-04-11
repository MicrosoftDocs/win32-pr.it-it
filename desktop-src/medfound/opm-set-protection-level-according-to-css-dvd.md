---
description: Imposta il livello di protezione HDCP per la riproduzione DVD, seguendo le regole CSS (Content Scramble System) del DVD.
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130494"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a>\_impostazione del \_ \_ livello di protezione di OPM \_ \_ in base al \_ \_ DVD CSS

Imposta il livello di protezione HDCP per la riproduzione DVD, seguendo le regole CSS (Content Scramble System) del DVD.



| Requisito | Valore |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID comando | \_impostazione del \_ \_ livello di protezione di OPM \_ \_ in base al \_ \_ DVD CSS                                                |
| Dati di input   | Struttura [**di \_ \_ parametri del \_ livello \_ di protezione set di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Commenti

Questo comando viene usato per impostare High-Bandwidth Digital protezione del contenuto (HDCP) quando si esegue la riproduzione di DVD standard. A differenza del comando di [**\_ impostazione del \_ \_ livello di protezione di OPM**](opm-set-protection-level.md) , se non è possibile impostare HDCP per qualche motivo, questo comando non interrompe la riproduzione. (Le regole CSS DVD contengono un provisioning "Best Effort" per i giocatori). In caso contrario, questo comando è identico al comando **OPM \_ set \_ Protection \_ Level** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandi di OPM](opm-commands.md)
</dt> </dl>

 

 




