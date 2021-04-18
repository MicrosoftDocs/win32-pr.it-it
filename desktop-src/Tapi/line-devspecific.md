---
description: Il messaggio della linea TAPI \_ DEVSPECIFIC viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano su una riga, un indirizzo o una chiamata. Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.
ms.assetid: 6a58e77b-6ee2-4d2d-aca2-71b239f6a1dc
title: Messaggio di LINE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91907b10c0176258648fa165bbeb922a61a402ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330466"
---
# <a name="line_devspecific-message"></a>\_Messaggio linea DEVSPECIFIC

Il messaggio della **linea TAPI \_ DEVSPECIFIC** viene inviato per notificare all'applicazione gli eventi specifici del dispositivo che si verificano su una riga, un indirizzo o una chiamata. Il significato del messaggio e l'interpretazione dei parametri sono specifici del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per un dispositivo o una chiamata a linee. Si tratta di un dispositivo specifico.

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

Il messaggio di **riga \_ DEVSPECIFIC** viene utilizzato da un provider di servizi insieme alla funzione [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) . Il suo significato è specifico del dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




