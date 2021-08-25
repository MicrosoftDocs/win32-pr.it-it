---
title: Interfaccia INapComponentConfig3 (NapCommon.h)
description: Fornisce metodi di configurazione di sistema di Protezione accesso alla rete per i validator di integrità del sistema per impostare e modificare i dati di configurazione per un ID di configurazione specifico.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- Interfaccia INapComponentConfig3 NAP
- Interfaccia INapComponentConfig3 NAP, descritta
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea8ab7b42589fa548439b03c04ade56db498750ccd47841b806dcb6b506d3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803081"
---
# <a name="inapcomponentconfig3-interface"></a>Interfaccia INapComponentConfig3

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

**L'interfaccia INapComponentConfig3** fornisce metodi di configurazione di sistema di Protezione accesso alla rete per i validator dell'integrità del sistema per impostare e modificare i dati di configurazione per un ID di configurazione specifico.

> [!Note]  
> Questa interfaccia eredita tutti i metodi di [**INapComponentConfig2**](inapcomponentconfig2.md) e deve essere usata.

 

## <a name="members"></a>Membri

**L'interfaccia INapComponentConfig3** eredita da [**INapComponentConfig2.**](inapcomponentconfig2.md) **INapComponentConfig3** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia INapComponentConfig3** include questi metodi.



| Metodo                                                                                | Descrizione                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig3::D eleteAllConfig**](inapcomponentconfig3-deleteallconfig.md) | Implementato da SHV per fornire un modo per ripristinare lo stato originale dell'archivio SHV dopo l'installazione.<br/>      |
| [**INapComponentConfig3::D eleteConfig**](inapcomponentconfig3-deleteconfig.md)       | Implementato da SHV per fornire un modo per eliminare i dati di configurazione per un ID di configurazione specifico.<br/>  |
| [**INapComponentConfig3::GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md) | Implementato da SHV per fornire un modo per ottenere i dati di configurazione per un ID di configurazione specifico.<br/>  |
| [**INapComponentConfig3::NewConfig**](inapcomponentconfig3-newconfig.md)             | Implementato da SHV per fornire un modo per creare i dati di configurazione per un ID di configurazione specifico.<br/>  |
| [**INapComponentConfig3::SetConfigToID**](inapcomponentconfig3-setconfigtoid.md)     | Implementato da SHV per fornire un modo per impostare i dati di configurazione per un ID di configurazione specifico.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia non deve essere implementata dagli agenti di integrità del sistema (SHA) o dai client di imposizione della quarantena (QEC).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> <dt>

[Interfacce di Protezione accesso alla rete](nap-interfaces.md)
</dt> <dt>

[Informazioni di riferimento su Protezione accesso alla rete](nap-reference.md)
</dt> </dl>

 

 





