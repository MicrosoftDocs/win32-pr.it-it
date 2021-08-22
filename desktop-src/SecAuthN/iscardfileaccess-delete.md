---
description: Il metodo Delete elimina un file in un percorso specificato all'interno dell'smart card file system.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: Metodo ISCardFileAccess::D elete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 721830ea3d446585e7f52c699642b1534c78d34826722b5737e191dfce94c817
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008049"
---
# <a name="iscardfileaccessdelete-method"></a>Metodo ISCardFileAccess::D elete

\[Il **metodo** Delete è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo Delete** elimina un file in un percorso specificato all'interno [*del*](../secgloss/s-gly.md) smart card file system.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*refType* \[ Pollici\]
</dt> <dd>

Tipo di riferimento utilizzato in *bstrPathSpec*.

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**SC \_ TYPE \_ BY \_ NAME**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**SC \_ TYPE \_ BY \_ ID**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ TYPE \_ BY \_ SHORT**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC \_ TYPE \_ BY \_ ANY**
</dt> </dl> </dd> <dt>

*bstrPathSpec* \[ Pollici\]
</dt> <dd>

Identificatore del file da eliminare.

</dd> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Specifica se è necessario usare la messaggistica sicura e preallocare i dati.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ SECURE \_ MESSAGING**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**SC \_ FL \_ PREALLOCATO**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                  | Descrizione                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | L'operazione è stata completata correttamente.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Parametro non valido.<br/>                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | L'interfaccia non ha implementato questo metodo.<br/> |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Crea**](iscardfileaccess-create.md)
</dt> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
