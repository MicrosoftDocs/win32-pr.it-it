---
description: Il metodo seproperties imposta la primitiva a cui fa riferimento TLVs (tag, length, value) per l'oggetto specificato.
ms.assetid: f8f75c8e-14f4-4bc4-b49d-b232ede374b0
title: 'Metodo ISCardFileAccess:: seproperties'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.SetProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: b54c2193ec17bca9f9b3ba00b2c2bc133707dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310957"
---
# <a name="iscardfileaccesssetproperties-method"></a>Metodo ISCardFileAccess:: seproperties

\[Il metodo **seproperties** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **seproperties** imposta la primitiva a cui fa riferimento TLVs (tag, length, value) per l'oggetto specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProperties(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags,
  [in] LPTLV_TABLE pTable
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

File.

</dd> <dt>

*flag* \[ in\]
</dt> <dd>

Specifica se utilizzare la messaggistica protetta.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ messaggistica protetta SC \_ FL**
</dt> </dl> </dd> <dt>

*pTable* \[ in\]
</dt> <dd>

Puntatore a strutture TLV il cui valore deve essere impostato.

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

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
