---
title: Metodo INapComponentInfo GetLocalizedString (NapCommon. h)
description: Viene utilizzato dal sistema NAP per ottenere le stringhe localizzate.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- NAP metodo GetLocalizedString
- Metodo GetLocalizedString NAP, interfaccia INapComponentInfo
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
ms.openlocfilehash: 781e4e8c93f58039c72a98f40a529243e5722d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964984"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a>Metodo INapComponentInfo:: GetLocalizedString

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapComponentInfo:: GetLocalizedString** viene utilizzato dal sistema NAP per ottenere le stringhe localizzate.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*msgid* \[ in\]
</dt> <dd>

[**MessageID**](nap-datatypes.md) che contiene l'ID risorsa della stringa da localizzare.

</dd> <dt>

*stringa* \[ di out\]
</dt> <dd>

Puntatore a un puntatore a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) che contiene la versione localizzata del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno di questi codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Le stringhe devono essere localizzate in base all'ID lingua del thread chiamante.

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

 

 





