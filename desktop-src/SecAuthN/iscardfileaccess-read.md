---
description: Il metodo Read legge e restituisce i dati specificati da un determinato file.
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: Metodo ISCardFileAccess::Read
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: c44839b9916bdee999eb1fb54d689dd51761c35d71bc3ba828171dda62e05c42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923200"
---
# <a name="iscardfileaccessread-method"></a>Metodo ISCardFileAccess::Read

\[Il **metodo** Read è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo Read** legge e restituisce i dati specificati da un determinato file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFile* \[ Pollici\]
</dt> <dd>

Handle del file aperto a cui accedere.

</dd> <dt>

*lBytesToRead* \[ Pollici\]
</dt> <dd>

Lunghezza dei dati da leggere (in) o numero di byte letti (in uscita). Restituisce un elenco di file come matrice di BSTR.

</dd> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Specifica se deve essere utilizzata la messaggistica protetta.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ SECURE \_ MESSAGING**
</dt> </dl> </dd> <dt>

*ppBuffer* \[ Cambio\]
</dt> <dd>

Oggetto [**IByteBuffer**](ibytebuffer.md) contenente i dati letti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess.**](iscardfileaccess.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore [*smart card*](../secgloss/s-gly.md) se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
