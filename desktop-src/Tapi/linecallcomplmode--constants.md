---
description: Le costanti del flag di bit LINECALLCOMPLMODE \_ descrivono diversi modi in cui è possibile completare una chiamata.
ms.assetid: 68f755a1-586b-4c5b-b8e8-c8b40eb71685
title: LINECALLCOMPLMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43f76c9b8012f9ecb60c6b0ffd787d5a0bad87794eb833cc4095c276ba983f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761755"
---
# <a name="linecallcomplmode_-constants"></a>Costanti LINECALLCOMPLMODE \_

Le costanti del flag di bit **LINECALLCOMPLMODE \_** descrivono diversi modi in cui è possibile completare una chiamata.

<dl> <dt>

<span id="LINECALLCOMPLMODE_CALLBACK"></span><span id="linecallcomplmode_callback"></span>**LINECALLCOMPLMODE \_ CALLBACK**
</dt> <dd> <dl> <dt>



Richiede alla stazione chiamata di restituire la chiamata quando torna inattiva.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_CAMPON"></span><span id="linecallcomplmode_campon"></span>**LINECALLCOMPLMODE \_ CAMPON**
</dt> <dd> <dl> <dt>



Accoda la chiamata fino al completamento della chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_INTRUDE"></span><span id="linecallcomplmode_intrude"></span>**LINECALLCOMPLMODE \_ INTRUDE**
</dt> <dd> <dl> <dt>



Aggiunge l'applicazione alla chiamata esistente alla stazione chiamata (barge in).


</dt> </dl> </dd> <dt>

<span id="LINECALLCOMPLMODE_MESSAGE"></span><span id="linecallcomplmode_message"></span>**LINECALLCOMPLMODE \_ MESSAGE**
</dt> <dd> <dl> <dt>



Lascia un breve messaggio predefinito per la stazione chiamata (Leave Word Calling). Il messaggio da inviare viene specificato separatamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




