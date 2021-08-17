---
description: Il messaggio LINE QUEUESTATUS viene inviato quando lo stato di una coda ACD cambia in un gestore dell'agente per il quale l'applicazione \_ ha attualmente una riga aperta. Questo messaggio viene generato usando la funzione lineProxyMessage.
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: LINE_QUEUESTATUS messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336a8239e31e5c0bcc70de747cbb48a2028c85e67f44a3e45032f02b37065d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975531"
---
# <a name="line_queuestatus-message"></a>LINE \_ QUEUESTATUS message

Il **messaggio LINE \_ QUEUESTATUS** viene inviato quando lo stato di una coda ACD cambia in un gestore dell'agente per il quale l'applicazione ha attualmente una riga aperta. Questo messaggio viene generato usando la [**funzione lineProxyMessage.**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)


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

Identificatore della coda il cui stato è stato modificato.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Specifica lo stato della coda modificato. Può essere una o più costanti [**LINEQUEUESTATUS \_**](linequeuestatus--constants.md).

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

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




