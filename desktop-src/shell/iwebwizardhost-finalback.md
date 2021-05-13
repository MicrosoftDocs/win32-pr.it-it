---
description: Passa alla pagina sul lato client immediatamente precedente alla pagina che ospita le pagine HTML sul lato server.
title: Metodo WebWizardHost.FinalBack (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: f131050bb5dd4cfc4b8533857c306f566f12ec2d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841872"
---
# <a name="webwizardhostfinalback-method"></a>Metodo WebWizardHost.FinalBack

Passa alla pagina sul lato client immediatamente precedente alla pagina che ospita le pagine HTML sul lato server.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

Quando la procedura guidata visualizza la prima pagina  sul lato server e l'utente fa clic sul pulsante Indietro, il server richiama **FinalBack** quando viene notificata tale evento dal gestore eventi del client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                            |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




