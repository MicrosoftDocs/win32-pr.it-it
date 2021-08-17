---
description: L'oggetto Error restituisce le informazioni di un singolo errore di unione.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Oggetto Error (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 237cf88b2830bf210e84d016b52b7fd0b0183c0c0072ac8f654663e2cd3c12dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947032"
---
# <a name="error-object"></a>Oggetto errore

**L'oggetto Error** restituisce le informazioni di un singolo errore di unione.

## <a name="members"></a>Membri

**L'oggetto Error** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto Error** ha queste proprietà.



| Proprietà                                                | Descrizione                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**DatabaseKeys**](error-databasekeys.md)<br/>   | Restituisce le chiavi primarie della riga nella tabella di database che ha causato l'errore.<br/> |
| [**Oggetto DatabaseTable**](error-databasetable.md)<br/> | Restituisce il nome della tabella nel database che causa l'errore.<br/>           |
| [**Linguaggio**](error-language.md)<br/>           | Restituisce la lingua dell'errore.<br/>                                                |
| [**ModuleKeys**](error-modulekeys.md)<br/>       | Restituisce le chiavi primarie della riga nella tabella del modulo che ha causato l'errore.<br/>   |
| [**ModuleTable**](error-moduletable.md)<br/>     | Restituisce il nome della tabella nel modulo che causa l'errore.<br/>             |
| [**Percorso**](error-path.md)<br/>                   | Restituire il percorso del file o della directory che causa l'errore. Attualmente inutilizzato.<br/>    |
| [**Tipo**](error-type.md)<br/>                   | Restituisce il tipo di errore.<br/>                                                        |



 

## <a name="c"></a>C++

interfaccia **IMsmError : IDispatch**

## <a name="interface-id"></a>ID interfaccia



| Costante           | Valore                                  |
|--------------------|----------------------------------------|
| **IID \_ IMsmError** | {0ADDA828-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




