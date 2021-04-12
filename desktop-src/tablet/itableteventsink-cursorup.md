---
description: Si verifica quando l'utente ha generato lo stilo dalla superficie del digitalizzatore del Tablet PC.
ms.assetid: 34dc7e6b-101a-4edd-8c3c-9aafb85cf58b
title: 'Metodo ITabletEventSink:: CursorUp'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorUp
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5e163fd01933ad0fc1a11429e77b37163655f39b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233872"
---
# <a name="itableteventsinkcursorup-method"></a>Metodo ITabletEventSink:: CursorUp

Si verifica quando l'utente ha generato lo stilo dalla superficie del digitalizzatore del Tablet PC.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CursorUp(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] ULONG             nSerialNumber,
  [in] ULONG             cbPkt,
  [in] BYTE              *pbPkt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TCID* \[ in\]
</dt> <dd>

Identificatore del tablet.

</dd> <dt>

*CID* \[ in\]
</dt> <dd>

Identificatore dello stilo.

</dd> <dt>

*nSerialNumber* \[ in\]
</dt> <dd>

Numero di serie dello stilo.

</dd> <dt>

*cbPkt* \[ in\]
</dt> <dd>

Numero di byte in un pacchetto di dati Stilo.

</dd> <dt>

*pbPkt* \[ in\]
</dt> <dd>

Dati dello stilo che indicano la posizione in cui lo stilo è stato rimosso dal tablet.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

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

 

 




