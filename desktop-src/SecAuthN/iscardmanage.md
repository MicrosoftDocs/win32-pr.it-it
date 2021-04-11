---
description: Usato per la connessione a una smart card o un lettore specifico, per la creazione di altre interfacce facoltative per eseguire funzioni di smart card specifiche, per bloccare una smart card specifica per l'uso esclusivo e per ottenere lo stato di una smart card o un lettore.
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
ms.openlocfilehash: cce31ea21701c098b09a0bd96360afb374a9bccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233263"
---
# <a name="iscardmanage-interface"></a>Interfaccia ISCardManage

\[L'interfaccia **ISCardManage** non è più disponibile per l'uso a partire da windows Server 2008, Windows Vista e windows Server 2003 con Service Pack 1 (SP1) e versioni successive. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

La definizione di interfaccia seguente viene fornita come standard che può essere seguita durante lo sviluppo di un [*provider di servizi*](../secgloss/c-gly.md)per [*Smart Card*](../secgloss/s-gly.md) .

È necessario fornire l'interfaccia **ISCardManage** . Viene utilizzato per la connessione a una [*Smart Card*](../secgloss/s-gly.md) o un [*lettore*](../secgloss/r-gly.md)specifico, per la creazione di altre interfacce facoltative per l'esecuzione di funzioni smart card specifiche, per il blocco di una smart card specifica per l'utilizzo esclusivo e per ottenere lo stato di una smart card o di un lettore. Come set, questi servizi possono essere responsabili della gestione di un contesto ben definito all'interno del quale un'applicazione può comunicare con una [*Smart Card*](../secgloss/s-gly.md) o un [*lettore*](../secgloss/r-gly.md).

Di seguito è riportato un utilizzo tipico dell'interfaccia **ISCardManage** .

**Per connettersi a una smart card**

1.  Creare l'interfaccia **ISCardManage** associata alla scheda.
2.  Connettersi a una smart card collegandosi a un lettore di smart card specifico ([**AttachByIFD**](iscardmanage-attachbyifd.md)) o usando un handle acquisito in precedenza ([**AttachByHandle**](iscardmanage-attachbyhandle.md)).
3.  Creare altre interfacce per eseguire operazioni di smart card ([**CreateCardAuth**](iscardmanage-createcardauth.md), [**CreateFileAccess**](iscardmanage-createfileaccess.md), [**CreateCHVerification**](iscardmanage-createchverification.md)o [**CreateInterface**](iscardmanage-createinterface.md)).
4.  Rilasciare la scheda ([**scollegamento**](iscardmanage-detach.md)).
5.  Rilasciare l'interfaccia **ISCardManage** e altre come richiesto.

## <a name="members"></a>Membri

L'interfaccia **ISCardManage** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardManage** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISCardManage** dispone di questi metodi.



| Metodo                                                            | Descrizione                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscardmanage-attachbyhandle.md)             | Consente a un'applicazione di creare un collegamento di comunicazione a una Smart Card utilizzando un handle restituito dal [*gestore di risorse*](../secgloss/r-gly.md)della smart card.<br/>                                              |
| [**AttachByIFD**](iscardmanage-attachbyifd.md)                   | Consente a un'applicazione di richiedere la creazione di un contesto per un lettore specifico a cui viene fatto riferimento con un nome visualizzato.<br/>                                                                                                                                               |
| [**CreateCardAuth**](iscardmanage-createcardauth.md)             | Consente la creazione di un'interfaccia [**ISCardAuth**](iscardauth.md) .<br/>                                                                                                                                                                                            |
| [**CreateCHVerification**](iscardmanage-createchverification.md) | Consente la creazione di un'interfaccia [**ISCardVerify**](iscardverify.md) .<br/>                                                                                                                                                                                        |
| [**CreateFileAccess**](iscardmanage-createfileaccess.md)         | Consente la creazione di un'interfaccia [**ISCardFileAccess**](iscardfileaccess.md) .<br/>                                                                                                                                                                                |
| [**CreateInterface**](iscardmanage-createinterface.md)           | Consente la creazione di un'interfaccia.<br/>                                                                                                                                                                                                                            |
| [**Scollegare**](iscardmanage-detach.md)                             | Rilascia l'allegato a una smart card o un lettore specifico allocato rispettivamente da [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD**](iscardmanage-attachbyifd.md) .<br/>                                                                |
| [**Riconnetti**](iscardmanage-reconnect.md)                       | Consente a un'applicazione di riconnettersi a una smart card o a un lettore senza dover eseguire uno [**scollegamento**](iscardmanage-detach.md) seguito rispettivamente da [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD**](iscardmanage-attachbyifd.md) .<br/> |
| [**SCardLock**](iscardmanage-scardlock.md)                       | Blocca una smart card o un lettore connesso per un uso esclusivo.<br/>                                                                                                                                                                                                       |
| [**SCardUnlock**](iscardmanage-scardunlock.md)                   | Rilascia l'utilizzo esclusivo della smart card o del lettore connesso.<br/>                                                                                                                                                                                                   |
| [**Stato**](iscardmanage-status.md)                             | Consente a un'applicazione di ottenere lo stato corrente della smart card o del lettore.<br/>                                                                                                                                                                                    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



 

 
