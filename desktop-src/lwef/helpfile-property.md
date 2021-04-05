---
title: Proprietà filelima
description: Proprietà filelima
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710921"
---
# <a name="helpfile-property"></a>Proprietà filelima

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Restituisce o imposta il percorso e il nome file di un file della Guida sensibile al contesto di Microsoft Windows fornito dall'applicazione client.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente. ***Caratteri ("*** CharacterID * * *").* *  \[  =  *Nome file* fileguida\]



| Parte       | Descrizione                                                                    |
|------------|--------------------------------------------------------------------------------|
| *Filename* | Espressione stringa che specifica il percorso e il nome del file della Guida di Windows. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Se è stato creato un file della Guida di Windows per l'applicazione e si è impostata **la proprietà filecommand del carattere** , Agent chiama automaticamente la guida quando [**HelpModeOn**](helpmodeon-property.md) è impostato su **true** e l'utente fa clic sul carattere o seleziona un comando dal menu di scelta rapida. Se nella proprietà [**HelpContextID**](helpcontextid-property.md) del comando selezionato è stato specificato un numero di contesto, nella Guida viene visualizzato un argomento corrispondente al contesto della Guida corrente. in caso contrario, viene visualizzato "nessun argomento della Guida associato a questo elemento".

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

## <a name="see-also"></a>Vedere anche

[**Proprietà HelpModeOn**](helpmodeon-property.md), [ **proprietà HelpContextID**](helpcontextid-property.md)


 

 




