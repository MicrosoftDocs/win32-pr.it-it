---
description: Passa alla pagina della procedura guidata lato client che segue la pagina che ospita le pagine HTML sul lato server oppure termina la procedura guidata se non sono presenti altre pagine lato client.
title: Metodo WebWizardHost. FinalNext (shldisp. h)
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
ms.openlocfilehash: 5693de342b03a9ee4b7ed04cf24d8cfa9ee8b784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232493"
---
# <a name="webwizardhostfinalnext-method"></a>WebWizardHost. FinalNext, metodo

Passa alla pagina della procedura guidata lato client che segue la pagina che ospita le pagine HTML sul lato server oppure termina la procedura guidata se non sono presenti altre pagine lato client.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

Quando la procedura guidata Visualizza l'ultima pagina HTML sul lato server e l'utente fa clic sul pulsante **Avanti** o **fine** , il server richiama **FinalNext** nel gestore eventi del pulsante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




