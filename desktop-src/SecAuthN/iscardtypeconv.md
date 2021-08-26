---
description: Fornisce i metodi necessari per supportare gli utenti delle altre smart card COM.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Interfaccia ISCardTypeConv (Scarddat.h)
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
ms.openlocfilehash: 7fbf009eeeb4f104e5bf09ba8e33b6b2b76eb889a0e44e7594172c697b438d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013591"
---
# <a name="iscardtypeconv-interface"></a>Interfaccia ISCardTypeConv

\[**L'interfaccia ISCardTypeConv** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

**L'interfaccia ISCardTypeConv** fornisce i metodi necessari per supportare gli utenti delle altre smart card [*COM.*](../secgloss/s-gly.md) Questa interfaccia viene fornita solo per la compatibilità con le versioni precedenti e non deve più essere usata.

## <a name="members"></a>Membri

**L'interfaccia ISCardTypeConv** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardTypeConv** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **ISCardTypeConv.**



| Metodo                                                                              | Descrizione                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertByteArrayToByteBuffer**](iscardtypeconv-convertbytearraytobytebuffer.md) | Converte una tipica matrice di byte C/C++ in un buffer universale di byte **(oggetto IStream).**<br/>                                   |
| [**ConvertByteBufferToByteArray**](iscardtypeconv-convertbytebuffertobytearray.md) | Converte una matrice di byte mappata in un buffer universale di byte (oggetto **IStream)** in una tipica matrice di byte C/C++.<br/>          |
| [**ConvertByteBufferToSafeArray**](iscardtypeconv-convertbytebuffertosafearray.md) | Converte una matrice di byte mappata in un buffer universale di byte (oggetto **IStream)** in un SAFEARRAY di unsigned char (byte).<br/> |
| [**ConvertSafeArrayToByteBuffer**](iscardtypeconv-convertsafearraytobytebuffer.md) | Converte una matrice di byte definita come SAFEARRAY in un buffer universale di byte **(oggetto IStream).**<br/>                          |
| [**CreateByteArray**](iscardtypeconv-createbytearray.md)                           | Crea una matrice di byte.<br/>                                                                                                   |
| [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)                         | Crea un buffer universale di byte di cui è stato eseguito il mapping in un **oggetto IStream** ([**IByteBuffer**](ibytebuffer.md)).<br/>                  |
| [**CreateSafeArray**](iscardtypeconv-createsafearray.md)                           | Crea un SAFEARRAY di automazione di caratteri senza segno (byte).<br/>                                                              |
| [**FreeIStreamMemoryPtr**](iscardtypeconv-freeistreammemoryptr.md)                 | Libera un puntatore di memoria al blocco di memoria HGLOBAL gestito da **un'interfaccia COM IStream.**<br/>                                  |
| [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)                     | Acquisisce un puntatore di byte al blocco di memoria HGLOBAL gestito dall'interfaccia COM **IStream.**<br/>                        |
| [**SizeOfIStream**](iscardtypeconv-sizeofistream.md)                               | Determina le dimensioni (numero di byte) di **un'interfaccia COM IStream.**<br/>                                                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardTypeConv è definito come \_ 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



 

 
