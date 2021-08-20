---
title: Metodo INapComponentInfo GetLocalizedString (NapCommon.h)
description: Viene usato dal sistema di Protezione accesso alla rete per ottenere stringhe localizzate.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- Metodo GetLocalizedString nap
- Metodo GetLocalizedString NAP , interfaccia INapComponentInfo
- Interfaccia INapComponentInfo NAP, metodo GetLocalizedString
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be55595bf6c5af6e435d9c53c9b473a721005699da494319ba55eaa828da2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134364"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a>Metodo INapComponentInfo::GetLocalizedString

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapComponentInfo::GetLocalizedString** viene usato dal sistema di Protezione accesso alla rete per ottenere stringhe localizzate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*msgId* \[ Pollici\]
</dt> <dd>

MessageId [**che**](nap-datatypes.md) contiene l'ID risorsa della stringa da localizzare.

</dd> <dt>

*string* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a [**un oggetto CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) che contiene la versione localizzata del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno di questi codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Le stringhe devono essere localizzate in base all'ID lingua del thread chiamante.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





