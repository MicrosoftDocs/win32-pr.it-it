---
description: Consente di aprire e gestire una connessione a una smart card.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Interfaccia scheda (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528152"
---
# <a name="iscard-interface"></a>Interfaccia scheda

\[L'interfaccia della **scheda** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

L'interfaccia della **scheda** consente di aprire e gestire una connessione a una [*Smart Card*](../secgloss/s-gly.md). Ogni connessione a una scheda richiede una singola istanza corrispondente dell'interfaccia della **scheda** .

Il gestore di [*risorse*](../secgloss/r-gly.md) della smart card deve essere disponibile ogni volta che viene creata un'istanza di una **scheda** . Se il servizio non è disponibile, la creazione dell'interfaccia avrà esito negativo.

Nell'esempio seguente viene illustrato un utilizzo tipico dell'interfaccia della **scheda** . L' **interfaccia della scheda viene** utilizzata per connettersi alla smart card, inviare una [*transazione*](../secgloss/t-gly.md)e rilasciare la smart card.

**Per inviare una transazione a una scheda specifica**

1.  Creare un'interfaccia di **scheda** .
2.  Connettersi a una smart card specificando un [*lettore*](../secgloss/r-gly.md) di smart card o utilizzando un handle valido precedentemente definito.
3.  Creare comandi di transazione con [**ISCardCmd**](iscardcmd.md)e interfacce smart card [**ISCardISO7816**](iscardiso7816.md) .
4.  Utilizzare **la scheda per** inviare i comandi di transazione per l'elaborazione da parte della smart card.
5.  Utilizzare **la scheda per** rilasciare la smart card.
6.  Rilasciare l'interfaccia di **scheda** .

## <a name="members"></a>Membri

L'interfaccia della **scheda** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . La **scheda** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia della **scheda** ha questi metodi.



| Metodo                                          | Descrizione                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscard-attachbyhandle.md) | Connette un oggetto a un handle di smart card aperto e configurato.<br/>                                                                                                                                                      |
| [**AttachByReader**](iscard-attachbyreader.md) | Apre la smart card nel lettore denominato.<br/>                                                                                                                                                                            |
| [**Scollegare**](iscard-detach.md)                 | Chiude la connessione aperta alla smart card.<br/>                                                                                                                                                                        |
| [**LockSCard**](iscard-lockscard.md)           | Attesta l'accesso esclusivo alla smart card.<br/>                                                                                                                                                                           |
| [**Ricollegare**](iscard-reattach.md)             | Reimposta e reinizializza la smart card.<br/>                                                                                                                                                                             |
| [**Transazione**](iscard-transaction.md)       | Esegue un'operazione di scrittura e lettura sull'oggetto comando della smart card ([*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md)).<br/> |
| [**UnlockScard**](iscard-unlockscard.md)       | Rilascia accesso esclusivo alla smart card.<br/>                                                                                                                                                                         |



 

### <a name="properties"></a>Proprietà

L'interfaccia della **scheda** dispone di queste proprietà.



| Proprietà                                               | Tipo di accesso          | Descrizione                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atr**](iscard-get-atr.md)<br/>               | Sola lettura<br/> | Recupera la [*stringa ATR*](../secgloss/a-gly.md) della smart card.<br/>                                                                   |
| [**CardHandle**](iscard-get-cardhandle.md)<br/> | Sola lettura<br/> | Recupera l'handle per la smart card connessa.<br/>                                                                                                                                  |
| [**Context**](iscard-get-context.md)<br/>       | Sola lettura<br/> | Recupera l'handle di contesto corrente di [*Resource Manager*](../secgloss/r-gly.md) .<br/>                            |
| [**Protocollo**](iscard-get-protocol.md)<br/>     | Sola lettura<br/> | Recupera l'identificatore del protocollo attualmente in uso nella smart card.<br/>                                                                                                        |
| [**Stato**](iscard-get-status.md)<br/>         | Sola lettura<br/> | Recupera lo [*stato*](../secgloss/s-gly.md) corrente in cui si trova la [*Smart Card*](../secgloss/s-gly.md) .<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | La \_ scheda IID è definita come 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



 

 
