---
description: Crea un'interfaccia ISCardAuth.
ms.assetid: a091e361-416e-45c9-8077-617b16db654c
title: Metodo ISCardManage::CreateCardAuth
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: f6f78e938e8c739bcc2bca6c2ce7769d64d6f72ad02296aa9b2fb692d6c129a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014131"
---
# <a name="iscardmanagecreatecardauth-method"></a>Metodo ISCardManage::CreateCardAuth

\[Il **metodo CreateCardAuth** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo CreateCardAuth** crea [**un'interfaccia ISCardAuth.**](iscardauth.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateCardAuth(
  [out] ISCardAuth **ppISCardAuth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppISCardAuth* \[ Cambio\]
</dt> <dd>

Puntatore restituito all'interfaccia creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro ppISCardAuth* non è valido.<br/>  |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido in *ppISCardAuth.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                              |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage.**](iscardmanage.md)

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

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
