---
description: Crea un'interfaccia ISCardVerify.
ms.assetid: 6338e672-83cd-46fe-8f94-f4ba6e2581ea
title: Metodo ISCardManage::CreateCHVerification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCHVerification
api_type:
- COM
api_location: ''
ms.openlocfilehash: 312fc18be42ccc7ba35a0d0a6288637bd92cd0f10a855dc95c457329c69cd7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922768"
---
# <a name="iscardmanagecreatechverification-method"></a>Metodo ISCardManage::CreateCHVerification

\[Il **metodo CreateCHVerification** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo CreateCHVerification** crea [**un'interfaccia ISCardVerify.**](iscardverify.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateCHVerification(
  [out] ISCardVerify **ppISCardVerify
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppISCardVerify* \[ Cambio\]
</dt> <dd>

Puntatore restituito [**all'interfaccia ISCardVerify**](iscardverify.md) creata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro ppISCardVerify* non è valido.<br/>  |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | È stato passato un puntatore non valido in *ppISCardVerify.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                                |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi definiti da questa interfaccia, vedere [**ISCardManage**](iscardmanage.md).

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

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> </dl>

 

 
