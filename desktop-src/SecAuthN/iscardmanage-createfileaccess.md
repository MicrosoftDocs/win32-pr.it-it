---
description: Crea un'interfaccia ISCardFileAccess.
ms.assetid: 06a5948f-c7bd-49bf-9032-f40f3d0d330c
title: 'Metodo ISCardManage:: CreateFileAccess'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3eb1f544e05959cc33119091268e1c7fe6266547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317061"
---
# <a name="iscardmanagecreatefileaccess-method"></a>Metodo ISCardManage:: CreateFileAccess

\[Il metodo **CreateFileAccess** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **CreateFileAccess** crea un'interfaccia [**ISCardFileAccess**](iscardfileaccess.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateFileAccess(
  [out] ISCardFileAccess **ppISCardFileAccess
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppISCardFileAccess* \[ out\]
</dt> <dd>

Puntatore restituito all'interfaccia [**ISCardFileAccess**](iscardfileaccess.md) creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                                  |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *ppISCardFileAccess* non è valido.<br/>  |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato in *ppISCardFileAccess*.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                                    |



 

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

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
