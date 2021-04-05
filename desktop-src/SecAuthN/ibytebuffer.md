---
description: Viene fornita l'interfaccia IByteBuffer per la lettura, la scrittura e la gestione di oggetti flusso. Questo oggetto è essenzialmente un wrapper per l'oggetto IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Interfaccia IByteBuffer (scardssp. h)
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
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968294"
---
# <a name="ibytebuffer-interface"></a>Interfaccia IByteBuffer

\[L'interfaccia **IByteBuffer** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'interfaccia [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) fornisce funzionalità simili.\]

Viene fornita l'interfaccia **IByteBuffer** per la lettura, la scrittura e la gestione di oggetti flusso. Questo oggetto è essenzialmente un wrapper per l'oggetto **IStream** .

## <a name="members"></a>Membri

L'interfaccia **IByteBuffer** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IByteBuffer** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IByteBuffer** dispone di questi metodi.



| Metodo                                           | Descrizione                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Clone**](ibytebuffer-clone.md)               | Clona un oggetto **IByteBuffer** .<br/>                                                              |
| [**Commit**](ibytebuffer-commit.md)             | Viene eseguito il commit di una [*transazione*](/windows/desktop/SecGloss/t-gly).<br/> |
| [**CopyTo**](ibytebuffer-copyto.md)             | Copia i byte in un altro oggetto.<br/>                                                                |
| [**Inizializzare**](ibytebuffer-initialize.md)     | Inizializza l'oggetto **IByteBuffer** .<br/>                                                        |
| [**LockRegion**](ibytebuffer-lockregion.md)     | Limita l'accesso a un intervallo di byte.<br/>                                                          |
| [**Lettura**](ibytebuffer-read.md)                 | Legge i byte in memoria.<br/>                                                                       |
| [**Ripristinare**](ibytebuffer-revert.md)             | Elimina le modifiche apportate dall'ultima chiamata al [**commit**](ibytebuffer-commit.md) .<br/>                     |
| [**Seek**](ibytebuffer-seek.md)                 | Modifica il puntatore di ricerca.<br/>                                                                      |
| [**SetSize**](ibytebuffer-setsize.md)           | Modifica la dimensione dell'oggetto flusso.<br/>                                                         |
| [**Stat**](ibytebuffer-stat.md)                 | Recupera le informazioni statistiche su un flusso.<br/>                                              |
| [**UnlockRegion**](ibytebuffer-unlockregion.md) | Rimuove la restrizione di accesso precedentemente impostata da [**LockRegion**](ibytebuffer-lockregion.md).<br/>     |
| [**Scrittura**](ibytebuffer-write.md)               | Scrive i byte nel flusso.<br/>                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer è definito come E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

