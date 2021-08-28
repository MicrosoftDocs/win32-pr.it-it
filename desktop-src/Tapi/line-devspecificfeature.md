---
description: Il messaggio TAPI LINE DEVSPECIFICFEATURE viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano in una riga, un indirizzo \_ o una chiamata. Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: LINE_DEVSPECIFICFEATURE messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c1ec56a41d6e57c6e090c9af682cb91c8ffdb891e376fcd9760ff1b51c5d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012531"
---
# <a name="line_devspecificfeature-message"></a>MESSAGGIO \_ LINE DEVSPECIFICFEATURE

Il messaggio TAPI **LINE \_ DEVSPECIFICFEATURE** viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano in una riga, un indirizzo o una chiamata. Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per un dispositivo di linea o una chiamata. Si tratta di un dispositivo specifico.

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

Il **messaggio LINE \_ DEVSPECIFICFEATURE** viene usato da un provider di servizi insieme alla [**funzione lineDevSpecificFeature.**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) Il significato è specifico del dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




