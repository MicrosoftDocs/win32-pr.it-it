---
title: Oggetto TaskVariables
description: Oggetto di script che definisce le variabili dell'attività che possono essere passate come parametri ai gestori di attività e ai file eseguibili esterni avviati dalle attività.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- Utilità di pianificazione oggetto TaskVariables
- Oggetto TaskVariables Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478352"
---
# <a name="taskvariables-object"></a>Oggetto TaskVariables

Oggetto di script che definisce le variabili dell'attività che possono essere passate come parametri ai gestori di attività e ai file eseguibili esterni avviati dalle attività.

## <a name="members"></a>Membri

L'oggetto **TaskVariables** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'oggetto **TaskVariables** dispone di questi metodi.



| Metodo                                         | Descrizione                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetContext**](taskvariables-getcontext.md) | Utilizzato per condividere il contesto tra diversi passaggi e attività che si trovano nella stessa istanza del processo.<br/> |
| [**GetInput**](taskvariables-getinput.md)     | Ottiene le variabili di input per un'attività.<br/>                                                           |
| [**SetOutput**](taskvariables-setoutput.md)   | Imposta le variabili di output per un'attività.<br/>                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





