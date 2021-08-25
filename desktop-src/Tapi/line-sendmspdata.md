---
description: Il messaggio TSPI LINE SENDMSPDATA viene inviato quando il provider di servizi di telefonia (TSP) desidera passare informazioni al provider di servizi multimediali \_ (MSP).
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: LINE_SENDMSPDATA messaggio (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90a4f9086bb734f73a9a28817009c11d261442cf4253791b51e48e89d511b2ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126211"
---
# <a name="line_sendmspdata-message"></a>LINE \_ SENDMSPDATA message

Il messaggio TSPI **LINE \_ SENDMSPDATA** viene inviato quando il provider di servizi di telefonia (TSP) desidera passare informazioni al provider di servizi multimediali (MSP).


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

Valore LINE \_ SENDMSPDATA.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identifica il msp che deve ricevere il messaggio. Se 0, il messaggio verrà inviato a tutti i msp. Si tratta dell'handle passato alla [**funzione \_ LineCreateMSPInstance TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)

</dd> <dt>

*dwParam2* 
</dt> <dd>

Buffer da passare al msp. Il buffer non viene interpretato da TAPI.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Dimensione, in byte, del buffer in *dwParam2*.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il provider di servizi deve negoziare un TAPI versione 3.0 o successiva per il funzionamento del messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni sul provider di Servizi multimediali (MSP)](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[**Riga \_ TSPIMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[**Riga \_ TSPICreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[**Riga \_ TSPICloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[**TSPI \_ lineRecieveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

