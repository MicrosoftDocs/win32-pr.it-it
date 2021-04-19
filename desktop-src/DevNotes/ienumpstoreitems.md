---
description: Fornisce i metodi di enumerazione standard COM per l'interfaccia IPStore.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: Interfaccia IEnumPStoreItems (PStore. h)
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
ms.openlocfilehash: 11ca255cb13d998d16596bc7cc54d28d2415b227
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326289"
---
# <a name="ienumpstoreitems-interface"></a>Interfaccia IEnumPStoreItems

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Fornisce i metodi di enumerazione standard COM per l'interfaccia [**IPStore**](ipstore.md) .

## <a name="members"></a>Membri

L'interfaccia **IEnumPStoreItems** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumPStoreItems** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IEnumPStoreItems** dispone di questi metodi.



| Metodo                                  | Descrizione                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone**](ienumpstoreitems-clone.md) | Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.<br/> |
| [**Avanti**](ienumpstoreitems-next.md)   | Ottiene l'elemento di dati specificato successivo nella sequenza di enumerazione.<br/>                          |
| [**Reset**](ienumpstoreitems-reset.md) | Reimposta l'inizio della sequenza di enumerazione.<br/>                                    |
| [**Ignora**](ienumpstoreitems-skip.md)   | Ignora l'elemento dati specificato nella sequenza di enumerazione.<br/>                              |



 

## <a name="remarks"></a>Commenti

È necessario liberare ogni elemento dopo l'enumerazione. È inoltre necessario rilasciare l'oggetto enumeratore quando non viene più utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
