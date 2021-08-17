---
description: Le costanti del flag di bit LINEDIALTONEMODE \_ descrivono diversi tipi di toni di selezione. Un segnale acustico speciale ha in genere un significato speciale (come per l'attesa dei messaggi).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: LINEDIALTONEMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b51ac15da6c1cba2b1b4e5b51710f04ba54549d2e08f4e9b50a20c543c305d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309961"
---
# <a name="linedialtonemode_-constants"></a>Costanti LINEDIALTONEMODE \_

Le costanti del flag di bit **LINEDIALTONEMODE \_** descrivono diversi tipi di toni di selezione. Un segnale acustico speciale ha in genere un significato speciale (come per l'attesa dei messaggi).

<dl> <dt>

<span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ EXTERNAL**
</dt> <dd> <dl> <dt>



Si tratta di un segnale di linea esterno (rete pubblica).


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ INTERNAL**
</dt> <dd> <dl> <dt>



Si tratta di un segnale acustico interno, come all'interno di un CENTRALINO.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ NORMAL**
</dt> <dd> <dl> <dt>



Si tratta di un normale tono di selezione, che in genere è un tono continuo.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ SPECIAL**
</dt> <dd> <dl> <dt>



Si tratta di un segnale acustico speciale che indica che una determinata condizione (nota dal commutatore o dalla rete) è attualmente attiva. I toni di selezione speciali usano in genere un tono interrotto. Come per un normale segnale di linea, questo indica che l'interruttore è pronto per ricevere il numero da comporre.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



La modalità del tono di selezione non è disponibile e non diventa nota.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



La modalità del tono di composizione non è attualmente nota, ma può diventare nota in un secondo momento.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I 16 bit di ordine elevato possono essere assegnati per le estensioni specifiche del dispositivo. I 16 bit di ordine basso sono riservati.

Le **costanti LINEDIALTONEMODE \_ vengono** usate all'interno della struttura di dati [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) per una chiamata nello stato dialtone.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




