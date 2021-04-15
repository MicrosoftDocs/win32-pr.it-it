---
description: La definizione dell'interfaccia ISCardAuth viene fornita come standard che può essere seguita durante lo sviluppo di un provider di servizi per smart card. L'interfaccia ISCardAuth può essere usata per esporre i servizi di autenticazione supportati da una smart card.
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
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484724"
---
# <a name="iscardauth-interface"></a>Interfaccia ISCardAuth

\[L'interfaccia **ISCardAuth** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

La definizione dell'interfaccia **ISCardAuth** viene fornita come standard che può essere seguita durante lo sviluppo di un [*provider di servizi*](../secgloss/c-gly.md)per [*Smart Card*](../secgloss/s-gly.md) .

L'interfaccia **ISCardAuth** può essere usata per esporre i servizi di autenticazione supportati da una smart card. Questi servizi includono l'autenticazione dell'applicazione, l'autenticazione con smart card e l'autenticazione utente.

Nell'esempio seguente viene illustrato un utilizzo tipico dell'interfaccia **ISCardAuth** .

**Per usare ISCardAuth**

1.  Creare un'interfaccia **ISCardAuth** (tramite il metodo di interfaccia [**ISCardManage**](iscardmanage.md) corrispondente).
2.  Chiamare il metodo **ISCardAuth** appropriato ([**\_ autenticazione app**](iscardauth-app-auth.md), [**getchallenge**](iscardauth-getchallenge.md), [**CPI \_ AUTH**](iscardauth-icc-auth.md)o [**\_ autenticazione utente**](iscardauth-user-auth.md)).
3.  Rilasciare l'interfaccia **ISCardAuth** .

## <a name="members"></a>Membri

L'interfaccia **ISCardAuth** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardAuth** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISCardAuth** dispone di questi metodi.



| Metodo                                          | Descrizione                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Autenticazione dell'APP \_**](iscardauth-app-auth.md)        | Consente all'applicazione di eseguire l'autenticazione usando un protocollo di verifica/firma.<br/> |
| [**Getchallenge**](iscardauth-getchallenge.md) | Restituisce una richiesta di verifica dalla smart card.<br/>                                            |
| [**\_Autenticazione ICC**](iscardauth-icc-auth.md)        | Consente a un'applicazione di autenticare la smart card.<br/>                               |
| [**\_Autenticazione utente**](iscardauth-user-auth.md)      | Consente l'accesso ai servizi di autenticazione utente.<br/>                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/> |
| Fine del supporto client<br/>    | Windows XP<br/>                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                       |



 

 
