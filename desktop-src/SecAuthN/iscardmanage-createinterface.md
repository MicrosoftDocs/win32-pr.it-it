---
description: Crea l'interfaccia specificata.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: Metodo ISCardManage::CreateInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8c9b231ec7930b78c1693e38268638e7a24b26dfa32d8f25acb5a429dbcdedc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922660"
---
# <a name="iscardmanagecreateinterface-method"></a>Metodo ISCardManage::CreateInterface

\[Il **metodo CreateInterface** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo CreateInterface** crea l'interfaccia specificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pguidInterface* \[ Pollici\]
</dt> <dd>

Valore GUID dell'interfaccia da creare.

</dd> <dt>

*bstrName* \[ Pollici\]
</dt> <dd>

Nome dell'interfaccia da creare se il GUID non è disponibile. I valori standard sono "CryptoProvider".

</dd> <dt>

*pUserData* \[ Pollici\]
</dt> <dd>

Puntatore ai dati specifici dell'utente da utilizzare nella creazione di un'interfaccia.

</dd> <dt>

*ppInterface* \[ Cambio\]
</dt> <dd>

Puntatore all'interfaccia restituita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

I possibili valori restituiti sono i seguenti:



| Codice restituito                                                                                   | Descrizione                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno dei parametri forniti non è valido.<br/>                                         |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | È stato passato un puntatore non valido nel *parametro pguidInterface* o *pUserData.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                                                                        |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi definiti [**dall'interfaccia ISCardManage,**](iscardmanage.md) vedere **ISCardManage**.

Oltre ai codici di errore COM elencati [](../secgloss/s-gly.md) in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per informazioni sui smart card di errore, vedere [Valori restituiti da smart card.](authentication-return-values.md)

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
</dt> </dl>

 

 
