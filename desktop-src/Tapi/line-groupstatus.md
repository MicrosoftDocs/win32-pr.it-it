---
description: Il messaggio di riga \_ GROUPSTATUS viene inviato quando lo stato di un gruppo ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta. Questo messaggio viene generato tramite la funzione lineProxyMessage.
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: Messaggio di LINE_GROUPSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327406"
---
# <a name="line_groupstatus-message"></a>\_Messaggio linea GROUPSTATUS

Il messaggio di **riga \_ GROUPSTATUS** viene inviato quando lo stato di un gruppo ACD viene modificato in un gestore dell'agente per il quale l'applicazione dispone attualmente di una linea aperta. Questo messaggio viene generato tramite la funzione [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo linea. Questo si riferisce al gestore agenti.

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

Specifica lo stato del gruppo che è stato modificato. L'applicazione può richiamare [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) per determinare le modifiche nei gruppi disponibili. Il parametro *dwParam2* è una o più [**\_ costanti LINEGROUPSTATUS**](linegroupstatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




