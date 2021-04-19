---
description: Il messaggio TSPI LINE \_ SENDMSPDATA viene inviato quando il provider di servizi di telefonia (TSP) vuole passare informazioni al provider di servizi multimediali (msp).
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: Messaggio LINE_SENDMSPDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326624"
---
# <a name="line_sendmspdata-message"></a>\_Messaggio linea SENDMSPDATA

Il messaggio TSPI **line \_ SENDMSPDATA** viene inviato quando il provider di servizi di telefonia (TSP) vuole passare informazioni al provider di servizi multimediali (msp).


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*htLine* 
</dt> <dd>

Handle TAPI per la riga.

</dd> <dt>

*htCall* 
</dt> <dd>

Handle TAPI per la chiamata.

</dd> <dt>

*dwMsg* 
</dt> <dd>

RIGA del valore \_ SENDMSPDATA.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identifica il MSP che deve ricevere il messaggio. Se è 0, il messaggio verrà inviato a tutti MSPs. Si tratta dell'handle passato alla funzione [**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) .

</dd> <dt>

*dwParam2* 
</dt> <dd>

Buffer da passare al MSP. Il buffer non è interpretato da TAPI.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Dimensione, in byte, del buffer in *dwParam2*.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per il corretto funzionamento di questo messaggio, il provider di servizi deve negoziare una versione di TAPI 3,0 o successiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sul provider di servizi multimediali (MSP)](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[**\_LINEMSPIDENTIFY TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[**\_LINECREATEMSPINSTANCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[**\_LINECLOSEMSPINSTANCE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[**\_LINERECIEVEMSPDATA TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

