---
title: Interfaccia INapComponentConfig (NapCommon. h)
description: Fornisce i metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV).
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- NAP interfaccia INapComponentConfig
- Interfaccia NAP di INapComponentConfig, descrizione
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400490"
---
# <a name="inapcomponentconfig-interface"></a>Interfaccia INapComponentConfig

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapComponentConfig** fornisce i metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV).

> [!Note]  
> [**INapComponentConfig2**](inapcomponentconfig2.md) e [**INapComponentConfig3**](inapcomponentconfig3.md) ereditano tutti i metodi di questa interfaccia e devono essere usati in alternativa.

 

## <a name="members"></a>Membri

L'interfaccia **INapComponentConfig** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapComponentConfig** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapComponentConfig** dispone di questi metodi.



| Metodo                                                                          | Descrizione                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**INapComponentConfig:: GetConfig**](inapcomponentconfig-getconfig.md)         | Recupera la configurazione del componente di convalida integrità di sistema.<br/>                                |
| [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)           | Avvia l'interfaccia utente personalizzata per un componente di convalida integrità di sistema.<br/>              |
| [**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md) | Specifica se il componente di convalida integrità di sistema supporta un'interfaccia utente personalizzata.<br/> |
| [**INapComponentConfig:: Seconfig**](inapcomponentconfig-setconfig.md)         | Imposta la configurazione del componente di convalida integrità di sistema.<br/>                                     |



 

## <a name="remarks"></a>Commenti

Questa interfaccia non deve essere implementata dagli agenti di integrità del sistema (SHAs) o dai client di imposizione di quarantena (QeC).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

