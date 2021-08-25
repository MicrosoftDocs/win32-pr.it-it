---
description: Abilita il completamento dell'attività.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Interfaccia TaskCompletionClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: d03e52a15e6689b7f1ea98a2f1021874cab6a8967dd148b7eaf685ff3984e8cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773651"
---
# <a name="taskcompletionclient-interface"></a>Interfaccia TaskCompletionClient

Abilita il completamento dell'attività.

## <a name="members"></a>Membri

**L'interfaccia TaskCompletionClient** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **TaskCompletionClient** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia TaskCompletionClient** include questi metodi.



| Metodo                                                                    | Descrizione                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [**ApplyTaskCompletion**](taskcompletionclient-applytaskcompletion.md)   | Avvia il completamento dell'attività.<br/> |
| [**RevokeTaskCompletion**](taskcompletionclient-revoketaskcompletion.md) | Termina il completamento dell'attività.<br/>   |



 

## <a name="remarks"></a>Commenti

Il GUID per questa interfaccia è "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".

Questa API è deprecata e potrebbe non essere disponibile nelle versioni future di Windows. Le app devono usare le API nel [**Windows. Spazio dei nomi ApplicationModel.ExtendedExecution.**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
