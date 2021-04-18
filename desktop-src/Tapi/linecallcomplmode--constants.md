---
description: Le \_ costanti del flag di bit LINECALLCOMPLMODE descrivono i diversi modi in cui è possibile completare una chiamata.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: Costanti LINECALLCOMPLMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 373a66b6ce13b7bfba00303bea824f542bf0016a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327307"
---
# <a name="linecallcomplmode_-constants"></a>\_Costanti LINECALLCOMPLMODE

Le costanti del flag di bit **LINECALLCOMPLMODE \_** descrivono i diversi modi in cui è possibile completare una chiamata.

<dl> <dt>

<span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**\_callback LINECALLCOMPLMODE**
</dt> <dd> <dl> <dt>



Richiede alla stazione chiamata di restituire la chiamata quando torna inattiva.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**\_campo LINECALLCOMPLMODE**
</dt> <dd> <dl> <dt>



Accoda la chiamata fino a quando non è possibile completare la chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ intrusione**
</dt> <dd> <dl> <dt>



Aggiunge l'applicazione alla chiamata esistente nella stazione chiamata (Barge in).


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**\_messaggio LINECALLCOMPLMODE**
</dt> <dd> <dl> <dt>



Lascia un breve messaggio predefinito per la stazione chiamata (lasciare la chiamata a Word). Il messaggio da inviare viene specificato separatamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




