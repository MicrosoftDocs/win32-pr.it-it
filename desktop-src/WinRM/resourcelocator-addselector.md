---
title: Metodo ResourceLocator.AddSelector (WSManDisp.h)
description: Aggiunge un selettore all'oggetto ResourceLocator. Il selettore specifica una particolare istanza di una risorsa.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- Metodo AddSelector Windows gestione remota
- Metodo AddSelector Windows, oggetto ResourceLocator
- Oggetto ResourceLocator Windows gestione remota , metodo AddSelector
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fc59aab6e5194716fa3b0cda98bb874d0045011c0159c5caaa3cbd53e7fbfd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121641"
---
# <a name="resourcelocatoraddselector-method"></a>Metodo ResourceLocator.AddSelector

Aggiunge un [*selettore*](windows-remote-management-glossary.md) [**all'oggetto ResourceLocator.**](resourcelocator.md) Il selettore specifica una particolare istanza di una *risorsa*. È possibile fornire un [**oggetto ResourceLocator**](resourcelocator.md) anziché specificare un URI di risorsa nelle operazioni dell'oggetto [**Session,**](session.md) ad esempio [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md)

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*resourceSelName* \[ Pollici\]
</dt> <dd>

Nome del selettore. Ad esempio, quando si richiedono dati WMI, questo parametro è la proprietà chiave per una classe WMI.

</dd> <dt>

*selValue* \[ Pollici\]
</dt> <dd>

Valore del selettore. Ad esempio, per i dati WMI, questo parametro contiene un valore per una proprietà chiave che identifica un'istanza specifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

**IWSManResourceLocator::AddSelector** è il metodo C++ corrispondente.

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





