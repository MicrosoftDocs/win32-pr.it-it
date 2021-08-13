---
title: Metodo AddFile IDeliveryOptimizationJob2
description: Il metodo AddFile aggiunge un singolo file a un processo DO esistente.
keywords:
- AddFile (metodo)
- Metodo AddFile, interfaccia IDeliveryOptimizationJob2
- Interfaccia IDeliveryOptimizationJob2, metodo AddFile
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6d27bca855bb9c719b485060fabf1f10b7130bd864569e74f98516ca76b8fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544636"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a>Metodo IDeliveryOptimizationJob2::AddFileWithRanges

Il metodo AddFile aggiunge un singolo file a un processo DO esistente.

## <a name="syntax"></a>Sintassi

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*fileId* \[ Pollici\]
</dt> <dd>

Stringa ID file, che identifica in modo univoco il file da scaricare.

</dd> <dt>

*remoteUrl* \[ Pollici\]
</dt> <dd>

URL del file che do tenterà di connettersi per scaricare il file.

</dd> <dt>

*rangeCount* \[ Pollici\]
</dt> <dd>

Numero di elementi contenuti negli *intervalli*. Un valore zero indica che non vengono usati intervalli per il file.

</dd> <dt>

*intervalli* \[ Pollici\]
</dt> <dd>

Elenco di intervalli facoltativo. Ogni intervallo nell'elenco è una [**BG_FILE_RANGE**](bg-file-range.md) struttura.

</dd> <dt>

*riid* \[ Pollici\]
</dt> <dd>

Tipo di oggetto contenuto nell'oggetto . Deve essere di tipo IID_IDeliveryOptimizationFile.

</dd> <dt>

*oggetto* \[ Cambio\]
</dt> <dd>

Oggetto IDeliveryOptimizationFile che rappresenta il file di download. 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce S_OK esito positivo o uno dei valori HRESULT standard in caso di errore.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|---------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato  | Windows 10, solo app desktop versione 1803 \[\]                                  |
| Server minimo supportato  | Windows Server, solo app desktop versione 1709 \[\]                              |
| Intestazione                    | Deliveryoptimization.h                                                          |
| Idl                       | DeliveryOptimization.idl                                                        |
| Libreria                   | Dosvc.lib                                                                       |
| DLL                       | Dosvc.dll                                                                       |
| IID                       | IID_IDeliveryOptimizationJob definito come EE2584CF-A69C-4848-B633-2649962B3EF7 |

## <a name="see-also"></a>Vedi anche

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
