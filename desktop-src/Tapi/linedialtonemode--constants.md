---
description: Le \_ costanti del flag di bit LINEDIALTONEMODE descrivono tipi diversi di toni di composizione. Un tono di connessione speciale in genere porta un significato speciale (come per i messaggi in attesa).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: Costanti LINEDIALTONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325018"
---
# <a name="linedialtonemode_-constants"></a>\_Costanti LINEDIALTONEMODE

Le costanti del flag di bit **LINEDIALTONEMODE \_** descrivono tipi diversi di toni di composizione. Un tono di connessione speciale in genere porta un significato speciale (come per i messaggi in attesa).

<dl> <dt>

<span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ esterno**
</dt> <dd> <dl> <dt>



Si tratta di un segnale di connessione esterno (rete pubblica).


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ interno**
</dt> <dd> <dl> <dt>



Si tratta di un tono di connessione interna, come all'interno di un PBX.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ normale**
</dt> <dd> <dl> <dt>



Si tratta di un tono di linea normale, che in genere è un tono continuo.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ speciale**
</dt> <dd> <dl> <dt>



Si tratta di un tono di connessione speciale che indica che è attualmente attiva una determinata condizione, nota con l'opzione o la rete. I toni della linea speciale usano in genere un tono interrotto. Come con un tono di linea normale, indica che l'opzione è pronta a ricevere il numero da comporre.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE non \_ disponibile**
</dt> <dd> <dl> <dt>



La modalità del tono di connessione non è disponibile e non viene riconosciuta.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ sconosciuto**
</dt> <dd> <dl> <dt>



La modalità del tono di connessione non è attualmente nota ma potrebbe essere nota in seguito.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo. I 16 bit di ordine inferiore sono riservati.

Le **\_ costanti LINEDIALTONEMODE** vengono usate all'interno della struttura di dati [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) per una chiamata nello stato Dialtone.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




