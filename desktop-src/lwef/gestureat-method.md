---
title: Metodo GestureAt
description: Metodo GestureAt
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c18c2a3913e8c9e805725f184bd5e969de6272ed05c562799805bd8c74256
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725721"
---
# <a name="gestureat-method"></a>Metodo GestureAt

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Riproduce l'animazione di inserimento per il carattere specificato nella posizione specificata.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Caratteri ("**_CharacterID_*_"). GestureAt_ *  *x,y*



| Parte  | Descrizione                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x,y* | Obbligatorio. Valore intero che indica la coordinata orizzontale (*x*) dello schermo e la coordinata verticale (*y*) dello schermo su cui il carattere gestirà. Queste coordinate devono essere specificate in pixel. |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Il server riproduce automaticamente l'animazione appropriata per il movimento verso la posizione specificata. Le coordinate sono sempre relative all'origine dello schermo (in alto a sinistra).

Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito [**un oggetto Request.**](/windows/desktop/lwef/the-request-object) Inoltre, se l'animazione associata non è stata caricata nel computer locale, il server imposta la proprietà [**Status**](status-property.md) dell'oggetto **Request** su "failed" con un numero di errore appropriato. Pertanto, se si usa il protocollo HTTP per accedere ai dati di animazione dei caratteri, usare il [**metodo Get**](get-method.md) per caricare le animazioni di stato **Gesturing** prima di chiamare il **metodo GestureAt.**

 

 