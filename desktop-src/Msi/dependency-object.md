---
description: L'oggetto Dependency restituisce un modulo da cui dipende il modulo corrente e che non è ancora stato unito al database di installazione corrente.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Oggetto Dependency (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dependency
- IMsmDependency
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: ac5786dcf3d4818fdfb3f0458cbfa85c923e5200ae69b5cb93d38330c322abf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378890"
---
# <a name="dependency-object"></a>Oggetto dependency

**L'oggetto Dependency** restituisce un modulo da cui dipende il modulo corrente e che non è ancora stato unito al database di installazione corrente.

## <a name="members"></a>Membri

**L'oggetto Dependency** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Dependency** ha queste proprietà.



| Proprietà                                           | Descrizione                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [**Lingua**](dependency-language.md)<br/> | Restituisce la lingua del modulo.<br/>           |
| [**Modulo**](dependency-module.md)<br/>     | Restituisce l'ID modulo del modulo richiesto.<br/> |
| [**Versione**](dependency-version.md)<br/>   | Restituisce la versione del modulo richiesto.<br/>   |



 

## <a name="c"></a>C++

interfaccia **IMsmDependency : IDispatch**

## <a name="interface-id"></a>ID interfaccia



| Costante                | Valore                                  |
|-------------------------|----------------------------------------|
| **IID \_ IMsmDependency** | {0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




