---
description: Fornisce lo stato di avanzamento e altre notifiche durante un trasferimento.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: Metodo IWiaTransferCallback::TransferCallback (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.TransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 02c24f4cb1795e233fbbbb3dc30ad1bbb3624e104d59ac72f8e310bbbd323820
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440319"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a>Metodo IWiaTransferCallback::TransferCallback

Fornisce lo stato di avanzamento e altre notifiche durante un trasferimento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT TransferCallback(
  [in] LONG              lFlags,
  [in] WiaTransferParams *pWiaTransferParams
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lFlags* \[ Pollici\]
</dt> <dd>

Tipo: **LONG**

Attualmente inutilizzato. Deve essere impostato su zero.

</dd> <dt>

*pWiaTransferParams* \[ Pollici\]
</dt> <dd>

Tipo: **[ **WiaTransferParams**](-wia-wiatransferparams.md)\***

Specifica un puntatore a una [**struttura WiaTransferParams.**](-wia-wiatransferparams.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Quando questo metodo viene implementato da un filtro di elaborazione delle immagini, il minidriver di acquisizione di immagini Windows (WIA) 2.0 lo chiama durante l'acquisizione dell'immagine per inviare messaggi di stato all'applicazione.

**IWiaTransferCallback::TransferCallback** di un filtro deve delegare al metodo **IWiaTransferCallback::TransferCallback** del callback dell'applicazione. In genere, il flusso di filtro filtra i dati passati e scrive i dati filtrati direttamente nel flusso fornito dall'applicazione. Quando il filtro di elaborazione delle immagini archivia i dati tra le chiamate al relativo metodo [IStream::Write,](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) deve anche modificare i valori *lPercentComplete* e *ulBytesWrittenToCurrentStream* nella struttura [**WiaTransferParams.**](-wia-wiatransferparams.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
