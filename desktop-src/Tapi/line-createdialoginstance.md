---
description: Il messaggio TSPI LINE \_ CREATEDIALOGINSTANCE fa in modo che TAPI crei un'associazione tra il provider di servizi e un'istanza della \_ funzione TUISPI providerGenericDialog in esecuzione nel contesto dell'applicazione.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: Messaggio LINE_CREATEDIALOGINSTANCE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328050"
---
# <a name="line_createdialoginstance-message"></a>\_Messaggio linea CREATEDIALOGINSTANCE

Il messaggio **TSPI \_ line CREATEDIALOGINSTANCE** fa in modo che TAPI crei un'associazione tra il provider di servizi e un'istanza della funzione [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) in esecuzione nel contesto dell'applicazione che ha richiamato la funzione asincrona TSPI identificata dal parametro *DwRequestID* della struttura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) a cui punta *lpTUISPICreateDialogInstanceParams*.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProvider* 
</dt> <dd>

ProviderHandle fornito al provider di servizi come parametro per [**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).

</dd> <dt>

*lpTUISPICreateDialogInstanceParams* 
</dt> <dd>

Puntatore a una struttura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_PROVIDERENUMDEVICES TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

