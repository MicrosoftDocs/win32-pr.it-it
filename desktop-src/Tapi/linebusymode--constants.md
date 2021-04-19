---
description: Le \_ costanti del flag di bit LINEBUSYMODE descrivono segnali di occupato diversi che possono essere generati dall'opzione o dalla rete. Questi segnali di occupato indicano in genere che un'altra risorsa necessaria per effettuare una chiamata è attualmente in uso.
ms.assetid: 4a3fa79f-7a7a-4f9b-9353-e6c5ca4fcb4e
title: Costanti LINEBUSYMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c996ad4e6142cc8312983945ae4c716ee0b35ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332900"
---
# <a name="linebusymode_-constants"></a>\_Costanti LINEBUSYMODE

Le costanti del flag di bit **LINEBUSYMODE \_** descrivono segnali di occupato diversi che possono essere generati dall'opzione o dalla rete. Questi segnali di occupato indicano in genere che un'altra risorsa necessaria per effettuare una chiamata è attualmente in uso.

<dl> <dt>

<span id="LINEBUSYMODE_STATION"></span><span id="linebusymode_station"></span>**\_stazione LINEBUSYMODE**
</dt> <dd> <dl> <dt>



Il segnale di occupato indica che la stazione dell'entità chiamata è occupata. Questa operazione viene in genere segnalata con un tono occupato *normale* .


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_TRUNK"></span><span id="linebusymode_trunk"></span>**\_trunk LINEBUSYMODE**
</dt> <dd> <dl> <dt>



Il segnale occupato indica che un tronco o un circuito è occupato. Questa operazione viene in genere segnalata con un tono di disponibilità *elevata* .


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNKNOWN"></span><span id="linebusymode_unknown"></span>**LINEBUSYMODE \_ sconosciuto**
</dt> <dd> <dl> <dt>



La modalità specifica del segnale occupato è attualmente sconosciuta, ma potrebbe essere nota in seguito.


</dt> </dl> </dd> <dt>

<span id="LINEBUSYMODE_UNAVAIL"></span><span id="linebusymode_unavail"></span>**LINEBUSYMODE non \_ disponibile**
</dt> <dd> <dl> <dt>



La modalità specifica del segnale occupato non è disponibile e non viene riconosciuta.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo. I 16 bit di ordine inferiore sono riservati.

> [!Note]  
> I segnali occupati possono essere inviati come segnali acustici o fuori banda. TAPI non presuppone il meccanismo di segnalazione specifico.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




