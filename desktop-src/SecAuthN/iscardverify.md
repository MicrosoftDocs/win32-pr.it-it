---
description: Fornisce servizi per l'impostazione del codice CHV (scheda di verifica del contenitore) e per la verifica dell'utente.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: Interfaccia ISCardVerify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757016"
---
# <a name="iscardverify-interface"></a>Interfaccia ISCardVerify

\[L'interfaccia **ISCardVerify** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

La definizione di interfaccia seguente viene fornita come standard che può essere seguita durante lo sviluppo di un [*provider di servizi*](../secgloss/c-gly.md)per [*Smart Card*](../secgloss/s-gly.md) . L'interfaccia **ISCardVerify** fornisce servizi per l'impostazione del codice CHV (scheda di verifica del contenitore) e per la verifica dell'utente.

La classe **ISCardVerify** è definita per le applicazioni che implementano i criteri CHV specifici dell'applicazione e che hanno una conoscenza approfondita dell'implementazione interna della smart card.

Di seguito è riportato un utilizzo tipico dell'interfaccia **ISCardVerify** .

La procedura seguente usa **ISCardVerify** per modificare il codice CHV.

**Per modificare il codice CHV di una smart card**

1.  Creare un'interfaccia **ISCardVerify** (tramite il metodo di interfaccia [**ISCardManage**](iscardmanage.md) corrispondente).
2.  Chiamare il metodo [**ChangeCode**](iscardverify-changecode.md) e fornire nuovo codice, specificando se è locale o globale e se è abilitato o disabilitato.
3.  Rilasciare l'interfaccia **ISCardVerify** .

## <a name="members"></a>Membri

L'interfaccia **ISCardVerify** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardVerify** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISCardVerify** dispone di questi metodi.



| Metodo                                                        | Descrizione                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeCode**](iscardverify-changecode.md)                 | Modifica il codice CHV corrente.<br/>                                                                                                    |
| [**ResetSecurityState**](iscardverify-resetsecuritystate.md) | Reimposta il [*contesto di sicurezza*](../secgloss/s-gly.md) della smart card.<br/> |
| [**Sbloccare**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))                       | Abilita nuovamente il [*contesto di sicurezza*](../secgloss/s-gly.md).<br/>               |
| [**Verificare**](iscardverify-verify.md)                         | Autentica l'utente.<br/>                                                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



 

 
