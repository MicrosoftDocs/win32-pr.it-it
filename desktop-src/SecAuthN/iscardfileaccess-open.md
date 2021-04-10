---
description: Il metodo Open apre il file specificato per un ulteriore utilizzo.
ms.assetid: a970daba-ed04-45f0-9b2d-3883807050df
title: 'Metodo ISCardFileAccess:: Open'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Open
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1b68c004d4de308b641a1c4cb187312150f4d2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131455"
---
# <a name="iscardfileaccessopen-method"></a>Metodo ISCardFileAccess:: Open

\[Il metodo **Open** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **Open** apre il file specificato per un ulteriore utilizzo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Open(
  [in]  REFTYPE     refType,
  [in]  BSTR        bstrPathSpec,
  [out] HSCARD_FILE *phFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RefType* \[ in\]
</dt> <dd>

Tipo di riferimento usato in *bstrPathSpec*.

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**\_tipo SC \_ per \_ nome**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**\_tipo SC \_ per \_ ID**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**\_tipo SC \_ per \_ breve**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC \_ digitare \_ per \_ qualsiasi**
</dt> </dl> </dd> <dt>

*bstrPathSpec* \[ in\]
</dt> <dd>

File da aprire.

</dd> <dt>

*phFile* \[ out\]
</dt> <dd>

Puntatore a un file HSCARD che conterrà \_ l'handle di file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per chiudere un file, chiamare [**Close**](iscardfileaccess-close.md).

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Chiudi**](iscardfileaccess-close.md)
</dt> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
