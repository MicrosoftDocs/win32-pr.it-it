---
title: Interfaccia INapComponentConfig (NapCommon.h)
description: Fornisce metodi di configurazione di sistema di Protezione accesso alla rete per i validator dell'integrità del sistema.
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- Interfaccia INapComponentConfig NAP
- Interfaccia INapComponentConfig NAP, descritta
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
ms.openlocfilehash: 3d0a1c61b3681178089b0cda813155f3629caa233a7995d28cee22b1f65754ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800023"
---
# <a name="inapcomponentconfig-interface"></a>Interfaccia INapComponentConfig

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**L'interfaccia INapComponentConfig fornisce** metodi di configurazione di sistema di Protezione accesso alla rete per i validator di integrità del sistema.

> [!Note]  
> [**INapComponentConfig2**](inapcomponentconfig2.md) e [**INapComponentConfig3**](inapcomponentconfig3.md) ereditano tutti i metodi di questa interfaccia e devono essere usati.

 

## <a name="members"></a>Membri

**L'interfaccia INapComponentConfig** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **INapComponentConfig** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapComponentConfig** include questi metodi.



| Metodo                                                                          | Descrizione                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md)         | Recupera la configurazione del componente SHV.<br/>                                |
| [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)           | Avvia l'interfaccia utente personalizzata per un componente SHV.<br/>              |
| [**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md) | Specifica se il componente SHV supporta un'interfaccia utente personalizzata.<br/> |
| [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)         | Imposta la configurazione del componente SHV.<br/>                                     |



 

## <a name="remarks"></a>Commenti

Questa interfaccia non deve essere implementata dagli agenti di integrità del sistema (SHA) o dai client di imposizione della quarantena (QEC).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

