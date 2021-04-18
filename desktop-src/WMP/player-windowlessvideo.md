---
title: Player. windowlessVideo
description: La proprietà windowlessVideo specifica o recupera un valore che indica se il controllo di Windows Media Player esegue il rendering del video in modalità senza finestra.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Player. windowlessVideo Windows Media Player
topic_type:
- apiref
api_name:
- Player.windowlessVideo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93f4a8a2b70a42cd0893d463eccca0427dde6c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327054"
---
# <a name="playerwindowlessvideo"></a>Player. windowlessVideo

La proprietà **windowlessVideo** specifica o recupera un valore che indica se il controllo di Windows Media Player esegue il rendering del video in modalità senza finestra.

## <a name="syntax"></a>Sintassi

*Player*. **windowlessVideo**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **valore booleano** che viene specificato in fase di progettazione ed è successivamente di sola lettura.



| Valore | Descrizione                                      |
|-------|--------------------------------------------------|
| true  | Il video viene sottoposto a rendering in modalità senza finestra.        |
| false | Valore predefinito. Il video viene sottoposto a rendering in modalità finestra. |



 

## <a name="remarks"></a>Commenti

Per impostazione predefinita, un controllo di Windows Media Player incorporato esegue il rendering dei video nella propria finestra all'interno dell'area client. Quando **windowlessVideo** è impostato su true, il controllo Player esegue il rendering del video direttamente nell'area client, in modo che sia possibile applicare effetti speciali o sovrapporre il video con il testo.

In Windows Vista, il rendering di video in modalità senza finestra può compromettere le prestazioni.

La proprietà **windowlessVideo** non è supportata per il navigatore Netscape. L'impostazione di un valore per questa proprietà in Navigator può produrre risultati imprevisti.

**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versione successiva.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



 

 





