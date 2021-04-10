---
title: MoveTo (metodo)
description: MoveTo (metodo)
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6a7f215de9ea6e323870ec7e10967462ab4174
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046745"
---
# <a name="moveto-method"></a>MoveTo (metodo)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Sposta il carattere specificato nella posizione specificata.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). MoveTo* *  *x, y* \[ *velocità*\]



| Parte    | Descrizione                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y*   | Obbligatorio. Valore intero che indica il bordo sinistro (*x*) e il bordo superiore (*y*) del frame di animazione. Esprimere queste coordinate in pixel.                                                   |
| *Velocità* | facoltativo. Valore long integer che specifica in millisecondi la velocità con cui il frame del carattere viene spostato. Il valore predefinito è 1000. Se si specifica zero (0), il frame viene spostato senza riprodurre un'animazione. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il server esegue automaticamente l'animazione appropriata assegnata agli Stati di **trasferimento** . La posizione di un carattere è basata sull'angolo superiore sinistro del frame.

Se si dichiara una variabile oggetto e la si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) . Inoltre, se l'animazione associata non è stata caricata nel computer locale, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **richiesta** su "failed" con un numero di errore appropriato. Se pertanto si utilizza il protocollo HTTP per accedere ai dati di tipo carattere o di animazione, utilizzare il metodo [**Get**](get-method.md) per caricare le animazioni dello stato di **trasferimento** prima di chiamare il metodo **MoveTo** .

Anche se l'animazione non è caricata, il server sposta ancora il frame.

> [!Note]  
> Se si chiama **MoveTo** con un valore diverso da zero prima che il carattere venga visualizzato, viene restituito uno stato di errore se è stato assegnato un oggetto [**Request**](/windows/desktop/lwef/the-request-object) , perché il valore diverso da zero indica che si sta provando a riprodurre un'animazione quando il carattere non è visibile.

 

> [!Note]  
> L'effetto effettivo del parametro *Speed* può variare in base alla velocità del processore del computer e alla priorità di altre attività in esecuzione nel sistema.

 

 

 