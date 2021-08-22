---
title: Metodo MoveTo
description: Metodo MoveTo
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a245d389bc23d79d9f6cc105fec28ed14f5d511123c1dd113115ff69fc95c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609081"
---
# <a name="moveto-method"></a>Metodo MoveTo

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Sposta il carattere specificato nella posizione specificata.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). Velocità MoveTo_ *  *x,y* \[ \]



| Parte    | Descrizione                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x,y*   | Obbligatorio. Valore intero che indica il bordo sinistro (*x*) e il bordo superiore (*y*) del frame di animazione. Esprimere queste coordinate in pixel.                                                   |
| *Velocità* | facoltativo. Valore Long Integer che specifica in millisecondi la velocità di spostamento del frame del carattere. Il valore predefinito è 1000. Se si specifica zero (0), il fotogramma viene spostato senza riprodurre un'animazione. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il server riproduce automaticamente l'animazione appropriata assegnata agli **stati spostamento.** La posizione di un carattere è basata sull'angolo superiore sinistro della cornice.

Se si dichiara una variabile oggetto e la si imposta su questo metodo, viene restituito un [**oggetto Request.**](/windows/desktop/lwef/the-request-object) Inoltre, se l'animazione associata non è stata caricata nel computer locale, il server imposta la proprietà [**Status**](status-property.md) dell'oggetto **Request** su "failed" con un numero di errore appropriato. Pertanto, se si usa il protocollo HTTP per accedere ai dati di animazione o carattere, usare il [**metodo Get**](get-method.md) per caricare le animazioni dello stato **Moving** prima di chiamare il **metodo MoveTo.**

Anche se l'animazione non viene caricata, il server sposta comunque il frame.

> [!Note]  
> Se si chiama **MoveTo** con un valore diverso da zero prima che il carattere venga visualizzato, restituirà uno stato di errore se è stato assegnato un oggetto [**Request,**](/windows/desktop/lwef/the-request-object) perché il valore diverso da zero indica che si sta tentando di riprodurre un'animazione quando il carattere non è visibile.

 

> [!Note]  
> *L'effetto* effettivo del parametro Speed può variare in base alla velocità del processore del computer e alla priorità di altre attività in esecuzione nel sistema.

 

 

 