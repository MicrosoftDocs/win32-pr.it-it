---
title: Interfaccia INapComponentInfo (NapCommon. h)
description: Fornisce metodi che i componenti plug-in, ad esempio SHAs e SHV, devono implementare affinché il sistema NAP comunichi con loro.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- NAP interfaccia INapComponentInfo
- Interfaccia NAP di INapComponentInfo, descrizione
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
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964012"
---
# <a name="inapcomponentinfo-interface"></a>Interfaccia INapComponentInfo

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapComponentInfo** fornisce metodi che i componenti plug-in, ad esempio Shas e SHV, devono implementare affinché il sistema NAP comunichi con loro. Il sistema NAP chiama l'implementazione di questi metodi per recuperare le informazioni amministrative statiche, ad esempio nome descrittivo o stringhe localizzate.

## <a name="members"></a>Membri

L'interfaccia **INapComponentInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapComponentInfo** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapComponentInfo** dispone di questi metodi.



| Metodo                                                                                                         | Descrizione                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**INapComponentInfo::ConvertErrorCodeToMessageId**](inapcomponentinfo-converterrorcodetomessageid-method.md) | Utilizzato dal sistema NAP per richiedere che il client di integrità converta un codice di errore HRESULT in un ID messaggio.<br/> |
| [**INapComponentInfo:: GetDescription**](inapcomponentinfo-getdescription-method.md)                           | Utilizzato dal sistema NAP per ottenere la descrizione di un client di integrità.<br/>                                  |
| [**INapComponentInfo:: GetFriendlyName**](inapcomponentinfo-getfriendlyname-method.md)                         | Utilizzato dal sistema NAP per ottenere il nome descrittivo di un client di integrità.<br/>                                |
| [**INapComponentInfo:: GetIcon**](inapcomponentinfo-geticon-method.md)                                         | Utilizzato dal sistema NAP per ottenere l'icona di un client di integrità.<br/>                                         |
| [**INapComponentInfo:: GetLocalizedString**](inapcomponentinfo-getlocalizedstring-method.md)                   | Utilizzato dal sistema NAP per ottenere le stringhe localizzate.<br/>                                                   |
| [**INapComponentInfo:: getvendorname**](inapcomponentinfo-getvendorname-method.md)                             | Utilizzato dal sistema NAP per ottenere il nome del fornitore di un client di integrità.<br/>                                  |
| [**INapComponentInfo:: GetVersion**](inapcomponentinfo-getversion-method.md)                                   | Utilizzato dal sistema NAP per ottenere la versione di un client di integrità.<br/>                                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

