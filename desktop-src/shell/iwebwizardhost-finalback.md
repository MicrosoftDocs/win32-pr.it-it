---
description: Passa alla pagina lato client immediatamente precedente alla pagina che ospita le pagine HTML sul lato server.
title: Metodo WebWizardHost. FinalBack (shldisp. h)
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
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882485"
---
# <a name="webwizardhostfinalback-method"></a>WebWizardHost. FinalBack, metodo

Passa alla pagina lato client immediatamente precedente alla pagina che ospita le pagine HTML sul lato server.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

Quando la procedura guidata Visualizza la prima pagina sul lato server e l'utente fa clic sul pulsante **indietro** , il server richiama **FinalBack** quando riceve una notifica dell'evento da parte del gestore eventi del client.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




