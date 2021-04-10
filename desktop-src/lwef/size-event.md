---
title: Evento dimensioni
description: Evento dimensioni
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855982"
---
# <a name="size-event"></a>Evento dimensioni

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando le dimensioni di un carattere cambiano.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

Dimensioni agente **secondario**  \_ **(ByVal** *CharacterID*, **ByVal** *Width*, **ByVal** *Height*)



| Parte          | Descrizione                                                         |
|---------------|---------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere spostato.                         |
| *Larghezza*       | Restituisce la nuova larghezza (in pixel) del fotogramma carattere come numero intero.  |
| *Altezza*      | Restituisce la nuova altezza (in pixel) del fotogramma di caratteri come valore integer. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento si verifica quando un'applicazione modifica la dimensione di un carattere. Questo evento viene inviato solo ai client del carattere, ovvero le applicazioni che hanno caricato il carattere.

### <a name="see-also"></a>Vedere anche

[**Sposta evento**](move-event.md)


 

 




