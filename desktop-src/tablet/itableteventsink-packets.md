---
description: Si verifica quando lo stilo si sposta sul digitalizzatore.
ms.assetid: 67d55dbc-6119-45d9-8016-a2a59f5f04ea
title: Metodo ITabletEventSink::P ackets
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
ms.openlocfilehash: 29b118771fb5217ed13c01ef9376ad9b426e1ecd74a4bf931d8412a0b47e913b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712121"
---
# <a name="itableteventsinkpackets-method"></a>Metodo ITabletEventSink::P ackets

Si verifica quando lo stilo si sposta sul digitalizzatore.

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

*tcid* \[ Pollici\]
</dt> <dd>

Identificatore della tablet.

</dd> <dt>

*cPkts* \[ Pollici\]
</dt> <dd>

Numero di pacchetti.

</dd> <dt>

*cbPkts* \[ Pollici\]
</dt> <dd>

Dimensioni del buffer di pacchetti

</dd> <dt>

*pbPkts* \[ Pollici\]
</dt> <dd>

Buffer di pacchetti.

</dd> <dt>

*pnSerialNumbers* \[ Pollici\]
</dt> <dd>

Matrice di numeri di serie.

</dd> <dt>

*Cid* 
</dt> <dd>

Identificatore dello stilo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletEventSink**](itableteventsink.md)
</dt> </dl>

 

 




