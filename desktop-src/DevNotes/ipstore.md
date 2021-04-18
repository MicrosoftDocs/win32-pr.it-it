---
description: Fornisce metodi standard COM per gestire gli elementi di dati di archiviazione protetti.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: Interfaccia IPStore (PStore. h)
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
ms.openlocfilehash: 4193e21255445c397bfab6439c4890789b8c5562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324703"
---
# <a name="ipstore-interface"></a>Interfaccia IPStore

\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP. È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive. PStore usa un'implementazione precedente della protezione dei dati. Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Questa interfaccia può essere modificata o non disponibile nelle versioni future di Windows.\]

Fornisce metodi standard COM per gestire gli elementi di dati di archiviazione protetti. Il metodo [**PStoreCreateInstance**](pstorecreateinstance.md) restituisce un puntatore a questa interfaccia.

## <a name="members"></a>Membri

L'interfaccia **IPStore** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IPStore** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IPStore** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**CloseItem**](ipstore-closeitem.md)                   | Chiude un elemento dati specificato dall'archivio protetto.<br/>                                                       |
| [**CreateSubtype**](ipstore-createsubtype.md)           | Crea il sottotipo specificato all'interno del tipo specificato.<br/>                                                   |
| [**CreateType**](ipstore-createtype.md)                 | Crea il tipo specificato con il nome specificato.<br/>                                                        |
| [**DeleteItem**](ipstore-deleteitem.md)                 | Elimina l'elemento specificato dall'archivio protetto.<br/>                                                     |
| [**DeleteSubtype**](ipstore-deletesubtype.md)           | Elimina il sottotipo di elemento specificato dalla risorsa di archiviazione protetta.<br/>                                             |
| [**DeleteType**](ipstore-deletetype.md)                 | Elimina il tipo specificato dalla risorsa di archiviazione protetta.<br/>                                                     |
| [**EnumItems**](ipstore-enumitems.md)                   | Restituisce il puntatore a interfaccia di un sottotipo per l'enumerazione degli elementi nel database di archiviazione protetta.<br/>        |
| [**EnumSubtypes**](ipstore-enumsubtypes.md)             | Restituisce un'interfaccia per l'enumerazione dei sottotipi dei tipi attualmente registrati nel database protetto.<br/> |
| [**EnumTypes**](ipstore-enumtypes.md)                   | Restituisce un'interfaccia per l'enumerazione dei tipi attualmente registrati nel database protetto.<br/>             |
| [**GetInfo**](ipstore-getinfo.md)                       | Recupera le informazioni sul provider di archiviazione.<br/>                                                          |
| [**GetProvParam**](ipstore-getprovparam.md)             | Non implementato.<br/>                                                                                           |
| [**GetSubtypeInfo**](ipstore-getsubtypeinfo.md)         | Recupera le informazioni associate a un sottotipo.<br/>                                                           |
| [**GetTypeInfo**](ipstore-gettypeinfo.md)               | Recupera le informazioni associate a un tipo.<br/>                                                              |
| [**OpenItem**](ipstore-openitem.md)                     | Apre un elemento per più accessi.<br/>                                                                       |
| [**ReadAccessRuleSet**](ipstore-readaccessruleset.md)   | Non implementato.<br/>                                                                                           |
| [**ReadItem**](ipstore-readitem.md)                     | Legge l'elemento dati specificato dall'archivio protetto.<br/>                                                      |
| [**SetProvParam**](ipstore-setprovparam.md)             | Imposta le informazioni sul parametro specificato.<br/>                                                                  |
| [**WriteAccessRuleset**](ipstore-writeaccessruleset.md) | Non implementato.<br/>                                                                                           |
| [**WriteItem**](ipstore-writeitem.md)                   | Scrive un elemento di dati in un archivio protetto.<br/>                                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
