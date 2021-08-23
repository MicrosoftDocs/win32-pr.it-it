---
description: Il metodo GetCurrentDir restituisce un percorso assoluto alla directory attualmente selezionata.
ms.assetid: 12196143-a98a-4772-a803-d0c9b95a66e4
title: Metodo ISCardFileAccess::GetCurrentDir
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetCurrentDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8aea75dc5ed413a2ad400be927020e44e01dcc1670fbc35e099e7829ba03286f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008039"
---
# <a name="iscardfileaccessgetcurrentdir-method"></a>Metodo ISCardFileAccess::GetCurrentDir

\[Il **metodo GetCurrentDir** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo GetCurrentDir** restituisce un percorso assoluto alla directory attualmente selezionata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentDir(
  [out] BSTR *pbstrPathSpec
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbstrPathSpec* \[ Cambio\]
</dt> <dd>

Puntatore a un oggetto BSTR che conterrà il percorso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Per modificare la directory corrente, chiamare [**ChangeDir**](iscardfileaccess-changedir.md).

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardFileAccess**](iscardfileaccess.md).

Oltre ai codici di errore COM elencati [](../secgloss/s-gly.md) in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ChangeDir**](iscardfileaccess-changedir.md)
</dt> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
