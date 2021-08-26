---
description: Crea un collegamento di comunicazione a un smart card (ICC) usando un handle restituito dal gestore smart card risorse.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: Metodo ISCardManage::AttachByHandle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: c464f2d514a59754b5dc4d9d98f745a4802843c3cfafa3df16057c53456221c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014161"
---
# <a name="iscardmanageattachbyhandle-method"></a>Metodo ISCardManage::AttachByHandle

\[Il **metodo AttachByHandle** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo AttachByHandle** crea un collegamento di comunicazione a [*un smart card*](../secgloss/s-gly.md) (ICC) usando un handle restituito dall'smart card resource [*manager.*](../secgloss/r-gly.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hICC* \[ Pollici\]
</dt> <dd>

Handle per un smart card.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti:



| Codice restituito                                                                                   | Descrizione                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro hICC* non è valido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                     |



 

## <a name="remarks"></a>Commenti

Per associare un [*lettore*](../secgloss/r-gly.md) chiamare [**AttachByIFD**](iscardmanage-attachbyifd.md).

Per rilasciare un allegato, chiamare [**Detach**](iscardmanage-detach.md).

Per riconnettersi al smart card senza chiamare [**Detach**](iscardmanage-detach.md) e **AttachByHandle,** chiamare [**Reconnect**](iscardmanage-reconnect.md).

Per un elenco di tutti i metodi definiti [**dall'interfaccia ISCardManage,**](iscardmanage.md) vedere [**ISCardManage**](iscardmanage.md).

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per informazioni sui smart card di errore, vedere [Valori restituiti da smart card.](authentication-return-values.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Detach**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Riconnetti**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
