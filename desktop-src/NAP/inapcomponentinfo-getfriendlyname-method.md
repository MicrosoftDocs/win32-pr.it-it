---
title: Metodo GetFriendlyName INapComponentInfo (NapCommon. h)
description: Viene utilizzato dal sistema NAP per ottenere il nome descrittivo di un client di integrità.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- Metodo GetFriendlyName NAP
- Metodo GetFriendlyName NAP, interfaccia INapComponentInfo
- INapComponentInfo Interface NAP, metodo GetFriendlyName
topic_type:
- apiref
api_name:
- INapComponentInfo.GetFriendlyName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848f8fb8365f91bceb5a44c498578f04a1776b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478916"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a>Metodo INapComponentInfo:: GetFriendlyName

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapComponentInfo:: GetFriendlyName** viene utilizzato dal sistema NAP per ottenere il nome descrittivo di un client di integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FriendlyName* \[ out\]
</dt> <dd>

Puntatore a un [**MessageID**](nap-datatypes.md) che contiene l'ID risorsa del nome descrittivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno di questi codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





