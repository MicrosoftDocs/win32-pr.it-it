---
title: Metodo GetStatus di IWMDRMIndividualizationStatus (wmdrmsdk. h)
description: Il metodo GetStatus recupera informazioni dettagliate sullo stato di individualizzazione.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- Metodo GetStatus formato Windows Media
- Metodo GetStatus formato Windows Media, interfaccia IWMDRMIndividualizationStatus
- Interfaccia IWMDRMIndividualizationStatus-formato Windows Media, metodo GetStatus
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328534"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a>Metodo IWMDRMIndividualizationStatus:: GetStatus

Il metodo **GetStatus** recupera informazioni dettagliate sullo stato di individualizzazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStatus* \[ out\]
</dt> <dd>

Riceve una struttura di [**\_ \_ stato**](drmwm-individualize-status.md) del sistema di personalizzazione WM che contiene informazioni dettagliate sullo stato del tentativo di individualizzazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





