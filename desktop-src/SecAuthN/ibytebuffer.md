---
description: L'interfaccia IByteBuffer viene fornita per leggere, scrivere e gestire gli oggetti flusso. Questo oggetto è essenzialmente un wrapper per l'oggetto IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Interfaccia IByteBuffer (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8f0aa81106629142efeec7e22bdb495bea853c3c689d6b55887a62f896d89d62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417411"
---
# <a name="ibytebuffer-interface"></a>Interfaccia IByteBuffer

\[**L'interfaccia IByteBuffer** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. [**L'interfaccia IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre funzionalità simili.\]

**L'interfaccia IByteBuffer** viene fornita per leggere, scrivere e gestire gli oggetti flusso. Questo oggetto è essenzialmente un wrapper per **l'oggetto IStream.**

## <a name="members"></a>Membri

**L'interfaccia IByteBuffer** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IByteBuffer** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IByteBuffer** include questi metodi.



| Metodo                                           | Descrizione                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Clone**](ibytebuffer-clone.md)               | Clona un **oggetto IByteBuffer.**<br/>                                                              |
| [**Eseguire il commit**](ibytebuffer-commit.md)             | Esegue il commit di una [*transazione*](/windows/desktop/SecGloss/t-gly).<br/> |
| [**CopyTo**](ibytebuffer-copyto.md)             | Copia i byte in un altro oggetto .<br/>                                                                |
| [**Inizializzare**](ibytebuffer-initialize.md)     | Inizializza **l'oggetto IByteBuffer.**<br/>                                                        |
| [**LockRegion**](ibytebuffer-lockregion.md)     | Limita l'accesso a un intervallo di byte.<br/>                                                          |
| [**Leggere**](ibytebuffer-read.md)                 | Legge i byte in memoria.<br/>                                                                       |
| [**Ripristinare**](ibytebuffer-revert.md)             | Rimuove le modifiche dopo [**l'ultima chiamata Commit.**](ibytebuffer-commit.md)<br/>                     |
| [**Seek**](ibytebuffer-seek.md)                 | Modifica il puntatore seek.<br/>                                                                      |
| [**SetSize**](ibytebuffer-setsize.md)           | Modifica la dimensione dell'oggetto flusso.<br/>                                                         |
| [**Stat**](ibytebuffer-stat.md)                 | Recupera informazioni statistiche su un flusso.<br/>                                              |
| [**UnlockRegion**](ibytebuffer-unlockregion.md) | Rimuove la restrizione di accesso impostata in precedenza [**da LockRegion.**](ibytebuffer-lockregion.md)<br/>     |
| [**Scrivere**](ibytebuffer-write.md)               | Scrive byte nel flusso.<br/>                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID IByteBuffer è definito \_ come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

