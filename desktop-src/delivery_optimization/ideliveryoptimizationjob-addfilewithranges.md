---
title: Metodo IDeliveryOptimizationJob AddFileWithRanges (Deliveryoptimization. h)
description: Aggiunge un file a un processo di download e specifica gli intervalli del file che si desidera scaricare.
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
ms.openlocfilehash: cc147f5cb3f91a2fe0b8518493dba72798ce8056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302656"
---
# <a name="ideliveryoptimizationjobaddfilewithranges-method"></a>Metodo IDeliveryOptimizationJob:: AddFileWithRanges

Aggiunge un file a un processo di download e specifica gli intervalli del file che si desidera scaricare.

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

*fileId* \[ in\]
</dt> <dd>

Stringa con terminazione null che è un identificatore univoco del contenuto pubblicato. Per il contenuto non pubblicato, può trattarsi di qualsiasi stringa univoca che il chiamante può usare per identificare i file all'interno di un processo.

</dd> <dt>

*remoteUrl* \[ in\]
</dt> <dd>

Stringa con terminazione null che contiene il nome del file nel server.

</dd> <dt>

*localName* \[ in\]
</dt> <dd>

Stringa con terminazione null che contiene il nome del file nel client.

</dd> <dt>

*rangeCount* \[ in, facoltativo\]
</dt> <dd>

Numero di elementi negli *intervalli*.

</dd> <dt>

*intervalli* \[ in, facoltativo\]
</dt> <dd>

Matrice di una o più strutture di [**BG_FILE_RANGE**](/windows/desktop/api/bits2_0/ns-bits2_0-bg_file_range) che specificano gli intervalli da scaricare. Non specificare intervalli duplicati o sovrapposti.

</dd> <dt>

*Filesize* \[ in, facoltativo\]
</dt> <dd>

Dimensioni del file, in byte. Passare **DO_UNKNOWN_FILE_SIZE** se le dimensioni non sono note all'applicazione chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori restituiti seguenti e altri.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codice restituito</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong><strong>S_OK</strong></strong></dt> </dl></td>
<td>Esito positivo.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> </dl></td>
<td>Il nome del file locale è NULL o una stringa vuota. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>E_ACCESSDENIED</strong></dt> </dl></td>
<td>L'utente non dispone delle autorizzazioni necessarie per scrivere nella directory specificata nel client.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_RANGE</strong></dt> </dl></td>
<td>Uno degli intervalli non è valido. Ad esempio, InitialOffset è impostato su <strong>BG_LENGTH_TO_EOF</strong>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>DO_E_OVERLAPPING_RANGES</strong></dt> </dl></td>
<td>Non è possibile specificare intervalli duplicati o sovrapposti. <br/>
<blockquote>
[!Note]<br />
Gli intervalli sono ordinati in base all'offset del valore, non alla lunghezza. Se vengono immessi intervalli con lo stesso offset, ma in ordine inverso, viene restituito questo errore. Se, ad esempio, vengono immessi 100,5 e 100,0 in questo ordine, non sarà possibile aggiungere il file al processo.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>DO_E_INVALID_STATE</strong></dt> </dl></td>
<td>Lo stato del processo non può essere <strong>BG_JOB_STATE_CANCELLED</strong> o <strong>BG_JOB_STATE_ACKNOWLEDGED</strong>.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob viene definito come EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md)
</dt> </dl>

 

