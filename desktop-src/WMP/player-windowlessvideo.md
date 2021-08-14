---
title: Player.windowlessVideo
description: La proprietà windowlessVideo specifica o recupera un valore che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra.
ms.assetid: 314a75a3-d096-4cd4-a747-e31367e0e265
keywords:
- Player.windowlessVideo Windows Media Player
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
ms.openlocfilehash: 733f8488d1d45f4c7e9794e64e2b3a70b41722048eac82d5d8eb6eb2f1d91cd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572078"
---
# <a name="playerwindowlessvideo"></a>Player.windowlessVideo

La **proprietà windowlessVideo** specifica o recupera un valore che indica se il controllo Windows Media Player esegue il rendering del video in modalità senza finestra.

## <a name="syntax"></a>Sintassi

*lettore*. **windowlessVideo**

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **valore booleano** specificato in fase di progettazione e successivamente di sola lettura.



| Valore | Descrizione                                      |
|-------|--------------------------------------------------|
| true  | Il rendering del video viene eseguito in modalità senza finestra.        |
| false | Valore predefinito. Il rendering del video viene eseguito in modalità finestra. |



 

## <a name="remarks"></a>Commenti

Per impostazione predefinita, un controllo Windows Media Player incorporato esegue il rendering del video nella relativa finestra all'interno dell'area client. Quando **windowlessVideo** è impostato su true, il controllo Player esegue il rendering del video direttamente nell'area client, in modo che sia possibile applicare effetti speciali o applicare un livello al video con testo.

In Windows Vista il rendering di video in modalità senza finestra può ridurre le prestazioni.

La **proprietà windowlessVideo** non è supportata per Netscape Navigator. L'impostazione di un valore per questa proprietà nello strumento di navigazione può produrre risultati imprevisti.

**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player per Windows XP o versioni successive.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



 

 





