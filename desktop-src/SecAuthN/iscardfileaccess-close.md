---
description: Il metodo Close chiude il file specificato. Non sono consentiti altri accessi al file.
ms.assetid: fecce23e-8604-4a87-9efb-a26e2498c2f3
title: Metodo ISCardFileAccess::Close
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Close
api_type:
- COM
api_location: ''
ms.openlocfilehash: a68f779425bfe6af56a44a8b4210f5e809abddccbaab83abfb15ab2a5b147e18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923450"
---
# <a name="iscardfileaccessclose-method"></a>Metodo ISCardFileAccess::Close

\[Il **metodo Close** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo Close** chiude il file specificato. Non sono consentiti altri accessi al file.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Close(
  [in] HSCARD_FILE hFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFile* \[ Pollici\]
</dt> <dd>

Handle per il file da chiudere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per aprire un file, chiamare [**Open**](iscardfileaccess-open.md).

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
</dt> <dt>

[**Aperto**](iscardfileaccess-open.md)
</dt> </dl>

 

 
