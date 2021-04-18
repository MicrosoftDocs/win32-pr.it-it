---
description: Fornisce lo stato di avanzamento e altre notifiche durante un trasferimento.
ms.assetid: 0faba0f8-b318-4c47-85e0-5ce128fe1c82
title: 'Metodo IWiaTransferCallback:: TransferCallback (WIA. h)'
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
ms.openlocfilehash: f1e2f939a7a3d768fc744c0603563b0a088e08f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307351"
---
# <a name="iwiatransfercallbacktransfercallback-method"></a>Metodo IWiaTransferCallback:: TransferCallback

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

*è* \[ in\]
</dt> <dd>

Tipo: **Long**

Attualmente non usato. Deve essere impostato su zero.

</dd> <dt>

*pWiaTransferParams* \[ in\]
</dt> <dd>

Tipo: **[**WiaTransferParams**](-wia-wiatransferparams.md) \** _

Specifica un puntatore a una struttura [_ *WiaTransferParams* *](-wia-wiatransferparams.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Quando questo metodo viene implementato da un filtro di elaborazione delle immagini, Windows Image Acquisition (WIA) 2,0 minidriver lo chiama durante l'acquisizione dell'immagine per inviare i messaggi di stato all'applicazione.

Un filtro **IWiaTransferCallback:: TransferCallback** deve delegare al metodo **IWiaTransferCallback:: TransferCallback** del callback dell'applicazione. In genere, il flusso di filtro filtra i dati passati e scrive i dati filtrati direttamente nel flusso fornito dall'applicazione. Quando il filtro di elaborazione delle immagini archivia i dati tra le chiamate al relativo metodo [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , deve anche modificare i valori *lPercentComplete* e *ulBytesWrittenToCurrentStream* nella struttura [**WiaTransferParams**](-wia-wiatransferparams.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
