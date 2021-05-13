---
description: Passa alla pagina della procedura guidata sul lato client che segue la pagina che ospita le pagine HTML sul lato server o termina la procedura guidata se non sono presenti altre pagine sul lato client.
title: Metodo WebWizardHost.FinalNext (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: fa59a70c04e7f78a315955aeabb9477c6f28c80d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841842"
---
# <a name="webwizardhostfinalnext-method"></a>Metodo WebWizardHost.FinalNext

Passa alla pagina della procedura guidata sul lato client che segue la pagina che ospita le pagine HTML sul lato server o termina la procedura guidata se non sono presenti altre pagine sul lato client.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

Quando la procedura guidata visualizza l'ultima pagina HTML sul  lato  server e l'utente fa clic sul pulsante Avanti o Fine, il server richiama **FinalNext** nel gestore eventi di tale pulsante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                            |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




