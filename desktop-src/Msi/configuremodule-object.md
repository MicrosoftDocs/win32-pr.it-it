---
description: L'oggetto ConfigureModule è un'interfaccia implementata dal client.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Oggetto ConfigureModule (Mergemod.h)
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
ms.openlocfilehash: 7685ce1f1c9c7d8f519395c578000375742eea49dd169085e99c582e14c35a29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143712"
---
# <a name="configuremodule-object"></a>Oggetto ConfigureModule

**L'oggetto ConfigureModule** è un'interfaccia implementata dal client. Mergemod.dllchiama metodi **sull'interfaccia IMsmConfigureModule** per richiedere che lo strumento client fornica informazioni di configurazione. Il modulo viene configurato in base alle risposte del client alle chiamate su questa interfaccia.

## <a name="members"></a>Membri

**L'oggetto ConfigureModule** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'oggetto ConfigureModule** dispone di questi metodi.



| Metodo                                                           | Descrizione                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**ProvideIntegerData**](configuremodule-provideintegerdata.md) | Chiamato da Mergemod.dll ottenere numeri interi usati per configurare il modulo.<br/> |
| [**ProvideTextData**](configuremodule-providetextdata.md)       | Chiamato da Mergemod.dll ottenere il testo usato per configurare il modulo.<br/>     |



 

## <a name="remarks"></a>Commenti

### <a name="c"></a>C++

interfaccia **IMsmConfigureModule : IDispatch**

### <a name="interface-id"></a>ID interfaccia



| Costante                     | Valore                                  |
|------------------------------|----------------------------------------|
| **IID \_ IMsmConfigureModule** | {AC013209-18A7-4851-8A21-2353443D70A0} |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




