---
description: Le \_ costanti del flag di bit LINECALLHUBTRACKING descrivono il tipo di rilevamento dell'hub di chiamata fornito.
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: Costanti LINECALLHUBTRACKING_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327882"
---
# <a name="linecallhubtracking_-constants"></a>\_Costanti LINECALLHUBTRACKING

Le costanti del flag di bit **LINECALLHUBTRACKING \_** descrivono il tipo di rilevamento dell'hub di chiamata fornito.

<dl> <dt>

<span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**\_ALLCALLS LINECALLHUBTRACKING**
</dt> <dd> <dl> <dt>



Il rilevamento dell'hub chiamate viene fornito a livello di chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING \_ None**
</dt> <dd> <dl> <dt>



Nessun rilevamento dell'hub di chiamata specificato.


</dt> </dl> </dd> <dt>

<span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**\_PROVIDERLEVEL LINECALLHUBTRACKING**
</dt> <dd> <dl> <dt>



Gli hub di chiamata vengono rilevati a livello del provider di servizi. Le modifiche della chiamata da una chiamata non vengono segnalate.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Quando si verificano modifiche in questa struttura di dati, all'applicazione viene inviato un messaggio di [**riga \_ CALLINFO**](line-callinfo.md) . I parametri di questo messaggio sono un handle per la chiamata e un'indicazione dell'elemento informazioni che è stato modificato. La struttura dei dati [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) indica il tipo di rilevamento fornito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEA \_ CALLINFO**](line-callinfo.md)
</dt> <dt>

[**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




