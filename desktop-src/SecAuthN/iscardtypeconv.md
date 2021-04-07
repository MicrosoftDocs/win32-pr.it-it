---
description: Fornisce i metodi necessari per supportare gli utenti delle altre interfacce COM per smart card.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Interfaccia ISCardTypeConv (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881682"
---
# <a name="iscardtypeconv-interface"></a>Interfaccia ISCardTypeConv

\[L'interfaccia **ISCardTypeConv** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

L'interfaccia **ISCardTypeConv** fornisce i metodi necessari per supportare gli utenti delle altre interfacce com per [*Smart Card*](../secgloss/s-gly.md) . Questa interfaccia viene fornita solo per compatibilità con le versioni precedenti e non deve più essere utilizzata.

## <a name="members"></a>Membri

L'interfaccia **ISCardTypeConv** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardTypeConv** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISCardTypeConv** dispone di questi metodi.



| Metodo                                                                              | Descrizione                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertByteArrayToByteBuffer**](iscardtypeconv-convertbytearraytobytebuffer.md) | Converte una matrice di byte C/C++ tipica in un buffer universale di byte (oggetto **IStream** ).<br/>                                   |
| [**ConvertByteBufferToByteArray**](iscardtypeconv-convertbytebuffertobytearray.md) | Converte una matrice di byte mappata in un buffer universale di byte (oggetto **IStream** ) in una matrice di byte C/C++ tipica.<br/>          |
| [**ConvertByteBufferToSafeArray**](iscardtypeconv-convertbytebuffertosafearray.md) | Converte una matrice di byte mappata in un buffer universale di byte (oggetto **IStream** ) in un SAFEARRAY di unsigned char (byte).<br/> |
| [**ConvertSafeArrayToByteBuffer**](iscardtypeconv-convertsafearraytobytebuffer.md) | Converte una matrice di byte definita come SAFEARRAY in un buffer universale di byte (oggetto **IStream** ).<br/>                          |
| [**CreateByteArray**](iscardtypeconv-createbytearray.md)                           | Crea una matrice di byte.<br/>                                                                                                   |
| [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)                         | Crea un buffer universale di byte mappato in un oggetto **IStream** ([**IByteBuffer**](ibytebuffer.md)).<br/>                  |
| [**CreateSafeArray**](iscardtypeconv-createsafearray.md)                           | Crea un SAFEARRAY di automazione di caratteri non firmati (byte).<br/>                                                              |
| [**FreeIStreamMemoryPtr**](iscardtypeconv-freeistreammemoryptr.md)                 | Libera un puntatore di memoria per il blocco di memoria HGLOBAL gestito da un'interfaccia com **IStream** .<br/>                                  |
| [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)                     | Acquisisce un puntatore di byte al blocco di memoria HGLOBAL gestito dall'interfaccia com **IStream** .<br/>                        |
| [**SizeOfIStream**](iscardtypeconv-sizeofistream.md)                               | Determina la dimensione (numero di byte) di un'interfaccia com **IStream** .<br/>                                                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv è definito come 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



 

 
