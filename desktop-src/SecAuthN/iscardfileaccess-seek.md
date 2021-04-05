---
description: Il metodo Seek seleziona l'oggetto da cui verrà eseguito l'accesso (lettura/scrittura).
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: 'Metodo ISCardFileAccess:: Seek'
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
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756881"
---
# <a name="iscardfileaccessseek-method"></a>Metodo ISCardFileAccess:: Seek

\[Il metodo **Seek** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **Seek** seleziona l'oggetto da cui verrà eseguito l'accesso (lettura/scrittura).

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

*hFile* \[ in\]
</dt> <dd>

Handle del file aperto.

</dd> <dt>

*Cerca* \[ in\]
</dt> <dd>

Posizione in cui deve iniziare la ricerca.



| Valore                                                                                                | Significato                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>SC \_ Seek \_ dall' \_ inizio</dt> </dl> | Iniziare la ricerca all'inizio.<br/>          |
| <dl> <dt>SC \_ Seek \_ dalla \_ fine </dt> </dl>      | Inizia la ricerca dalla fine.<br/>              |
| <dl> <dt>SC \_ Seek \_ relativo</dt> </dl>        | Inizia la ricerca dalla posizione corrente.<br/> |



 

</dd> <dt>

*lOffset* \[ in\]
</dt> <dd>

Numero di oggetti dati dall'oggetto di riferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per leggere o scrivere da un file, chiamare rispettivamente [**Read**](iscardfileaccess-read.md) o [**Write**](iscardfileaccess-write.md) .

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**Lettura**](iscardfileaccess-read.md)
</dt> <dt>

[**Scrittura**](iscardfileaccess-write.md)
</dt> </dl>

 

 
