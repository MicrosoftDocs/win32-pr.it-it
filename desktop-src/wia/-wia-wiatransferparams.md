---
description: "Il WiaTransferParams viene trasmesso a un'applicazione durante il trasferimento dei dati dal sistema di runtime di acquisizione immagini Windows (WIA) al metodo IWiaTransferCallback:: TransferCallback."
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Struttura WiaTransferParams (WIA. h)
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
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307286"
---
# <a name="wiatransferparams-structure"></a>Struttura WiaTransferParams

Il **WiaTransferParams** viene trasmesso a un'applicazione durante il trasferimento dei dati dal sistema di runtime di acquisizione immagini Windows (WIA) al metodo [**IWiaTransferCallback:: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .

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

Tipo: **Long**

</dd> <dd>

Indica lo stato del trasferimento dei dati.

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**\_ \_ stato messaggio di trasferimento WIA \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ fine \_ del flusso del messaggio di trasferimento WIA \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ fine \_ del trasferimento del messaggio di trasferimento WIA \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**\_stato del \_ dispositivo del messaggio di trasferimento WIA \_ \_**


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**\_ \_ \_ pagina nuovo messaggio di trasferimento WIA \_**


</dt> <dd></dd> </dl> </dd> <dt>

**lPercentComplete**
</dt> <dd>

Tipo: **Long**

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

Stato, o stato di errore, del dispositivo impostato dal driver; ad esempio, "riscaldamento".

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 




