---
description: Le costanti del flag di bit LINEDEVSTATUSFLAGS descrivono \_ una raccolta di elementi booleani di stato del dispositivo a linee.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: LINEDEVSTATUSFLAGS_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6649dc39c787be7c0b7f027637f12ff7f5d028add09b9f7d568149c6e9f76c97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682010"
---
# <a name="linedevstatusflags_-constants"></a>Costanti LINEDEVSTATUSFLAGS \_

Le costanti del flag di bit **LINEDEVSTATUSFLAGS \_** descrivono una raccolta di elementi booleani di stato del dispositivo a linee.

<dl> <dt>

<span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ CONNESSO**
</dt> <dd> <dl> <dt>



Specifica se la linea è connessa a TAPI. Se **TRUE,** la linea è connessa e TAPI è in grado di operare sul dispositivo di linea. Se **FALSE,** la linea viene disconnessa e l'applicazione non è in grado di controllare il dispositivo di linea tramite TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS \_ INSERVICE**
</dt> <dd> <dl> <dt>



Indica se la riga è in servizio. Se **TRUE,** la riga è in servizio. se **FALSE,** la riga non è in servizio.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS \_ BLOCCATO**
</dt> <dd> <dl> <dt>



Indica se la riga è bloccata o sbloccata. Questo bit viene usato più spesso con i dispositivi line associati ai telefoni cellulari. Molti telefoni cellulari hanno un meccanismo di sicurezza che richiede l'immissione di una password per consentire al telefono di effettuare chiamate. Questo bit può essere usato per indicare alle applicazioni che il telefono è bloccato e non può effettuare chiamate finché la password non viene immessa nell'interfaccia utente del telefono in modo che l'applicazione possa presentare un avviso appropriato all'utente.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS \_ MSGWAIT**
</dt> <dd> <dl> <dt>



Indica se la riga contiene un messaggio in attesa. Se **TRUE,** un messaggio è in attesa. se **FALSE**, nessun messaggio è in attesa.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

Le costanti LINEDEVSTATUSFLAGS vengono usate all'interno del membro \_ **dwDevStatusFlags** della struttura di dati [**LINEDEVSTATUS.**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




