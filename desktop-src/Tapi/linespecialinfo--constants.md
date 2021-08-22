---
description: Le costanti del flag di bit LINESPECIALINFO descrivono speciali segnali di informazioni che la rete può usare per segnalare diverse operazioni di creazione di report \_ e di osservazione della rete.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: LINESPECIALINFO_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1585146040db4392a271f5095420eee61f9873906443b58198676de806cb37f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002979"
---
# <a name="linespecialinfo_-constants"></a>Costanti LINESPECIALINFO \_

Le costanti del flag di bit **LINESPECIALINFO \_** descrivono speciali segnali di informazioni che la rete può usare per segnalare diverse operazioni di creazione di report e di osservazione della rete. Si tratta di sequenze di tono codificate speciali trasmesse all'inizio degli annunci registrati di consulenza di rete.

<dl> <dt>

<span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**LINESPECIALINFO \_ CUSTIRREG**
</dt> <dd> <dl> <dt>



Questo tono di informazioni speciali precede un numero non valido, aiS, cambio di numero Centerx e stazione non operativa, codice di accesso non composto o composto per errore o messaggio dell'operatore di intercettazione manuale (categoria irregolarità del cliente). LINESPECIALINFO CUSTIRREG viene segnalato anche quando le informazioni di fatturazione vengono rifiutate e quando l'indirizzo composto \_ viene bloccato all'interruttore.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOCIRCUIT**
</dt> <dd> <dl> <dt>



Questo tono informativo speciale precede un circuito senza circuito o un annuncio di emergenza (categoria di blocco del trunk).


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**RIORDINO LINESPECIALINFO \_**
</dt> <dd> <dl> <dt>



Questo tono informativo speciale precede un annuncio di riordino (categoria irregolarità delle apparecchiature). LINESPECIALINFO REORDER viene segnalato anche quando il telefono viene mantenuto \_ offhook troppo lungo.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO \_ UNAVAIL**
</dt> <dd> <dl> <dt>



Le specifiche relative al tono delle informazioni speciali non sono disponibili e non saranno note.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Le specifiche relative al tono delle informazioni speciali sono attualmente sconosciute, ma potrebbero diventare note in un secondo momento.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I 16 bit di ordine elevato possono essere assegnati per le estensioni specifiche del dispositivo. I 16 bit di ordine basso sono riservati.

I toni delle informazioni speciali sono definiti per i messaggi di consulenza e in genere non vengono usati a scopo di fatturazione o supervisione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




