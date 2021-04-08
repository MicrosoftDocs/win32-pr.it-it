---
title: Interfaccia INapClientManagement2 (NapManagement. h)
description: Fornisce metodi per la gestione client di protezione accesso alla rete. | Interfaccia INapClientManagement2 (NapManagement. h)
ms.assetid: 3cf29bfe-471a-481a-903d-bf0479c57a08
keywords:
- NAP interfaccia INapClientManagement2
- Interfaccia NAP di INapClientManagement2, descrizione
topic_type:
- apiref
api_name:
- INapClientManagement2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3441b52ddf776337765f39d23528bc223a17b1e4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058560"
---
# <a name="inapclientmanagement2-interface"></a>Interfaccia INapClientManagement2

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'interfaccia **INapClientManagement2** fornisce metodi per la gestione client di protezione accesso alla rete.

> [!Note]  
> Questa interfaccia eredita tutti i metodi di [**INapClientManagement**](inapclientmanagement.md) e deve essere usata in alternativa.

 

## <a name="members"></a>Membri

L'interfaccia **INapClientManagement2** eredita da [**INapClientManagement**](inapclientmanagement.md). **INapClientManagement2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **INapClientManagement2** dispone di questi metodi.



| Metodo                                                                                                    | Descrizione                                                                                                |
|:----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**INapClientManagement2::GetSystemIsolationInfoEx**](inapclientmanagement2-getsystemisolationinfoex.md) | Recupera le informazioni sullo stato di isolamento e sullo stato di isolamento esteso del client di protezione accesso alla rete.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> <dt>

[Interfacce NAP](nap-interfaces.md)
</dt> <dt>

[Riferimento NAP](nap-reference.md)
</dt> </dl>

 

 





