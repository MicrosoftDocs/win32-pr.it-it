---
description: Il messaggio TSPI LINE CREATEDIALOGINSTANCE fa sì che TAPI crei un'associazione tra il provider di servizi e un'istanza della funzione \_ TUISPI providerGenericDialog in esecuzione nel contesto \_ dell'applicazione.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: LINE_CREATEDIALOGINSTANCE messaggio (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e670a0dbcdde82721e5441b95983d5852e821cc981062947a0d6b76639ad762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873501"
---
# <a name="line_createdialoginstance-message"></a>MESSAGGIO LINE \_ CREATEDIALOGINSTANCE

Il messaggio TSPI **LINE \_ CREATEDIALOGINSTANCE** fa sì che TAPI crei un'associazione tra il provider di servizi e un'istanza della funzione [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) in esecuzione nel contesto dell'applicazione che ha richiamato la funzione TSPI asincrona identificata dal *parametro dwRequestID* della struttura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) a cui punta *lpTUISPICreateDialogInstanceParams*.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProvider* 
</dt> <dd>

ProviderHandle fornito al provider di servizi come parametro per [**provider \_ TSPIEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).

</dd> <dt>

*lpTUISPICreateDialogInstanceParams* 
</dt> <dd>

Puntatore a [**una struttura TUISPICREATEDIALOGINSTANCEPARAMS.**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Provider \_ TSPIEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

