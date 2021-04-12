---
title: Metodo GestureAt
description: Metodo GestureAt
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472803"
---
# <a name="gestureat-method"></a>Metodo GestureAt

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Riproduce l'animazione gestuale per il carattere specificato nella posizione specificata.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agente ***. Caratteri ("*** CharacterID * * *"). GestureAt* *  *x, y*



| Parte  | Descrizione                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y* | Obbligatorio. Valore intero che indica la coordinata orizzontale (*x*) dello schermo e la coordinata verticale (*y*) dello schermo a cui il carattere gestirà. È necessario specificare queste coordinate in pixel. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il server esegue automaticamente l'animazione appropriata per eseguire un movimento verso la posizione specificata. Le coordinate sono sempre relative all'origine dello schermo (in alto a sinistra).

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) . Inoltre, se l'animazione associata non è stata caricata nel computer locale, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **richiesta** su "failed" con un numero di errore appropriato. Se pertanto si utilizza il protocollo HTTP per accedere ai dati di animazione di tipo carattere, utilizzare il metodo [**Get**](get-method.md) per caricare le animazioni dello stato **gestuale** prima di chiamare il metodo **GestureAt** .

 

 