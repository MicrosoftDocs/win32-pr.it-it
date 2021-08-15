---
description: Imposta lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale.
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: Metodo IVmApplicationHealthMonitor::SetApplicationState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 785b5e6254bde84497f4fcf72d15b20ff16ccd7319ecc3631c0864b3e4992655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392356"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a>Metodo IVmApplicationHealthMonitor::SetApplicationState

Imposta lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Rappresentazione **BSTR** del **GUID che** identifica l'applicazione. È responsabilità dell'applicazione chiamante creare e gestire gli identificatori utilizzati per le applicazioni monitorate.

</dd> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Nome visualizzato dell'applicazione. Questo nome viene usato in una voce del registro eventi informativo per la modifica dello stato.

</dd> <dt>

*Stato* \[ Pollici\]
</dt> <dd>

Valore [**dell'enumerazione APPLICATION \_ STATE**](application-state.md) che specifica il nuovo stato di integrità dell'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Lo stato delle applicazioni in esecuzione nella macchina virtuale si riflette nel valore della proprietà **OperationalStatus** \[ 1 \] della classe [**Msvm \_ HeartbeatComponent.**](msvm-heartbeatcomponent.md)

Per usare questo elemento di programmazione, Windows 8 componenti di integrazione devono essere installati nella macchina virtuale in cui è in esecuzione l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                                |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                      |
| Versione<br/>                  | Componenti di integrazione per Windows 8<br/>                                                           |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




