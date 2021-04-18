---
title: Metodo IWMDRMDevice2 GetPartialSyncList
description: Il metodo GetPartialSyncList ottiene un elenco di sincronizzazione parziale.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Metodo GetPartialSyncList Windows Media Gestione dispositivi
- Metodo GetPartialSyncList Windows Media Gestione dispositivi, interfaccia IWMDRMDevice2
- Interfaccia IWMDRMDevice2 Windows Media Gestione dispositivi, metodo GetPartialSyncList
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
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332153"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a>Metodo IWMDRMDevice2:: GetPartialSyncList

Il metodo **GetPartialSyncList** ottiene un elenco di sincronizzazione parziale.

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

*cMinCountThreshold* \[ in\]
</dt> <dd>

Soglia numero minimo.

</dd> <dt>

*cMinHoursThreshold* \[ in\]
</dt> <dd>

Soglia ore minime.

</dd> <dt>

*dwStartingIndex* \[ in\]
</dt> <dd>

Posizione iniziale per l'indicizzazione.

</dd> <dt>

*cItems* \[ in\]
</dt> <dd>

Numero di elementi da indicizzare.

</dd> <dt>

*ppbSyncList* \[ out\]
</dt> <dd>

Elenco di sincronizzazione delle licenze recuperato.

</dd> <dt>

*pcbSyncList* \[ out\]
</dt> <dd>

Dimensioni in byte dell'elenco di sincronizzazione delle licenze.

</dd> <dt>

*pdwNextStartingIndex* \[ out\]
</dt> <dd>

Posizione iniziale successiva per l'indicizzazione.

</dd> <dt>

*pcItemsProcessed* \[ out\]
</dt> <dd>

Numero di elementi in fase di elaborazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. Tutti i metodi di interfaccia in Windows Media Gestione dispositivi possono restituire una delle classi di codici di errore seguenti:

-   Codici di errore COM standard
-   Codici di errore di Windows convertiti in valori HRESULT
-   Codici di errore di Windows Media Gestione dispositivi

Per un elenco completo dei codici di errore possibili, vedere [codici di errore](error-codes.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IWMDRMDevice:: getsyncs**](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[**Interfaccia IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





