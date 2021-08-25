---
title: Metodo Session.Delete (WSManDisp.h)
description: Elimina la risorsa specificata nell'URI della risorsa.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Eliminare il metodo Windows gestione remota
- Metodo Delete Windows gestione remota , oggetto Session
- Oggetto sessione Windows metodo Gestione remota , Delete
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
ms.openlocfilehash: 769ef3f462fa542e9afc6859b564e1a32ed87578894df4008fb6a19ad8aadad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858671"
---
# <a name="sessiondelete-method"></a>Metodo Session.Delete

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

*resourceUri* \[ Pollici\]
</dt> <dd>

URI della risorsa da eliminare. È anche possibile usare un [**oggetto ResourceLocator**](resourcelocator.md) per specificare la risorsa.

</dd> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Riservato per utilizzi futuri. Deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La sintassi seguente viene usata per chiamare questo metodo.


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

 





