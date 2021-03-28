---
description: Consente il completamento dell'attività.
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
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233188"
---
# <a name="taskcompletionclient-interface"></a>Interfaccia TaskCompletionClient

Consente il completamento dell'attività.

## <a name="members"></a>Membri

L'interfaccia **TaskCompletionClient** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **TaskCompletionClient** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **TaskCompletionClient** dispone di questi metodi.



| Metodo                                                                    | Descrizione                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [**ApplyTaskCompletion**](taskcompletionclient-applytaskcompletion.md)   | Inizia il completamento dell'attività.<br/> |
| [**RevokeTaskCompletion**](taskcompletionclient-revoketaskcompletion.md) | Termina il completamento dell'attività.<br/>   |



 

## <a name="remarks"></a>Commenti

Il GUID per questa interfaccia è "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".

Questa API è deprecata e potrebbe non essere disponibile nelle versioni future di Windows. In alternativa, le app devono usare le API nello spazio dei nomi [**Windows. ApplicationModel. ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
