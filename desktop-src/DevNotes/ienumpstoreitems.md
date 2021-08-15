---
description: Fornisce i metodi di enumerazione standard COM per l'interfaccia IPStore.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: Interfaccia IEnumPStoreItems (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f5952dbaff2560ae4c2fc59af73246c2cd5c1d050bb53bc3c7b9091c8a39822f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542241"
---
# <a name="ienumpstoreitems-interface"></a>Interfaccia IEnumPStoreItems

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Fornisce i metodi di enumerazione standard COM per [**l'interfaccia IPStore.**](ipstore.md)

## <a name="members"></a>Membri

**L'interfaccia IEnumPStoreItems** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumPStoreItems** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IEnumPStoreItems** include questi metodi.



| Metodo                                  | Descrizione                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumpstoreitems-clone.md) | Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.<br/> |
| [**Avanti**](ienumpstoreitems-next.md)   | Ottiene il successivo elemento di dati specificato nella sequenza di enumerazione.<br/>                          |
| [**Reset**](ienumpstoreitems-reset.md) | Reimposta all'inizio della sequenza di enumerazione.<br/>                                    |
| [**Ignora**](ienumpstoreitems-skip.md)   | Ignora l'elemento di dati specificato nella sequenza di enumerazione.<br/>                              |



 

## <a name="remarks"></a>Commenti

È necessario liberare ogni elemento dopo l'enumerazione. L'oggetto enumeratore deve essere rilasciato anche quando non viene più utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
