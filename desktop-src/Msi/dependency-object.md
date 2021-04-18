---
description: L'oggetto Dependency restituisce un modulo dal quale dipende il modulo corrente e che non è ancora stato unito al database di installazione corrente.
ms.assetid: 3157f07d-99de-4628-9b03-eb86eb4896a4
title: Oggetto Dependency (Mergemod. h)
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
ms.openlocfilehash: 24b215b67d22d27639f3e002590e7d08dd54b0c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328775"
---
# <a name="dependency-object"></a>Oggetto Dependency

L'oggetto **Dependency** restituisce un modulo dal quale dipende il modulo corrente e che non è ancora stato unito al database di installazione corrente.

## <a name="members"></a>Membri

L'oggetto di **dipendenza** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto di **dipendenza** dispone di queste proprietà.



| Proprietà                                           | Descrizione                                             |
|:---------------------------------------------------|:--------------------------------------------------------|
| [**Lingua**](dependency-language.md)<br/> | Restituisce la lingua del modulo.<br/>           |
| [**Modulo**](dependency-module.md)<br/>     | Restituisce l'ID del modulo richiesto.<br/> |
| [**Versione**](dependency-version.md)<br/>   | Restituisce la versione del modulo richiesto.<br/>   |



 

## <a name="c"></a>C++

interfaccia **IMsmDependency: IDispatch**

## <a name="interface-id"></a>ID interfaccia



| Costante                | Valore                                  |
|-------------------------|----------------------------------------|
| **\_IMSMDEPENDENCY IID** | {0ADDA82D-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




