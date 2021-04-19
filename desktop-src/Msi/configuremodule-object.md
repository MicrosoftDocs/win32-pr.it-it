---
description: L'oggetto ConfigureModule è un'interfaccia implementata dal client.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Oggetto ConfigureModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332624"
---
# <a name="configuremodule-object"></a>Oggetto ConfigureModule

L' **oggetto ConfigureModule** è un'interfaccia implementata dal client. Mergemod.dllchiama i metodi sull'interfaccia **IMsmConfigureModule** per richiedere che lo strumento client fornisca informazioni di configurazione. Il modulo è configurato in base alle risposte del client alle chiamate su questa interfaccia.

## <a name="members"></a>Membri

L'oggetto **ConfigureModule** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'oggetto **ConfigureModule** dispone di questi metodi.



| Metodo                                                           | Descrizione                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**ProvideIntegerData**](configuremodule-provideintegerdata.md) | Chiamato da Mergemod.dll per ottenere numeri interi utilizzati per configurare il modulo.<br/> |
| [**ProvideTextData**](configuremodule-providetextdata.md)       | Chiamato da Mergemod.dll per ottenere il testo utilizzato per configurare il modulo.<br/>     |



 

## <a name="remarks"></a>Commenti

### <a name="c"></a>C++

interfaccia **IMsmConfigureModule: IDispatch**

### <a name="interface-id"></a>ID interfaccia



| Costante                     | Valore                                  |
|------------------------------|----------------------------------------|
| **\_IMSMCONFIGUREMODULE IID** | {AC013209-18A7-4851-8A21-2353443D70A0} |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




