---
description: Le costanti del flag di bit PHONELAMPMODE descrivono diversi modi in cui è possibile accesa una lampadina per telefoni.
ms.assetid: 4f6ed2fa-32c9-44b4-bfb5-2c1446ea84fe
title: PHONELAMPMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a39aa3437fa813b37bad74d9c42798d0151ea3ae17adee4dad90e19675e8db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118862247"
---
# <a name="phonelampmode_-constants"></a>PHONELAMPMODE_ costanti

Le **PHONELAMPMODE_** flag di bit descrivono diversi modi in cui è possibile accende la lampadina di un telefono.

<dl> <dt>

<span id="PHONELAMPMODE_DUMMY"></span><span id="phonelampmode_dummy"></span>**PHONELAMPMODE_DUMMY**
</dt> <dd> <dl> <dt>



Questo valore viene usato per descrivere la posizione di un pulsante/lampione senza lampioni corrispondenti.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_BROKENFLUTTER"></span><span id="phonelampmode_brokenflutter"></span>**PHONELAMPMODE_BROKENFLUTTER**
</dt> <dd> <dl> <dt>



Il flutter interrotto è la sovrapposizione di flash e flutter.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLASH"></span><span id="phonelampmode_flash"></span>**PHONELAMPMODE_FLASH**
</dt> <dd> <dl> <dt>



Flash indica un rallentamento dell'on-and-off.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_FLUTTER"></span><span id="phonelampmode_flutter"></span>**PHONELAMPMODE_FLUTTER**
</dt> <dd> <dl> <dt>



Flutter significa velocizzarsi e disattivare.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_OFF"></span><span id="phonelampmode_off"></span>**PHONELAMPMODE_OFF**
</dt> <dd> <dl> <dt>



La lampadina è spenta.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_STEADY"></span><span id="phonelampmode_steady"></span>**PHONELAMPMODE_STEADY**
</dt> <dd> <dl> <dt>



Stabile significa che la lampadina è continuamente accesa.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_UNKNOWN"></span><span id="phonelampmode_unknown"></span>**PHONELAMPMODE_UNKNOWN**
</dt> <dd> <dl> <dt>



La modalità lamp è attualmente sconosciuta.


</dt> </dl> </dd> <dt>

<span id="PHONELAMPMODE_WINK"></span><span id="phonelampmode_wink"></span>**PHONELAMPMODE_WINK**
</dt> <dd> <dl> <dt>



Wink indica la frequenza normale di attivazione e disattamento.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I 16 bit di ordine elevato possono essere assegnati per le estensioni specifiche del dispositivo. I 16 bit meno bassi sono riservati.

Se le cadenze di on e off esatte possono differire tra i set di telefoni di fornitori diversi, il mapping dei modelli di illuminazione lamp effettivi per la maggior parte dei telefoni sui valori elencati sopra dovrebbe essere semplice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




