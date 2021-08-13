---
description: WiaTransferParams viene trasmesso a un'applicazione durante un trasferimento dei dati dal sistema di run-time di acquisizione di immagini Windows (WIA) al metodo IWiaTransferCallback::TransferCallback.
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Struttura WiaTransferParams (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 7d128a39ff5d9d29bf0766273adaace7eae86b10c9556284c1f5b6f1c9285d30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449907"
---
# <a name="wiatransferparams-structure"></a>Struttura WiaTransferParams

**WiaTransferParams** viene trasmesso a un'applicazione durante un trasferimento dei dati dal sistema di run-time di acquisizione di immagini di Windows (WIA) al metodo [**IWiaTransferCallback::TransferCallback.**](-wia-iwiatransfercallback-transfercallback.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a>Members

<dl> <dt>

**lMessage**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Indica lo stato del trasferimento dei dati.

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**WIA \_ TRANSFER \_ MSG \_ STATUS**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**FINE FLUSSO \_ \_ MSG TRASFERIMENTO \_ \_ WIA \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**FINE \_ TRASFERIMENTO \_ MSG \_ \_ WIA \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**WIA TRANSFER MSG DEVICE STATUS (STATO DEL \_ DISPOSITIVO WIA TRANSFER \_ \_ MSG) \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**NUOVA PAGINA WIA \_ TRANSFER \_ MSG \_ \_**


</dt> <dd></dd> </dl> </dd> <dt>

**lPercentComplete**
</dt> <dd>

Tipo: **LONG**

</dd> <dd>

Indica lo stato di avanzamento del trasferimento dei dati come percentuale.

</dd> <dt>

**ulTransferredBytes**
</dt> <dd>

Tipo: **ULONG64**

</dd> <dd>

Indica la quantità di dati trasferiti.

</dd> <dt>

**hrErrorStatus**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Stato, o stato di errore, del dispositivo impostato dal driver. ad esempio "riscaldamento".

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                   |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 




