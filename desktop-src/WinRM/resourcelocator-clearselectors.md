---
title: Metodo ResourceLocator. ClearSelectors (WSManDisp. h)
description: Rimuove tutti i selettori da un oggetto ResourceLocator.
ms.assetid: 759880e6-5026-45de-b7e1-a4f5a16c32a0
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo ClearSelectors
- Metodo ClearSelectors Gestione remota Windows, oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, metodo ClearSelectors
topic_type:
- apiref
api_name:
- ResourceLocator.ClearSelectors
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd5dbf1322a5e0c36a1383581e2822fbd00a00e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121070"
---
# <a name="resourcelocatorclearselectors-method"></a>ResourceLocator. ClearSelectors, metodo

Rimuove tutti i [*selettori*](windows-remote-management-glossary.md) da un oggetto [**resourceLocator**](resourcelocator.md) . È possibile specificare un oggetto [**resourceLocator**](resourcelocator.md) invece di specificare un URI di risorsa nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintassi


```VB
ResourceLocator.ClearSelectors()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="remarks"></a>Commenti

**IWSManResourceLocator:: ClearSelectors** è il metodo C++ corrispondente.

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

 

 





