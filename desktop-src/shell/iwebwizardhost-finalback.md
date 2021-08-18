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
ms.openlocfilehash: 0338b20023fda059a5205c9a42a7b7d669c5554d5fca878fcb8904c807ceceae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092608"
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

Quando la procedura guidata visualizza la prima pagina  sul lato server e l'utente fa clic sul pulsante Indietro, il server richiama **FinalBack** quando viene notificato tale evento dal gestore eventi del client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




