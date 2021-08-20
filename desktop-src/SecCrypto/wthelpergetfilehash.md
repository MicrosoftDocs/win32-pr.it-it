---
description: Verifica la firma di un file firmato e ottiene il valore hash e l'identificatore dell'algoritmo per il file.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: Funzione WTHelperGetFileHash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: a136aaf0b5c8bbf860fa27c9b439cae89a74e5149698e4841b38cdb8d9e4f6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970482"
---
# <a name="wthelpergetfilehash-function"></a>Funzione WTHelperGetFileHash

\[La **funzione WTHelperGetFileHash** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

La **funzione WTHelperGetFileHash** verifica la firma di un file firmato e ottiene il valore hash e l'identificatore dell'algoritmo per il file.

> [!Note]  
> Questa funzione non è dichiarata in un file di intestazione pubblicato. Per usare questa funzione, dichiararla nel formato esatto visualizzato. A questa funzione non è associata alcuna libreria di importazione. È necessario usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente Wintrust.dll.

 

## <a name="syntax"></a>Sintassi


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwszFilename* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione Null che contiene il percorso e il nome file del file per cui ottenere l'hash.

</dd> <dt>

*dwFlags* \[ Pollici\]
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> <dt>

*pvReserved* \[ in, out, facoltativo\]
</dt> <dd>

Questo parametro non viene usato e deve essere **NULL.**

</dd> <dt>

*pbFileHash* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer per ricevere il valore hash per il file. Il *parametro pcbFileHash* contiene le dimensioni di questo buffer.

</dd> <dt>

*pcbFileHash* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a **una variabile DWORD** che, in input, contiene le dimensioni, in byte, del buffer *pbFileHash* e, nell'output, riceve le dimensioni, in byte, del valore hash.

Per ottenere le dimensioni necessarie del valore hash, passare **NULL** per il *parametro pbFileHash.* Questa funzione inserirà le dimensioni richieste, in byte, del valore hash in questa posizione.

Se il *parametro pbFileHash* non è **NULL** e le dimensioni non sono sufficienti per ricevere il valore hash, questa funzione inserirà le dimensioni richieste, in byte, in questa posizione e restituirà **ERROR MORE \_ \_ DATA**.

</dd> <dt>

*pHashAlgid* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una [**variabile \_ ID ALG**](alg-id.md) per ricevere l'identificatore dell'algoritmo usato per creare il valore hash. Questo parametro può essere **NULL** se queste informazioni non sono necessarie.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un codice di stato che indica l'esito positivo o negativo della funzione.

I codici restituiti possibili includono, ma non solo, quanto segue.



| Codice restituito                                                                                               | Descrizione                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ RIUSCITO**</dt> </dl>             | Il file è firmato e la firma è stata verificata.<br/>                                                                                        |
| <dl> <dt>**ERRORE \_ - ALTRI \_ DATI**</dt> </dl>          | Il *parametro pbFileHash* non è **NULL** e le dimensioni specificate dal *parametro pcbFileHash* non sono sufficienti per ricevere l'hash.<br/> |
| <dl> <dt>**MEMORIA \_ INSUFFICIENTE \_ PER \_ L'ERRORE**</dt> </dl> | Si è verificato un errore di allocazione della memoria.<br/>                                                                                                      |
| <dl> <dt>**TRUST \_ E \_ BAD \_ DIGEST**</dt> </dl>      | La firma del file non è stata verificata.<br/>                                                                                                |
| <dl> <dt>**TRUST \_ E \_ NOSIGNATURE**</dt> </dl>      | Il file non è stato firmato o ha una firma non valida.<br/>                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
