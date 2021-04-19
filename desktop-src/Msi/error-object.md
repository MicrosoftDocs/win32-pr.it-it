---
description: L'oggetto Error restituisce le informazioni di un singolo errore di merge.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Oggetto Error (Mergemod. h)
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
ms.openlocfilehash: 36fce310e6f75889ba5092f4fe43b6ca52ee2963
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326381"
---
# <a name="error-object"></a>Oggetto errore

L'oggetto **Error** restituisce le informazioni di un singolo errore di merge.

## <a name="members"></a>Membri

L'oggetto **Error** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **Error** dispone di queste proprietà.



| Proprietà                                                | Descrizione                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**DatabaseKeys**](error-databasekeys.md)<br/>   | Restituisce le chiavi primarie della riga nella tabella di database che ha causato l'errore.<br/> |
| [**DatabaseTable**](error-databasetable.md)<br/> | Restituisce il nome della tabella del database che ha causato l'errore.<br/>           |
| [**Linguaggio**](error-language.md)<br/>           | Restituisce la lingua dell'errore.<br/>                                                |
| [**ModuleKeys**](error-modulekeys.md)<br/>       | Restituisce le chiavi primarie della riga nella tabella dei moduli che hanno causato l'errore.<br/>   |
| [**ModuleTable**](error-moduletable.md)<br/>     | Restituisce il nome della tabella del modulo che ha causato l'errore.<br/>             |
| [**Percorso**](error-path.md)<br/>                   | Restituisce il percorso del file o della directory che ha causato l'errore. Attualmente non usato.<br/>    |
| [**Tipo**](error-type.md)<br/>                   | Restituisce il tipo di errore.<br/>                                                        |



 

## <a name="c"></a>C++

interfaccia **IMsmError: IDispatch**

## <a name="interface-id"></a>ID interfaccia



| Costante           | Valore                                  |
|--------------------|----------------------------------------|
| **\_IMSMERROR IID** | {0ADDA828-2C26-11D2-AD65-00A0C9AF11A6} |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




