---
title: Metodo IDeliveryOptimizationJob AddFileWithRanges (Deliveryoptimization.h)
description: Aggiunge un file a un processo di download e specifica gli intervalli del file da scaricare.
ms.assetid: 23F0A39F-670F-4030-A3B3-4F9277FFA8AB
keywords:
- Metodo AddFileWithRanges
- Metodo AddFileWithRanges, interfaccia IDeliveryOptimizationJob
- Interfaccia IDeliveryOptimizationJob, metodo AddFileWithRanges
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob.AddFileWithRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 197aa7443123c81d1a675d321b91573823a84f15
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476129"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a>Metodo IDeliveryOptimizationJob::AddFileWithRanges

Aggiunge un file a un processo di download e specifica gli intervalli del file da scaricare.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddFileWithRanges(
  [in]           LPCWSTR       fileId,
  [in]           LPCWSTR       remoteUrl,
  [in]           LPCWSTR       localName,
  [in, optional] DWORD         rangeCount,
  [in, optional] BG_FILE_RANGE ranges[],
  [in, optional] ULONG64       fileSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fileId* \[ Pollici\]
</dt> <dd>

Stringa con terminazione Null che rappresenta un identificatore univoco del contenuto pubblicato. Per il contenuto non pubblicato, può trattarsi di qualsiasi stringa univoca che il chiamante può usare per identificare i file all'interno di un processo.

</dd> <dt>

*remoteUrl* \[ Pollici\]
</dt> <dd>

Stringa con terminazione Null che contiene il nome del file nel server.

</dd> <dt>

*localName* \[ Pollici\]
</dt> <dd>

Stringa con terminazione Null che contiene il nome del file nel client.

</dd> <dt>

*rangeCount* \[ in, facoltativo\]
</dt> <dd>

Numero di elementi in *Ranges*.

</dd> <dt>

*intervalli* \[ in, facoltativo\]
</dt> <dd>

Matrice di una o [**più BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) che specificano gli intervalli da scaricare. Non specificare intervalli duplicati o sovrapposti.

</dd> <dt>

*fileSize* \[ in, facoltativo\]
</dt> <dd>

Dimensioni del file, in byte. Passare **DO_UNKNOWN_FILE_SIZE** se le dimensioni non sono note all'applicazione chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori restituiti seguenti, nonché altri.




| Codice restituito | Descrizione | 
|-------------|-------------|
| <dl><dt><strong><strong>S_OK</strong></strong></dt></dl> | Operazione completata.<br /> | 
| <dl><dt><strong>E_INVALIDARG</strong></dt></dl> | Il nome del file locale è NULL o una stringa vuota. <br /> | 
| <dl><dt><strong>E_ACCESSDENIED</strong></dt></dl> | L'utente non dispone dell'autorizzazione per scrivere nella directory specificata nel client.<br /> | 
| <dl><dt><strong>DO_E_INVALID_RANGE</strong></dt></dl> | Uno degli intervalli non è valido. Ad esempio, InitialOffset è impostato su <strong>BG_LENGTH_TO_EOF</strong>.<br /> | 
| <dl><dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt></dl> | Non è possibile specificare intervalli duplicati o sovrapposti. <br /><blockquote>[!Note]<br />Gli intervalli vengono ordinati in base all'offset del valore, non alla lunghezza. Se vengono immessi intervalli con lo stesso offset, ma sono in ordine inverso, verrà restituito questo errore. Ad esempio, se vengono immessi 100.5 e 100.0 in questo ordine, non sarà possibile aggiungere il file al processo.</blockquote><br /> | 
| <dl><dt><strong>DO_E_INVALID_STATE</strong></dt></dl> | Lo stato del processo non può <strong>essere BG_JOB_STATE_CANCELLED</strong> o <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.<br /> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob definito come EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Processo di iDeliveryOptimization**](ideliveryoptimizationjob.md)
</dt> </dl>

 

