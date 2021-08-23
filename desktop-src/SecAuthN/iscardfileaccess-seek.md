---
description: Il metodo Seek seleziona l'oggetto da cui verrà eseguito l'accesso (lettura/scrittura).
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: Metodo ISCardFileAccess::Seek
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5f4059eb2943411cfa5a3fb2b2ae247cd0fda7dd735cc1f1f61d516181976b6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923160"
---
# <a name="iscardfileaccessseek-method"></a>Metodo ISCardFileAccess::Seek

\[Il **metodo Seek** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo Seek** seleziona l'oggetto da cui verrà eseguito l'accesso (lettura/scrittura).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFile* \[ Pollici\]
</dt> <dd>

Handle del file aperto.

</dd> <dt>

*Cerca* \[ Pollici\]
</dt> <dd>

Posizione in cui deve iniziare la ricerca.



| Valore                                                                                                | Significato                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>SC \_ SEEK \_ \_ DALL'INIZIO</dt> </dl> | Iniziare la ricerca all'inizio.<br/>          |
| <dl> <dt>SC \_ SEEK \_ FROM \_ END </dt> </dl>      | Iniziare la ricerca dalla fine.<br/>              |
| <dl> <dt>SC \_ SEEK \_ RELATIVE</dt> </dl>        | Inizia la ricerca dalla posizione corrente.<br/> |



 

</dd> <dt>

*lOffset* \[ Pollici\]
</dt> <dd>

Numero di oggetti dati dall'oggetto di riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per leggere o scrivere da un file, chiamare [**rispettivamente Read**](iscardfileaccess-read.md) [**o Write.**](iscardfileaccess-write.md)

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess.**](iscardfileaccess.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

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
</dt> <dt>

[**Leggere**](iscardfileaccess-read.md)
</dt> <dt>

[**Scrivere**](iscardfileaccess-write.md)
</dt> </dl>

 

 
