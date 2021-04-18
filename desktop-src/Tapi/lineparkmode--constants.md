---
description: Le \_ costanti del flag di bit LINEPARKMODE descrivono modi diversi di chiamate di parcheggio.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: Costanti LINEPARKMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331254"
---
# <a name="lineparkmode_-constants"></a>\_Costanti LINEPARKMODE

Le costanti del flag di bit **LINEPARKMODE \_** descrivono modi diversi di chiamate di parcheggio.

<dl> <dt>

<span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ diretto**
</dt> <dd> <dl> <dt>



Specifica il Call Park diretto. L'indirizzo in cui deve essere parcheggiata la chiamata deve essere fornito all'opzione.


</dt> </dl> </dd> <dt>

<span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE non \_ indirizzato**
</dt> <dd> <dl> <dt>



Specifica il Call Park non indirizzato. L'indirizzo in cui viene parcheggiata la chiamata viene selezionato dall'opzione e fornito dal passaggio all'applicazione.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Le **\_ costanti LINEPARKMODE** vengono usate per il parcheggio di una chiamata. Consultare le funzionalità del dispositivo address di una linea per individuare la modalità del parco disponibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




