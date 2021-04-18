---
description: Le \_ costanti del flag di bit LINEDEVSTATUSFLAGS descrivono una raccolta di elementi di stato dei dispositivi lineari booleani.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: Costanti LINEDEVSTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325017"
---
# <a name="linedevstatusflags_-constants"></a>\_Costanti LINEDEVSTATUSFLAGS

Le costanti del flag di bit **LINEDEVSTATUSFLAGS \_** descrivono una raccolta di elementi di stato dei dispositivi lineari booleani.

<dl> <dt>

<span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ connesso**
</dt> <dd> <dl> <dt>



Specifica se la linea è connessa a TAPI. Se **true**, la linea è connessa e TAPI è in grado di operare sul dispositivo a linee. Se **false**, la riga è disconnessa e l'applicazione non è in grado di controllare il dispositivo della linea tramite TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS \_ INservice**
</dt> <dd> <dl> <dt>



Indica se la riga è nel servizio. Se **true**, la riga è in servizio; Se **false**, la riga è fuori servizio.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS \_ bloccato**
</dt> <dd> <dl> <dt>



Indica se la riga è bloccata o sbloccata. Questo bit viene spesso usato con i dispositivi lineari associati ai telefoni cellulari. Molti telefoni cellulari hanno un meccanismo di sicurezza che richiede l'immissione di una password per consentire al telefono di inserire le chiamate. Questo bit può essere utilizzato per indicare alle applicazioni che il telefono è bloccato e non è in grado di effettuare chiamate finché la password non viene immessa nell'interfaccia utente del telefono, in modo che l'applicazione possa presentare un avviso appropriato all'utente.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**\_MSGWAIT LINEDEVSTATUSFLAGS**
</dt> <dd> <dl> <dt>



Indica se la riga presenta un messaggio in attesa. Se **true**, un messaggio è in attesa; Se **false**, nessun messaggio è in attesa.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Le \_ costanti LINEDEVSTATUSFLAGS vengono utilizzate all'interno del membro **dwDevStatusFlags** della struttura di dati [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




