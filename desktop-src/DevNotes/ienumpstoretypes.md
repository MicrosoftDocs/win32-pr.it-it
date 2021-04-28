---
description: "Interfaccia IEnumPStoreTypes: fornisce metodi di enumerazione standard COM per l'interfaccia IPStore."
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Interfaccia IEnumPStoreTypes (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7ca2e250864889a5fda465e146287bf59a2b6346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089359"
---
# <a name="ienumpstoretypes-interface"></a>Interfaccia IEnumPStoreTypes

\[L'archiviazione protetta (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Fornisce metodi di enumerazione standard COM per [**l'interfaccia IPStore.**](ipstore.md)

## <a name="members"></a>Membri

**L'interfaccia IEnumPStoreTypes** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumPStoreTypes** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IEnumPStoreTypes** include questi metodi.



| Metodo                                  | Descrizione                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumpstoretypes-clone.md) | Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.<br/> |
| [**Avanti**](ienumpstoretypes-next.md)   | Ottiene il tipo di provider specificato successivo nella sequenza di enumerazione.<br/>                      |
| [**Reset**](ienumpstoretypes-reset.md) | Reimposta all'inizio della sequenza di enumerazione.<br/>                                    |
| [**Ignora**](ienumpstoretypes-skip.md)   | Ignora il tipo di provider specificato nella sequenza di enumerazione.<br/>                          |



 

## <a name="remarks"></a>Commenti

L'oggetto enumeratore deve essere rilasciato quando non viene più utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
