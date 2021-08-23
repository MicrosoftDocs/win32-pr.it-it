---
description: Fornisce servizi per l'impostazione del codice CHV (verifica del titolare della carta) e per la verifica dell'utente.
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
ms.openlocfilehash: e2f676360636395e0df811abed225c1a53be69a7da07f38a8acb08fc8d45e2ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141014"
---
# <a name="iscardverify-interface"></a>Interfaccia ISCardVerify

\[**L'interfaccia ISCardVerify** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

La definizione di interfaccia seguente viene fornita come standard che può essere seguita quando si sviluppa un provider [*smart card*](../secgloss/s-gly.md) [*di servizi*](../secgloss/c-gly.md). **L'interfaccia ISCardVerify** fornisce servizi per l'impostazione del codice CHV (verifica del titolare della carta) e per la verifica dell'utente.

La **classe ISCardVerify** è definita per le applicazioni che implementano criteri CHV specifici dell'applicazione e che hanno una conoscenza dettagliata dell'implementazione interna del smart card.

Di seguito è riportato un uso tipico **dell'interfaccia ISCardVerify.**

La procedura seguente usa **ISCardVerify** per modificare il codice CHV.

**Per modificare il codice CHV di un smart card**

1.  Creare **un'interfaccia ISCardVerify** (tramite il metodo di [**interfaccia ISCardManage**](iscardmanage.md) corrispondente).
2.  Chiamare il [**metodo ChangeCode**](iscardverify-changecode.md) e specificare il nuovo codice, specificando se è locale o globale e se è abilitato o disabilitato.
3.  Rilasciare **l'interfaccia ISCardVerify.**

## <a name="members"></a>Membri

**L'interfaccia ISCardVerify** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardVerify** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ISCardVerify** include questi metodi.



| Metodo                                                        | Descrizione                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeCode**](iscardverify-changecode.md)                 | Modifica il codice CHV corrente.<br/>                                                                                                    |
| [**ResetSecurityState**](iscardverify-resetsecuritystate.md) | Reimposta il contesto [*di sicurezza dell'smart card.*](../secgloss/s-gly.md)<br/> |
| [**Sbloccare**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))                       | Abilita nuovamente il contesto [*di sicurezza*](../secgloss/s-gly.md).<br/>               |
| [**Verificare**](iscardverify-verify.md)                         | Autentica l'utente.<br/>                                                                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



 

 
