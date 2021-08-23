---
description: La definizione dell'interfaccia ISCardAuth viene fornita come standard che può essere seguita durante lo sviluppo di smart card provider di servizi. L'interfaccia ISCardAuth può essere usata per esporre i servizi di autenticazione supportati da un smart card.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: Interfaccia ISCardAuth
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 55f92b06fb9c86c46ee0f9bf08350510ba4e6f897a95294a15265df7918de516
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577851"
---
# <a name="iscardauth-interface"></a>Interfaccia ISCardAuth

\[**L'interfaccia ISCardAuth** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

La **definizione dell'interfaccia ISCardAuth** viene fornita come standard che può essere seguita quando si sviluppa [*smart card*](../secgloss/s-gly.md) provider [*di servizi.*](../secgloss/c-gly.md)

**L'interfaccia ISCardAuth** può essere usata per esporre i servizi di autenticazione supportati da un smart card. Questi servizi includono l'autenticazione dell'applicazione, smart card e l'autenticazione utente.

L'esempio seguente illustra un uso tipico **dell'interfaccia ISCardAuth.**

**Per usare ISCardAuth**

1.  Creare **un'interfaccia ISCardAuth** (tramite il metodo di [**interfaccia ISCardManage**](iscardmanage.md) corrispondente).
2.  Chiamare il metodo **ISCardAuth** appropriato ([**APP \_ Auth**](iscardauth-app-auth.md), [**GetChallenge**](iscardauth-getchallenge.md), [**ICC \_ Auth**](iscardauth-icc-auth.md)o [**User \_ Auth**](iscardauth-user-auth.md)).
3.  Rilasciare **l'interfaccia ISCardAuth.**

## <a name="members"></a>Membri

**L'interfaccia ISCardAuth** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardAuth** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ISCardAuth** include questi metodi.



| Metodo                                          | Descrizione                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Autenticazione \_ APP**](iscardauth-app-auth.md)        | Consente all'applicazione di autenticarsi usando un protocollo di verifica/firma.<br/> |
| [**GetChallenge**](iscardauth-getchallenge.md) | Restituisce una richiesta di smart card.<br/>                                            |
| [**Autenticazione \_ ICC**](iscardauth-icc-auth.md)        | Consente a un'applicazione di autenticare il smart card.<br/>                               |
| [**Autenticazione \_ utente**](iscardauth-user-auth.md)      | Consente l'accesso ai servizi di autenticazione utente.<br/>                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



 

 
