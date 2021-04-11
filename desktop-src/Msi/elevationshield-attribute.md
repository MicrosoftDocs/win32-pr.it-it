---
description: Questo attributo aggiunge l'icona di elevazione (UAC) del controllo dell'account utente (icona scudo) al controllo pulsante.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Attributo ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131790"
---
# <a name="elevationshield-attribute"></a>Attributo ElevationShield

Questo attributo aggiunge l'icona di elevazione (UAC) del [*controllo dell'account utente*](u-gly.md) (icona scudo) al [controllo pulsante](pushbutton-control.md).

Se questo bit è impostato e l'installazione non è ancora in esecuzione con privilegi [*elevati*](e-gly.md) , il controllo pulsante viene creato usando l'icona di elevazione del [*controllo dell'account utente*](u-gly.md) (UAC).

Se questo bit è impostato e l'installazione è già in esecuzione con privilegi [*elevati*](e-gly.md) , il controllo pulsante viene creato usando gli altri attributi dell'icona.

Se questo bit non è impostato, il controllo pulsante viene creato usando gli altri attributi dell'icona.

## <a name="valid-controls"></a>Controlli validi

[Pulsante](pushbutton-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                                  |
|---------|-------------|-------------------------------------------|
| 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

 

 



