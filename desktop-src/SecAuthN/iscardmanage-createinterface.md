---
description: Crea l'interfaccia specificata.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: 'Metodo ISCardManage:: CreateInterface'
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
ms.openlocfilehash: 99a3f7c1acd4266395917b47c81f044d5385b3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232834"
---
# <a name="iscardmanagecreateinterface-method"></a>Metodo ISCardManage:: CreateInterface

\[Il metodo **CreateInterface** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **CreateInterface** crea l'interfaccia specificata.

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

*pguidInterface* \[ in\]
</dt> <dd>

Valore GUID dell'interfaccia da creare.

</dd> <dt>

*bstrName* \[ in\]
</dt> <dd>

Nome dell'interfaccia da creare se il GUID non è disponibile. I valori standard sono "CryptoProvider".

</dd> <dt>

*pUserData* \[ in\]
</dt> <dd>

Puntatore a dati specifici dell'utente da utilizzare nella creazione di un'interfaccia.

</dd> <dt>

*ppInterface* \[ out\]
</dt> <dd>

Puntatore all'interfaccia restituita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

I possibili valori restituiti sono i seguenti:



| Codice restituito                                                                                   | Descrizione                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno dei parametri specificati non è valido.<br/>                                         |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un puntatore errato è stato passato nel parametro *pguidInterface* o *pUserData* .<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                                                                        |



 

## <a name="remarks"></a>Commenti

Per un elenco di tutti i metodi definiti dall'interfaccia [**ISCardManage**](iscardmanage.md) , vedere **ISCardManage**.

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della [*Smart Card*](../secgloss/s-gly.md) se è stata chiamata una funzione Smart Card per completare la richiesta. Per informazioni sui codici di errore della smart card, vedere [valori restituiti da Smart Card](authentication-return-values.md).

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

 

 
