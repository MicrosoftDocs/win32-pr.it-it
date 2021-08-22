---
description: Il metodo ChangeDir modifica la directory smart card corrente nella nuova directory specificata.
ms.assetid: 1eb53236-c88f-4b43-ac91-de67d4029433
title: Metodo ISCardFileAccess::ChangeDir
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.ChangeDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3d14f104fd40a10c4d17e3751b59245299e7c8f5b63508d6e73ef1140ec7e906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008059"
---
# <a name="iscardfileaccesschangedir-method"></a>Metodo ISCardFileAccess::ChangeDir

\[Il **metodo ChangeDir** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo ChangeDir** modifica la directory [*smart card*](../secgloss/s-gly.md) corrente nella nuova directory specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ChangeDir(
  [in] REFTYPE refType,
  [in] BSTR    bstrNewDir
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*refType* \[ Pollici\]
</dt> <dd>

Tipo di riferimento utilizzato in *bstrNewDir*.

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**SC \_ TYPE \_ BY \_ NAME**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**SC \_ TYPE \_ BY \_ ID**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ TYPE \_ BY \_ SHORT**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC \_ TYPE \_ BY \_ ANY**
</dt> </dl> </dd> <dt>

*bstrNewDir* \[ Pollici\]
</dt> <dd>

Nome file/directory (per *refType*) da selezionare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per ottenere un percorso assoluto della directory attualmente selezionata, chiamare [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md).

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

[**GetCurrentDir**](iscardfileaccess-getcurrentdir.md)
</dt> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
