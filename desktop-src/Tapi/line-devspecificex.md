---
description: Il messaggio TAPI LINE DEVSPECIFICEX viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano in una riga, un indirizzo \_ o una chiamata. Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: LINE_DEVSPECIFICEX messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b65b322b265b6bbd9717a9fc5b3c0eccf46bb3802fef7684a58d2d69645cdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867071"
---
# <a name="line_devspecificex-message"></a>LINE \_ DEVSPECIFICEX message

Il messaggio TAPI **LINE \_ DEVSPECIFICEX** viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano in una riga, un indirizzo o una chiamata. Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per un dispositivo di linea o una chiamata. Questo parametro è specifico del dispositivo.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Specifico del dispositivo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Specifico del dispositivo.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Specifico del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il **messaggio LINE \_ DEVSPECIFICEX** viene usato da un provider di servizi insieme alla [**funzione lineDevSpecific.**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) Il significato è specifico del dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




