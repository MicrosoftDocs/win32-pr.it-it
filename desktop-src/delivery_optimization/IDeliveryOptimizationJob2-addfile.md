---
title: Metodo IDeliveryOptimizationJob2 AddFile
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
ms.openlocfilehash: 8225db8cccb1e1d3bb364ba1dc29f30526fe36b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119351"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a>Metodo IDeliveryOptimizationJob2:: AddFileWithRanges

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

*fileId* \[ in\]
</dt> <dd>

Stringa ID file, che identifica in modo univoco il file da scaricare.

</dd> <dt>

*remoteUrl* \[ in\]
</dt> <dd>

L'URL del file che tenterà di connettersi per scaricare il file.

</dd> <dt>

*rangeCount* \[ in\]
</dt> <dd>

Numero di elementi contenuti in *intervalli*. Un valore pari a zero indica che per il file non viene utilizzato alcun intervallo.

</dd> <dt>

*intervalli* \[ in\]
</dt> <dd>

Elenco di intervalli facoltativo. Ogni intervallo nell'elenco è una struttura [**BG_FILE_RANGE**](bg-file-range.md) .

</dd> <dt>

*riid* \[ in\]
</dt> <dd>

Tipo di oggetto contenuto nell'oggetto. Deve essere di tipo IID_IDeliveryOptimizationFile.

</dd> <dt>

*oggetto* \[ di out\]
</dt> <dd>

Oggetto IDeliveryOptimizationFile, che rappresenta il file di download. 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce S_OK in esito positivo o uno dei valori HRESULT standard in errore.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|---------------------------|---------------------------------------------------------------------------------|
| Client minimo supportato  | Solo app desktop Windows 10 versione 1803 \[\]                                  |
| Server minimo supportato  | Windows Server, versione 1709 \[ solo per le app desktop\]                              |
| Intestazione                    | Deliveryoptimization. h                                                          |
| IDL                       | DeliveryOptimization. idl                                                        |
| Libreria                   | Dosvc. lib                                                                       |
| DLL                       | Dosvc.dll                                                                       |
| IID                       | IID_IDeliveryOptimizationJob viene definito come EE2584CF-A69C-4848-B633-2649962B3EF7 |

## <a name="see-also"></a>Vedi anche

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
