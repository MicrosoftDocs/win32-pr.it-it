---
title: Evento Size
description: Evento Size
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146763c649ab22c59a8367e3135ee0ea277c8ae4c8e4bc58588cd70c0b5ec1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961021"
---
# <a name="size-event"></a>Evento Size

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Si verifica quando le dimensioni di un carattere cambiano.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

**Dimensioni**  \_ **dell'agente secondario (ByVal** *CharacterID,* **ByVal** *Width,* **ByVal** *Height*)



| Parte          | Descrizione                                                         |
|---------------|---------------------------------------------------------------------|
| *CharacterID* | Restituisce l'ID del carattere spostato.                         |
| *Larghezza*       | Restituisce la nuova larghezza (in pixel) del frame di caratteri come numero intero.  |
| *Altezza*      | Restituisce la nuova altezza (in pixel) del frame di caratteri come numero intero. |



 

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo evento si verifica quando un'applicazione modifica le dimensioni di un carattere. Questo evento viene inviato solo ai client del carattere (applicazioni che hanno caricato il carattere).

### <a name="see-also"></a>Vedere anche

[**Evento Move**](move-event.md)


 

 




