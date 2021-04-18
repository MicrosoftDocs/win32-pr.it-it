---
description: Il messaggio della linea TAPI \_ DEVSPECIFICEX viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano su una riga, un indirizzo o una chiamata. Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: Messaggio di LINE_DEVSPECIFICEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba25047858c641ea4c6cec7d15ba06df24e8ee39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330465"
---
# <a name="line_devspecificex-message"></a>\_Messaggio linea DEVSPECIFICEX

Il messaggio della **linea TAPI \_ DEVSPECIFICEX** viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano su una riga, un indirizzo o una chiamata. Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per un dispositivo o una chiamata a linee. Questo parametro è specifico del dispositivo.

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

Il messaggio di **riga \_ DEVSPECIFICEX** viene utilizzato da un provider di servizi insieme alla funzione [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) . Il suo significato è specifico del dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




