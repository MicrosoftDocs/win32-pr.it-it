---
description: Fornisce i metodi di enumerazione standard COM per l'interfaccia IPStore.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Interfaccia IEnumPStoreProviders (PStore. h)
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
ms.openlocfilehash: e01bd28722fdb4d5a0ff7e3db4f715ddc1df2315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332098"
---
# <a name="ienumpstoreproviders-interface"></a>Interfaccia IEnumPStoreProviders

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Fornisce i metodi di enumerazione standard COM per l'interfaccia [**IPStore**](ipstore.md) .

## <a name="members"></a>Membri

L'interfaccia **IEnumPStoreProviders** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreProviders** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IEnumPStoreProviders** dispone di questi metodi.



| Metodo                                      | Descrizione                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumpstoreproviders-clone.md) | Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.<br/> |
| [**Avanti**](ienumpstoreproviders-next.md)   | Ottiene il provider specificato successivo nella sequenza di enumerazione.<br/>                           |
| [**Reset**](ienumpstoreproviders-reset.md) | Reimposta l'inizio della sequenza di enumerazione.<br/>                                    |
| [**Ignora**](ienumpstoreproviders-skip.md)   | Ignora il provider specificato nella sequenza di enumerazione.<br/>                               |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
