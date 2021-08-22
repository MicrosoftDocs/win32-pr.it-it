---
description: Usato per la connessione a un smart card o un lettore specifico, per la creazione di altre interfacce facoltative per eseguire funzioni smart card specifiche, per bloccare un smart card specifico per l'uso esclusivo e per ottenere lo stato di un smart card o di un lettore.
ms.assetid: 67077034-5bd0-4176-9dc7-774caba3d427
title: Interfaccia ISCardManage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage
api_type:
- COM
api_location: ''
ms.openlocfilehash: c027ae9004a8437f3d182fdef3335c8fbbad67abaab5c15e351520f2ae592818
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922650"
---
# <a name="iscardmanage-interface"></a>Interfaccia ISCardManage

\[**L'interfaccia ISCardManage** non è più disponibile per l'uso a Windows Server 2008, Windows Vista e Windows Server 2003 con Service Pack 1 (SP1) e versioni successive. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

La definizione di interfaccia seguente viene fornita come standard che può essere seguita durante lo sviluppo di [*un provider smart card*](../secgloss/s-gly.md) di [*servizi*](../secgloss/c-gly.md).

È **necessario fornire l'interfaccia ISCardManage.** Viene usato per la connessione a un [](../secgloss/r-gly.md)smart card o un lettore [*specifico,*](../secgloss/s-gly.md) per la creazione di altre interfacce facoltative per eseguire funzioni smart card specifiche, per bloccare un smart card specifico per l'uso esclusivo e per ottenere lo stato di un smart card o di un lettore. Come set, questi servizi possono essere responsabili della gestione di un contesto ben definito all'interno del quale un'applicazione può comunicare con un smart card [*o*](../secgloss/s-gly.md) [*lettore.*](../secgloss/r-gly.md)

Di seguito è riportato un uso tipico **dell'interfaccia ISCardManage.**

**Per connettersi a un smart card**

1.  Creare **l'interfaccia ISCardManage** associata alla scheda.
2.  Connessione a un smart card connettersi a un lettore smart card specifico ([**AttachByIFD**](iscardmanage-attachbyifd.md)) o usando un handle acquisito in precedenza ([**AttachByHandle**](iscardmanage-attachbyhandle.md)).
3.  Creare altre interfacce per eseguire smart card seguenti ([**CreateCardAuth**](iscardmanage-createcardauth.md), [**CreateFileAccess**](iscardmanage-createfileaccess.md), [**CreateCHVerification**](iscardmanage-createchverification.md)o [**CreateInterface**](iscardmanage-createinterface.md)).
4.  Rilasciare la scheda ([**Scollega**](iscardmanage-detach.md)).
5.  Rilasciare **l'interfaccia ISCardManage** e altre in base alle esigenze.

## <a name="members"></a>Membri

**L'interfaccia ISCardManage** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardManage** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ISCardManage** include questi metodi.



| Metodo                                                            | Descrizione                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscardmanage-attachbyhandle.md)             | Consente a un'applicazione di creare un collegamento di comunicazione a un smart card utilizzando un handle restituito dal gestore smart card [*risorse.*](../secgloss/r-gly.md)<br/>                                              |
| [**AttachByIFD**](iscardmanage-attachbyifd.md)                   | Consente a un'applicazione di richiedere la definizione di un contesto per un lettore specifico a cui viene fatto riferimento con un nome visualizzato.<br/>                                                                                                                                               |
| [**CreateCardAuth**](iscardmanage-createcardauth.md)             | Consente la creazione di [**un'interfaccia ISCardAuth.**](iscardauth.md)<br/>                                                                                                                                                                                            |
| [**CreateCHVerification**](iscardmanage-createchverification.md) | Consente la creazione di [**un'interfaccia ISCardVerify.**](iscardverify.md)<br/>                                                                                                                                                                                        |
| [**CreateFileAccess**](iscardmanage-createfileaccess.md)         | Consente la creazione di [**un'interfaccia ISCardFileAccess.**](iscardfileaccess.md)<br/>                                                                                                                                                                                |
| [**CreateInterface**](iscardmanage-createinterface.md)           | Consente la creazione di un'interfaccia.<br/>                                                                                                                                                                                                                            |
| [**Detach**](iscardmanage-detach.md)                             | Rilascia l'allegato a un smart card o lettore allocato rispettivamente da [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD.**](iscardmanage-attachbyifd.md)<br/>                                                                |
| [**Riconnetti**](iscardmanage-reconnect.md)                       | Consente a un'applicazione di riconnettersi a un smart card o lettore senza dover eseguire [**un'operazione Detach**](iscardmanage-detach.md) seguita rispettivamente da [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD.**](iscardmanage-attachbyifd.md)<br/> |
| [**SCardLock**](iscardmanage-scardlock.md)                       | Blocca un'istanza smart card o un lettore connesso per uso esclusivo.<br/>                                                                                                                                                                                                       |
| [**SCardUnlock**](iscardmanage-scardunlock.md)                   | Rilascia l'uso esclusivo dell'smart card o del lettore connesso.<br/>                                                                                                                                                                                                   |
| [**Status**](iscardmanage-status.md)                             | Consente a un'applicazione di ottenere lo stato corrente del smart card o del lettore.<br/>                                                                                                                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



 

 
