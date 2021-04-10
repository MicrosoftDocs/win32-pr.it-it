---
title: Metodo ResourceLocator. AddSelector (WSManDisp. h)
description: Aggiunge un selettore all'oggetto ResourceLocator. Il selettore specifica una particolare istanza di una risorsa.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo AddSelector
- Metodo AddSelector Gestione remota Windows, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, metodo AddSelector
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
ms.openlocfilehash: 064108f535c9f46dc074d1b37754e626dc3f1d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964268"
---
# <a name="resourcelocatoraddselector-method"></a>ResourceLocator. AddSelector, metodo

Aggiunge un [*selettore*](windows-remote-management-glossary.md) all'oggetto [**resourceLocator**](resourcelocator.md) . Il selettore specifica una particolare istanza di una *risorsa*. È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*resourceSelName* \[ in\]
</dt> <dd>

Nome del selettore. Ad esempio, quando si richiedono dati WMI, questo parametro è la proprietà chiave per una classe WMI.

</dd> <dt>

*selValue* \[ in\]
</dt> <dd>

Valore del selettore. Per i dati WMI, ad esempio, questo parametro contiene un valore per una proprietà chiave che identifica un'istanza specifica.

</dd> </dl>

## <a name="remarks"></a>Commenti

**IWSManResourceLocator:: AddSelector** è il metodo C++ corrispondente.

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





