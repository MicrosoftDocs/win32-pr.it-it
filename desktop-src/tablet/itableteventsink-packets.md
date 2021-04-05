---
description: Si verifica quando lo stilo viene spostato sul digitalizzatore.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: ITabletEventSink::P metodo ackets
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.Packets
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fb671b0556cf121e28ae81c5dcfa804208e00006
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967929"
---
# <a name="itableteventsinkpackets-method"></a>ITabletEventSink::P metodo ackets

Si verifica quando lo stilo viene spostato sul digitalizzatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Packets(
  [in] TABLET_CONTEXT_ID tcid,
  [in] ULONG             cPkts,
  [in] ULONG             cbPkts,
  [in] BYTE              *pbPkts,
  [in] ULONG             *pnSerialNumbers,
       t                 cid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TCID* \[ in\]
</dt> <dd>

Identificatore del tablet.

</dd> <dt>

*cPkts* \[ in\]
</dt> <dd>

Numero di pacchetti.

</dd> <dt>

*cbPkts* \[ in\]
</dt> <dd>

Dimensioni del buffer di pacchetti

</dd> <dt>

*pbPkts* \[ in\]
</dt> <dd>

Buffer del pacchetto.

</dd> <dt>

*pnSerialNumbers* \[ in\]
</dt> <dd>

Matrice di numeri di serie.

</dd> <dt>

*CID* 
</dt> <dd>

Identificatore dello stilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




