---
description: Fornisce metodi standard COM per gestire gli elementi di dati di archiviazione protetti.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: Interfaccia IPStore (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d6404d182a0c46de222b64892caa8b0e853610c980bfb79d286f781277493cba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749707"
---
# <a name="ipstore-interface"></a>Interfaccia ipstore

\[Protected Archiviazione (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. Pstore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

\[Questa interfaccia potrebbe essere modificata o non disponibile nelle versioni future Windows.\]

Fornisce metodi standard COM per gestire gli elementi di dati di archiviazione protetti. Il [**metodo PStoreCreateInstance**](pstorecreateinstance.md) restituisce un puntatore a questa interfaccia.

## <a name="members"></a>Membri

**L'interfaccia IPStore** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IPStore** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IPStore** include questi metodi.



| Metodo                                                   | Descrizione                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**CloseItem**](ipstore-closeitem.md)                   | Chiude un elemento di dati specificato dall'archiviazione protetta.<br/>                                                       |
| [**CreateSubtype**](ipstore-createsubtype.md)           | Crea il sottotipo specificato all'interno del tipo specificato.<br/>                                                   |
| [**Createtype**](ipstore-createtype.md)                 | Crea il tipo specificato con il nome specificato.<br/>                                                        |
| [**Deleteitem**](ipstore-deleteitem.md)                 | Elimina l'elemento specificato dall'archiviazione protetta.<br/>                                                     |
| [**DeleteSubtype**](ipstore-deletesubtype.md)           | Elimina il sottotipo di elemento specificato dall'archiviazione protetta.<br/>                                             |
| [**DeleteType**](ipstore-deletetype.md)                 | Elimina il tipo specificato dall'archiviazione protetta.<br/>                                                     |
| [**EnumItems**](ipstore-enumitems.md)                   | Restituisce il puntatore a interfaccia di un sottotipo per l'enumerazione degli elementi nel database di archiviazione protetta.<br/>        |
| [**EnumSubtypes**](ipstore-enumsubtypes.md)             | Restituisce un'interfaccia per enumerare i sottotipi dei tipi attualmente registrati nel database protetto.<br/> |
| [**EnumTypes**](ipstore-enumtypes.md)                   | Restituisce un'interfaccia per enumerare i tipi attualmente registrati nel database protetto.<br/>             |
| [**GetInfo**](ipstore-getinfo.md)                       | Recupera informazioni sul provider di archiviazione.<br/>                                                          |
| [**GetProvParam**](ipstore-getprovparam.md)             | Non implementato.<br/>                                                                                           |
| [**GetSubtypeInfo**](ipstore-getsubtypeinfo.md)         | Recupera le informazioni associate a un sottotipo.<br/>                                                           |
| [**GetTypeInfo**](ipstore-gettypeinfo.md)               | Recupera le informazioni associate a un tipo.<br/>                                                              |
| [**OpenItem**](ipstore-openitem.md)                     | Apre un elemento per più accessi.<br/>                                                                       |
| [**ReadAccessRuleSet**](ipstore-readaccessruleset.md)   | Non implementato.<br/>                                                                                           |
| [**ReadItem**](ipstore-readitem.md)                     | Legge l'elemento di dati specificato dall'archiviazione protetta.<br/>                                                      |
| [**SetProvParam**](ipstore-setprovparam.md)             | Imposta le informazioni sui parametri specificati.<br/>                                                                  |
| [**WriteAccessRuleset**](ipstore-writeaccessruleset.md) | Non implementato.<br/>                                                                                           |
| [**WriteItem**](ipstore-writeitem.md)                   | Scrive un elemento di dati nell'archiviazione protetta.<br/>                                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Pstore.h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
