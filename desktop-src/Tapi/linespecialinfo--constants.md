---
description: Le \_ costanti dei flag di bit di LINESPECIALINFO descrivono i segnali di informazioni speciali che la rete può usare per segnalare varie operazioni di Reporting e di osservazione della rete.
ms.assetid: b94f8a6f-b84d-4976-b4d4-10dee5a1a4d8
title: Costanti LINESPECIALINFO_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78154757515ebd5bfa36778795c26ef9fdc96db1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326882"
---
# <a name="linespecialinfo_-constants"></a>\_Costanti LINESPECIALINFO

Le costanti dei flag di bit di **LINESPECIALINFO \_** descrivono i segnali di informazioni speciali che la rete può usare per segnalare varie operazioni di Reporting e di osservazione della rete. Si tratta di sequenze di tono codificate speciali trasmesse all'inizio degli annunci registrati di Network Advisor.

<dl> <dt>

<span id="LINESPECIALINFO_CUSTIRREG"></span><span id="linespecialinfo_custirreg"></span>**\_CUSTIRREG LINESPECIALINFO**
</dt> <dd> <dl> <dt>



Questo tono speciale di informazioni precede un numero vacante, un AIS, una modifica del numero di Centrex e una stazione non lavorativa, codice di accesso non composto o con connessione in errore o messaggio dell'operatore di intercettazione manuale (categoria di irregolarità del cliente). LINESPECIALINFO \_ CUSTIRREG viene segnalato anche quando le informazioni di fatturazione vengono rifiutate e quando l'indirizzo composto viene bloccato al commutino.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_NOCIRCUIT"></span><span id="linespecialinfo_nocircuit"></span>**LINESPECIALINFO \_ NOcircuit**
</dt> <dd> <dl> <dt>



Questo tono speciale di informazioni precede un circuito no o un annuncio di emergenza (categoria blocco trunk).


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_REORDER"></span><span id="linespecialinfo_reorder"></span>**LINESPECIALINFO \_ Riordina**
</dt> <dd> <dl> <dt>



Questo tono speciale di informazioni precede un annuncio di riordino (categoria di irregolarità delle apparecchiature). \_Il riordino LINESPECIALINFO viene inoltre segnalato quando il telefono viene mantenuto troppo a lungo.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNAVAIL"></span><span id="linespecialinfo_unavail"></span>**LINESPECIALINFO non \_ disponibile**
</dt> <dd> <dl> <dt>



Le specifiche relative al tono speciale per le informazioni non sono disponibili e non diventeranno note.


</dt> </dl> </dd> <dt>

<span id="LINESPECIALINFO_UNKNOWN"></span><span id="linespecialinfo_unknown"></span>**LINESPECIALINFO \_ sconosciuto**
</dt> <dd> <dl> <dt>



Le specifiche relative al tono di informazione speciale sono attualmente sconosciute, ma possono essere note in seguito.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo. I 16 bit di ordine inferiore sono riservati.

Per i messaggi consultivi vengono definite note speciali e non vengono in genere utilizzate per scopi di fatturazione o di supervisione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




