---
title: Metodo Session. Delete (WSManDisp. h)
description: Elimina la risorsa specificata nell'URI della risorsa.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Elimina Gestione remota Windows del metodo
- Elimina Gestione remota Windows metodo, oggetto sessione
- Gestione remota Windows oggetto sessione, metodo Delete
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf4b46997a7e3cf50dbf50c2828de78a814a513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963951"
---
# <a name="sessiondelete-method"></a>Metodo Session. Delete

Elimina la risorsa specificata nell'URI della risorsa.

## <a name="syntax"></a>Sintassi


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*resourceUri* \[ in\]
</dt> <dd>

URI della risorsa da eliminare. È anche possibile usare un oggetto [**resourceLocator**](resourcelocator.md) per specificare la risorsa.

</dd> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Riservato per utilizzi futuri. Deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, viene usata la sintassi seguente.


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente vengono eliminati i listener configurati per il trasporto HTTP.


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

 





