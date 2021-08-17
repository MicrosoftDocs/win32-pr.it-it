---
title: Interfaccia INapComponentInfo (NapCommon.h)
description: Fornisce metodi che i componenti plug-in, ad esempio SHA e SHV, devono implementare per la comunicazione con il sistema di Protezione accesso alla rete.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- Interfaccia INapComponentInfo NAP
- Interfaccia INapComponentInfo NAP, descritta
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b188aae04ab407c5ae26e1d1a764e9093cc101cbe7d714ef8a8e0146013fefee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799706"
---
# <a name="inapcomponentinfo-interface"></a>Interfaccia INapComponentInfo

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**L'interfaccia INapComponentInfo** fornisce metodi che i componenti plug-in, ad esempio SHA e SHV, devono implementare per comunicare con il sistema nap. Il sistema di Protezione accesso alla rete chiama l'implementazione di questi metodi per recuperare informazioni amministrative statiche, ad esempio nome descrittivo o stringhe localizzate.

## <a name="members"></a>Membri

**L'interfaccia INapComponentInfo** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapComponentInfo** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapComponentInfo** include questi metodi.



| Metodo                                                                                                         | Descrizione                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**INapComponentInfo::ConvertErrorCodeToMessageId**](inapcomponentinfo-converterrorcodetomessageid-method.md) | Utilizzato dal sistema di Protezione accesso alla rete per richiedere al client di integrità di convertire un codice di errore HRESULT in un ID messaggio.<br/> |
| [**INapComponentInfo::GetDescription**](inapcomponentinfo-getdescription-method.md)                           | Utilizzato dal sistema protezione accesso alla rete per ottenere la descrizione di un client di integrità.<br/>                                  |
| [**INapComponentInfo::GetFriendlyName**](inapcomponentinfo-getfriendlyname-method.md)                         | Utilizzato dal sistema di Protezione accesso alla rete per ottenere il nome descrittivo di un client di integrità.<br/>                                |
| [**INapComponentInfo::GetIcon**](inapcomponentinfo-geticon-method.md)                                         | Utilizzato dal sistema di Protezione accesso alla rete per ottenere l'icona di un client di integrità.<br/>                                         |
| [**INapComponentInfo::GetLocalizedString**](inapcomponentinfo-getlocalizedstring-method.md)                   | Utilizzato dal sistema di Protezione accesso alla rete per ottenere le stringhe localizzate.<br/>                                                   |
| [**INapComponentInfo::GetVendorName**](inapcomponentinfo-getvendorname-method.md)                             | Utilizzato dal sistema di Protezione accesso alla rete per ottenere il nome del fornitore di un client di integrità.<br/>                                  |
| [**INapComponentInfo::GetVersion**](inapcomponentinfo-getversion-method.md)                                   | Utilizzato dal sistema di Protezione accesso alla rete per ottenere la versione di un client di integrità.<br/>                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

