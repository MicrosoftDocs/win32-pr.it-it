---
description: Aggiorna i pulsanti indietro, avanti e fine nel frame della procedura guidata del client.
title: Metodo WebWizardHost. SetWizardButtons (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980250"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>WebWizardHost. SetWizardButtons, metodo

Aggiorna i pulsanti **indietro**, **Avanti** e **fine** nel frame della procedura guidata del client.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vbEnableBack* \[ in\]
</dt> <dd>

Tipo: **booleano**

Abilita il pulsante **indietro** .

</dd> <dt>

*vbEnableNext* \[ in\]
</dt> <dd>

Tipo: **booleano**

Abilita il pulsante **Avanti**.

</dd> <dt>

*vbLastPage* \[ in\]
</dt> <dd>

Tipo: **booleano**

Abilita il pulsante **fine** . Indica che si tratta dell'ultima pagina sul lato server.

</dd> </dl>

## <a name="remarks"></a>Commenti

Assicurarsi di implementare le funzioni del gestore in ogni pagina lato server per onback () e OnNext (), corrispondenti **ai pulsanti della** procedura guidata e **successivamente**. Le funzioni onback () e OnNext () rispondono a **SetWizardButtons**. Al momento opportuno, la funzione OnNext () chiama **SetWizardButtons** con *vbLastPage* = **true**, che può attivare un pulsante **fine** . OnNext () chiama anche [**FinalNext**](iwebwizardhost-finalnext.md) quando un utente fa clic sul pulsante **fine** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




