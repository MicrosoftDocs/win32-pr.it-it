---
description: Le costanti del flag di bit LINEBUSYMODE descrivono diversi segnali di occupato che \_ il commutatore o la rete può generare. Questi segnali di occupato indicano in genere che è attualmente in uso una risorsa diversa necessaria per effettuare una chiamata.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: LINEBUSYMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54563567944a2e5164717f7d64ff7026a0045ea735405a7bcad159969f07514a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681991"
---
# <a name="linebusymode_-constants"></a>Costanti LINEBUSYMODE \_

Le costanti del flag di bit **LINEBUSYMODE \_** descrivono diversi segnali di occupato che il commutatore o la rete può generare. Questi segnali di occupato indicano in genere che è attualmente in uso una risorsa diversa necessaria per effettuare una chiamata.

<dl> <dt>

<span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**STAZIONE \_ LINEBUSYMODE**
</dt> <dd> <dl> <dt>



Il segnale di occupato indica che la stazione della parte chiamata è occupata. Questo segnale viene in genere segnalato con un *normale tono* occupato.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**LINEBUSYMODE \_ TRUNK**
</dt> <dd> <dl> <dt>



Il segnale di occupato indica che un trunk o un circuito è occupato. Questo segnale viene in genere segnalato con un *tono di* occupato veloce.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



La modalità specifica del segnale occupato è attualmente sconosciuta, ma potrebbe diventare nota in un secondo momento.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



La modalità specifica del segnale occupato non è disponibile e non sarà nota.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I 16 bit di ordine elevato possono essere assegnati per le estensioni specifiche del dispositivo. I 16 bit di ordine basso sono riservati.

> [!Note]  
> I segnali di occupato possono essere inviati come toni in banda o come messaggi fuori banda. TAPI non presuppone il meccanismo di segnalazione specifico.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




