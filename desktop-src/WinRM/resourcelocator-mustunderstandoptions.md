---
title: Proprietà ResourceLocator. MustUnderstandOptions (WSManDisp. h)
description: Ottiene o imposta il valore MustUnderstandOptions per l'oggetto ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà MustUnderstandOptions
- Gestione remota Windows proprietà MustUnderstandOptions, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, proprietà MustUnderstandOptions
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2945efd1a224c333f45956a29df779efc98e944f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964803"
---
# <a name="resourcelocatormustunderstandoptions-property"></a>Proprietà ResourceLocator. MustUnderstandOptions

Ottiene o imposta il valore **MustUnderstandOptions** per l'oggetto [**resourceLocator**](resourcelocator.md) . È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a>Valore proprietà

Indica, quando **true**, che il servizio che implementa l' [protocollo WS-Management](ws-management-protocol.md) deve restituire un errore se non è in grado di elaborare l'opzione.

## <a name="remarks"></a>Commenti

**IWSManResourceLocator:: MustUnderstandOptions** è la proprietà C++ corrispondente.

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

 

 





