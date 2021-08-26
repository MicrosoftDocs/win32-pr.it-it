---
description: Consente di aprire e gestire una connessione a un smart card.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Interfaccia ISCard (Scardmgr.h)
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
ms.openlocfilehash: 68015cc4e834aaa1baaec0046a472d5a290cb22b0d0879e6d6f2fccfd9d21d67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015541"
---
# <a name="iscard-interface"></a>Interfaccia ISCard

\[**L'interfaccia ISCard** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

**L'interfaccia ISCard** consente di aprire e gestire una connessione a un [*smart card*](../secgloss/s-gly.md). Ogni connessione a una scheda richiede una singola istanza corrispondente **dell'interfaccia ISCard.**

Il smart card [*resource manager*](../secgloss/r-gly.md) deve essere disponibile ogni volta che viene creata un'istanza di **ISCard.** Se questo servizio non è disponibile, la creazione dell'interfaccia avrà esito negativo.

L'esempio seguente illustra un uso tipico **dell'interfaccia ISCard.** **L'interfaccia ISCard** viene usata per connettersi al smart card, inviare [*una*](../secgloss/t-gly.md)transazione e rilasciare il smart card.

**Per inviare una transazione a una scheda specifica**

1.  Creare **un'interfaccia ISCard.**
2.  Connettersi a un smart card specificando un smart card [*lettore*](../secgloss/r-gly.md) o usando un handle valido stabilito in precedenza.
3.  Creare comandi di transazione [**con ISCardCmd**](iscardcmd.md)e [**ISCardISO7816**](iscardiso7816.md) smart card interfacce.
4.  Usare **ISCard** per inviare i comandi di transazione per l'elaborazione da parte del smart card.
5.  Usare **ISCard** per rilasciare il smart card.
6.  Rilasciare **l'interfaccia ISCard.**

## <a name="members"></a>Membri

**L'interfaccia ISCard** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCard** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia ISCard** include questi metodi.



| Metodo                                          | Descrizione                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscard-attachbyhandle.md) | Associa un oggetto a un handle di smart card aperto e configurato.<br/>                                                                                                                                                      |
| [**AttachByReader**](iscard-attachbyreader.md) | Apre il smart card nel lettore denominato.<br/>                                                                                                                                                                            |
| [**Detach**](iscard-detach.md)                 | Chiude la connessione aperta al smart card.<br/>                                                                                                                                                                        |
| [**LockSCard**](iscard-lockscard.md)           | Rivendica l'accesso esclusivo alla smart card.<br/>                                                                                                                                                                           |
| [**Ricollegare**](iscard-reattach.md)             | Reimposta e reinizializza il smart card.<br/>                                                                                                                                                                             |
| [**Transazione**](iscard-transaction.md)       | Esegue un'operazione di scrittura e lettura sull'oggetto smart card comando ( unità dati [*del protocollo dell'applicazione*](../secgloss/a-gly.md)).<br/> |
| [**UnlockScard**](iscard-unlockscard.md)       | Rilascia l'accesso esclusivo al smart card.<br/>                                                                                                                                                                         |



 

### <a name="properties"></a>Proprietà

**L'interfaccia ISCard** ha queste proprietà.



| Proprietà                                               | Tipo di accesso          | Descrizione                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atr**](iscard-get-atr.md)<br/>               | Sola lettura<br/> | Recupera la stringa [*ATR del*](../secgloss/a-gly.md) smart card.<br/>                                                                   |
| [**CardHandle**](iscard-get-cardhandle.md)<br/> | Sola lettura<br/> | Recupera l'handle per l'oggetto smart card.<br/>                                                                                                                                  |
| [**Context**](iscard-get-context.md)<br/>       | Sola lettura<br/> | Recupera l'handle [*di contesto di Resource Manager*](../secgloss/r-gly.md) corrente.<br/>                            |
| [**Protocollo**](iscard-get-protocol.md)<br/>     | Sola lettura<br/> | Recupera l'identificatore del protocollo attualmente in uso nel smart card.<br/>                                                                                                        |
| [**Status**](iscard-get-status.md)<br/>         | Sola lettura<br/> | Recupera lo stato [*corrente in*](../secgloss/s-gly.md) [*cui*](../secgloss/s-gly.md) smart card si trova.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCard è definito come \_ 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



 

 
