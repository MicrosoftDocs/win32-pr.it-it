---
description: Aggiorna i pulsanti Indietro, Avanti e Fine nella cornice della procedura guidata del client.
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
ms.openlocfilehash: 36b40d0831c18a7931f3f29492dd4c7769440a76ddcec2aa33ba3e840e97950d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859124"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>Metodo WebWizardHost.SetWizardButtons

Aggiorna i **pulsanti Indietro** **,** Avanti **e** Fine nella cornice della procedura guidata del client.

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

Assicurarsi di implementare le funzioni del gestore in ogni pagina lato server per OnBack() e OnNext(), corrispondenti ai pulsanti **Indietro** e Avanti della **procedura guidata.** Le funzioni OnBack() e OnNext() rispondono a **SetWizardButtons.** Al momento appropriato, la funzione OnNext() chiama **SetWizardButtons** con *vbLastPage* = **true,** che può abilitare un **pulsante** Fine. OnNext() chiama anche [**FinalNext quando**](iwebwizardhost-finalnext.md) un utente fa clic sul **pulsante** Fine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




