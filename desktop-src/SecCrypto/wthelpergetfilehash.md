---
description: Verifica la firma di un file firmato e ottiene il valore hash e l'identificatore dell'algoritmo per il file.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: WTHelperGetFileHash (funzione)
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
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967615"
---
# <a name="wthelpergetfilehash-function"></a>WTHelperGetFileHash (funzione)

\[La funzione **WTHelperGetFileHash** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]

La funzione **WTHelperGetFileHash** verifica la firma di un file firmato e ottiene il valore hash e l'identificatore dell'algoritmo per il file.

> [!Note]  
> Questa funzione non è dichiarata in un file di intestazione pubblicato. Per usare questa funzione, dichiararla nel formato esatto indicato. A questa funzione non è associata alcuna libreria di importazione. È necessario utilizzare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegare dinamicamente a Wintrust.dll.

 

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

*pwszFilename* \[ in\]
</dt> <dd>

Puntatore a una stringa Unicode con terminazione null che contiene il percorso e il nome file del file per il quale ottenere l'hash.

</dd> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> <dt>

*pvReserved* \[ in, out, facoltativo\]
</dt> <dd>

Questo parametro non viene utilizzato e deve essere **null**.

</dd> <dt>

*pbFileHash* \[ out, facoltativo\]
</dt> <dd>

Puntatore a un buffer per ricevere il valore hash per il file. Il parametro *pcbFileHash* contiene la dimensione del buffer.

</dd> <dt>

*pcbFileHash* \[ in, out, facoltativo\]
</dt> <dd>

Puntatore a una variabile **DWORD** che, in input, contiene la dimensione, in byte, del buffer *pbFileHash* e, in output, riceve la dimensione, in byte, del valore hash.

Per ottenere le dimensioni richieste del valore hash, passare **null** per il parametro *pbFileHash* . Questa funzione inserisce la dimensione richiesta, in byte, del valore hash in questa posizione.

Se il parametro *pbFileHash* non è **null** e la dimensione non è sufficiente per ricevere il valore hash, questa funzione inserisce la dimensione richiesta, in byte, in questo percorso e restituisce un errore di **\_ altri \_ dati**.

</dd> <dt>

*pHashAlgid* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una variabile [**\_ ID ALG**](alg-id.md) per ricevere l'identificatore dell'algoritmo utilizzato per creare il valore hash. Questo parametro può essere **null** se queste informazioni non sono necessarie.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un codice di stato che indica l'esito positivo o negativo della funzione.

I codici restituiti possibili includono, ma non sono limitati a, quanto segue.



| Codice restituito                                                                                               | Descrizione                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE \_ riuscito**</dt> </dl>             | Il file è firmato e la firma è stata verificata.<br/>                                                                                        |
| <dl> <dt>**ERRORE di \_ più \_ dati**</dt> </dl>          | Il parametro *pbFileHash* non è **null** e le dimensioni specificate dal parametro *pcbFileHash* non sono sufficientemente grandi per la ricezione dell'hash.<br/> |
| <dl> <dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt> </dl> | Si è verificato un errore di allocazione della memoria.<br/>                                                                                                      |
| <dl> <dt>**TRUST \_ E \_ digest non valido \_**</dt> </dl>      | La firma del file non è stata verificata.<br/>                                                                                                |
| <dl> <dt>**TRUST \_ E \_ NoSignature**</dt> </dl>      | Il file non è stato firmato o non ha una firma valida.<br/>                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
