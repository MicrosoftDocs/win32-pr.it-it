---
title: Interfaccia INapCertRelyingParty (NapCertRelyingParty. h)
description: 'Certificato: le relying party devono usare per comunicare con NapAgent.'
ms.assetid: e5ae0f4d-24fa-4049-82d9-1c9baeb34e32
keywords:
- NAP interfaccia INapCertRelyingParty
- Interfaccia NAP di INapCertRelyingParty, descrizione
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
ms.openlocfilehash: 85b4439389c6ee65076f710bb6ea752c73a51ecd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048535"
---
# <a name="inapcertrelyingparty-interface"></a>Interfaccia INapCertRelyingParty

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapCertRelyingParty** fornisce i metodi che devono essere usati dai relying party per comunicare con napagent.

## <a name="members"></a>Membri

L'interfaccia **INapCertRelyingParty** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapCertRelyingParty** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapCertRelyingParty** dispone di questi metodi.



| Metodo                                                                                                        | Descrizione                                                                     |
|:--------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**INapCertRelyingParty::GetSubscribedRelyingParties**](inapcertrelyingparty-getsubscribedrelyingparties.md) | Ottiene un elenco di relying party che hanno sottoscritto.<br/>                 |
| [**INapCertRelyingParty::SubscribeCertByGroup**](inapcertrelyingparty-subscribecertbygroup.md)               | Sottoscrive un server di certificati di integrità già registrato (HCS).<br/> |
| [**INapCertRelyingParty::UnSubscribeCertByGroup**](inapcertrelyingparty-unsubscribecertbygroup.md)           | Annulla la sottoscrizione da un server HCS.<br/>                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapCertRelyingParty. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCertRelyingParty. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

