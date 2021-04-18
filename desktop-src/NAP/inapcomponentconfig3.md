---
title: Interfaccia INapComponentConfig3 (NapCommon. h)
description: Fornisce metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV) per impostare e modificare i dati di configurazione per un ID configurazione specifico.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- NAP interfaccia INapComponentConfig3
- Interfaccia NAP di INapComponentConfig3, descrizione
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
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301068"
---
# <a name="inapcomponentconfig3-interface"></a>Interfaccia INapComponentConfig3

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapComponentConfig3** fornisce metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV) per impostare e modificare i dati di configurazione per un ID configurazione specifico.

> [!Note]  
> Questa interfaccia eredita tutti i metodi di [**INapComponentConfig2**](inapcomponentconfig2.md) e deve essere usata in alternativa.

 

## <a name="members"></a>Membri

L'interfaccia **INapComponentConfig3** eredita da [**INapComponentConfig2**](inapcomponentconfig2.md). **INapComponentConfig3** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapComponentConfig3** dispone di questi metodi.



| Metodo                                                                                | Descrizione                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig3::D eleteAllConfig**](inapcomponentconfig3-deleteallconfig.md) | Implementata da SHV per fornire un modo per reimpostare l'archivio di convalida integrità di sistema sullo stato originale dopo l'installazione.<br/>      |
| [**INapComponentConfig3::D eleteConfig**](inapcomponentconfig3-deleteconfig.md)       | Implementato da SHV per fornire un modo per eliminare i dati di configurazione per un ID configurazione specifico.<br/>  |
| [**INapComponentConfig3::GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md) | Implementato da SHV per fornire un modo per ottenere i dati di configurazione per un ID configurazione specifico.<br/>  |
| [**INapComponentConfig3:: NewConfig**](inapcomponentconfig3-newconfig.md)             | Implementato da SHV per fornire un modo per creare i dati di configurazione per un ID configurazione specifico.<br/>  |
| [**INapComponentConfig3::SetConfigToID**](inapcomponentconfig3-setconfigtoid.md)     | Implementato da SHV per fornire un modo per impostare i dati di configurazione per un ID configurazione specifico.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia non deve essere implementata dagli agenti di integrità del sistema (SHAs) o dai client di imposizione di quarantena (QeC).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

 





