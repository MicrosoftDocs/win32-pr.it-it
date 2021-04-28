---
description: "Interfaccia IEnumPStoreProviders: fornisce metodi di enumerazione standard COM per l'interfaccia IPStore."
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Interfaccia IEnumPStoreProviders (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089349"
---
# <a name="ienumpstoreproviders-interface"></a>Interfaccia IEnumPStoreProviders

\[L'archiviazione protetta (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Fornisce metodi di enumerazione standard COM per [**l'interfaccia IPStore.**](ipstore.md)

## <a name="members"></a>Membri

**L'interfaccia IEnumPStoreProviders** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumPStoreProviders** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IEnumPStoreProviders** include questi metodi.



| Metodo                                      | Descrizione                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumpstoreproviders-clone.md) | Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.<br/> |
| [**Avanti**](ienumpstoreproviders-next.md)   | Ottiene il provider specificato successivo nella sequenza di enumerazione.<br/>                           |
| [**Reset**](ienumpstoreproviders-reset.md) | Reimposta all'inizio della sequenza di enumerazione.<br/>                                    |
| [**Ignora**](ienumpstoreproviders-skip.md)   | Ignora il provider specificato nella sequenza di enumerazione.<br/>                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
