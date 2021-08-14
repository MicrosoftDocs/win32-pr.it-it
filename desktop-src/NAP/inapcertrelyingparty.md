---
title: Interfaccia INapCertRelyingParty (NapCertRelyingParty.h)
description: Le relying party del certificato devono usare per comunicare con NapAgent.
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- Interfaccia INapCertRelyingParty NAP
- Interfaccia INapCertRelyingParty NAP, descritta
topic_type:
- apiref
api_name:
- INapCertRelyingParty
api_location:
- NapCertRelyingParty.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d2a68c6ce910fa63588df1fa7bc1834f6ed537a2a2c9b85f24d383497a8d463
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368610"
---
# <a name="inapcertrelyingparty-interface"></a>Interfaccia INapCertRelyingParty

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**L'interfaccia INapCertRelyingParty** fornisce metodi che le relying party di certificato devono usare per comunicare con NapAgent.

## <a name="members"></a>Membri

**L'interfaccia INapCertRelyingParty** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapCertRelyingParty** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapCertRelyingParty** include questi metodi.



| Metodo                                                                                                        | Descrizione                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**INapCertRelyingParty::GetSubscribedRelyingParties**](inapcertrelyingparty-getsubscribedrelyingparties.md) | Ottiene un elenco di relying party sottoscritte.<br/>                 |
| [**INapCertRelyingParty::SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md)               | Sottoscrive un server di certificati di integrità (HCS) già registrato.<br/> |
| [**INapCertRelyingParty::UnSubscribeCertByGroup**](inapcertrelyingparty-unsubscribecertbygroup.md)           | Annulla la sottoscrizione a un server HCS.<br/>                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapCertRelyingParty.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCertRelyingParty.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

