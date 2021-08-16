---
description: Questo attributo aggiunge l'icona di elevazione del controllo dell'account utente (icona dello schermo) al controllo PushButton.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Attributo ElevationShield
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4c5da7133a7216386be56328c0e21e2e365129caa185e045984cb5e89b7d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637491"
---
# <a name="elevationshield-attribute"></a>Attributo ElevationShield

Questo attributo aggiunge [*l'icona di elevazione del*](u-gly.md) controllo dell'account utente (icona dello schermo) al [controllo PushButton](pushbutton-control.md).

Se questo bit è impostato e l'installazione non è ancora in esecuzione con privilegi elevati, il controllo pulsante di scelta rapida viene creato usando l'icona di elevazione del controllo dell'account utente [*(icona*](u-gly.md) di schermatura). [](e-gly.md)

Se questo bit è impostato e l'installazione è già in esecuzione con privilegi elevati, il controllo pushbutton viene creato usando gli altri attributi dell'icona. [](e-gly.md)

Se questo bit non è impostato, il controllo pushbutton viene creato usando gli altri attributi dell'icona.

## <a name="valid-controls"></a>Controlli validi

[Pulsante](pushbutton-control.md)

## <a name="value"></a>Valore



| Decimal | Valore esadecimale | Costante                                  |
|---------|-------------|-------------------------------------------|
| 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

 

 



