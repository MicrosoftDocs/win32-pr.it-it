---
title: Metodo IWMDRMDevice2 GetPartialSyncList
description: Il metodo GetPartialSyncList ottiene un elenco di sincronizzazione parziale.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Metodo GetPartialSyncList windows Media Device Manager
- Metodo GetPartialSyncList windows Media Device Manager, interfaccia IWMDRMDevice2
- Interfaccia IWMDRMDevice2 windows Media Device Manager, metodo GetPartialSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0bcff91d41ce77003219336431433ee511ff144dfcb8be7880526994689a929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055659"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a>Metodo IWMDRMDevice2::GetPartialSyncList

Il **metodo GetPartialSyncList** ottiene un elenco di sincronizzazione parziale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*cMinCountThreshold* \[ Pollici\]
</dt> <dd>

Soglia minima di conteggio.

</dd> <dt>

*cMinHoursThreshold* \[ Pollici\]
</dt> <dd>

Soglia minima ore.

</dd> <dt>

*dwStartingIndex* \[ Pollici\]
</dt> <dd>

Posizione iniziale per l'indicizzazione.

</dd> <dt>

*cItems* \[ Pollici\]
</dt> <dd>

Numero di elementi da indicizzare.

</dd> <dt>

*ppbSyncList* \[ Cambio\]
</dt> <dd>

Recupero dell'elenco di sincronizzazione delle licenze.

</dd> <dt>

*pcbSyncList* \[ Cambio\]
</dt> <dd>

Dimensioni dell'elenco di sincronizzazione delle licenze, in byte.

</dd> <dt>

*pdwNextStartingIndex* \[ Cambio\]
</dt> <dd>

Posizione iniziale successiva per l'indicizzazione.

</dd> <dt>

*pcItemsProcessed* \[ Cambio\]
</dt> <dd>

Numero di elementi elaborati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. Tutti i metodi di interfaccia in Windows Gestione dispositivi multimediali possono restituire una delle classi di codici di errore seguenti:

-   Codici di errore COM standard
-   Windows codici di errore convertiti in valori HRESULT
-   Windows Codici di errore di Gestione dispositivi multimediali

Per un elenco completo dei possibili codici di errore, vedere [Codici di errore](error-codes.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMDRMDevice::GetSyncList**](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[**Interfaccia IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





