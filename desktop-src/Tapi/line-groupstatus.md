---
description: Il messaggio LINE GROUPSTATUS viene inviato quando lo stato di un gruppo ACD cambia in un gestore dell'agente per il quale l'applicazione \_ ha attualmente una riga aperta. Questo messaggio viene generato usando la funzione lineProxyMessage.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: LINE_GROUPSTATUS messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c70ba4badd27b4d42774549b4778bd77dda13f0ae7245ee6852c2b3afab164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761944"
---
# <a name="line_groupstatus-message"></a>LINE \_ GROUPSTATUS message

Il **messaggio LINE \_ GROUPSTATUS** viene inviato quando lo stato di un gruppo ACD cambia in un gestore dell'agente per il quale l'applicazione ha attualmente una riga aperta. Questo messaggio viene generato usando la [**funzione lineProxyMessage.**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)


```C++
        
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo line. Ciò è correlato al gestore dell'agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Specifica lo stato del gruppo modificato. L'applicazione può richiamare [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) per determinare le modifiche nei gruppi disponibili. Il *parametro dwParam2* è una o più costanti [**LINEGROUPSTATUS \_**](linegroupstatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




