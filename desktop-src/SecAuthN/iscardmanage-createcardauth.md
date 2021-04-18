---
description: Crea un'interfaccia ISCardAuth.
ms.assetid: a091e361-416e-45c9-8077-617b16db654c
title: 'Metodo ISCardManage:: CreateCardAuth'
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
ms.openlocfilehash: d0b81fd8211491527f39999c6873f7b047bcb32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313729"
---
# <a name="iscardmanagecreatecardauth-method"></a>Metodo ISCardManage:: CreateCardAuth

\[Il metodo **CreateCardAuth** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **CreateCardAuth** crea un'interfaccia [**ISCardAuth**](iscardauth.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateCardAuth(
  [out] ISCardAuth **ppISCardAuth
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppISCardAuth* \[ out\]
</dt> <dd>

Puntatore restituito all'interfaccia creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *ppISCardAuth* non è valido.<br/>  |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *ppISCardAuth*.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                              |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).

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

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
