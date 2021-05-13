---
description: Aggiorna i pulsanti Indietro, Avanti e Fine nel frame della procedura guidata del client.
title: Metodo WebWizardHost.SetWizardButtons (Shldisp.h)
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
ms.openlocfilehash: a1b2a79c7ea323c36371e08d3519e71e4c537935
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842622"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>Metodo WebWizardHost.SetWizardButtons

Aggiorna i **pulsanti Indietro** **,** Avanti **e** Fine nel frame della procedura guidata del client.

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

*vbEnableBack* \[ Pollici\]
</dt> <dd>

Tipo: **Boolean**

Abilita il **pulsante** Indietro.

</dd> <dt>

*vbEnableNext* \[ Pollici\]
</dt> <dd>

Tipo: **Boolean**

Abilita il pulsante **Avanti**.

</dd> <dt>

*vbLastPage* \[ Pollici\]
</dt> <dd>

Tipo: **Boolean**

Abilita il **pulsante** Fine. Indica che si tratta dell'ultima pagina sul lato server.

</dd> </dl>

## <a name="remarks"></a>Commenti

Assicurarsi di implementare le funzioni del gestore in ogni pagina lato server per OnBack() e OnNext(), corrispondenti ai pulsanti **Indietro** e Avanti della **procedura guidata.** Le funzioni OnBack() e OnNext() rispondono a **SetWizardButtons**. Al momento appropriato, la funzione OnNext() chiama **SetWizardButtons** con *vbLastPage* true , che = può abilitare un **pulsante** Fine. OnNext() chiama anche [**FinalNext quando**](iwebwizardhost-finalnext.md) un utente fa clic sul **pulsante** Fine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                            |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




