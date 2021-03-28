---
description: 'Esistono due tipi di pennelli: logico e fisico.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: Informazioni sui pennelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130366"
---
# <a name="about-brushes"></a>Informazioni sui pennelli

Esistono due tipi di pennelli: logico e fisico. Un *pennello logico* è una descrizione della bitmap ideale utilizzata da un'applicazione per disegnare forme. Un *pennello fisico* è la bitmap effettiva creata da un driver di dispositivo in base alla definizione del pennello logico di un'applicazione. Per ulteriori informazioni sulle bitmap, vedere [bitmap](bitmaps.md).

Quando un'applicazione chiama una delle funzioni che creano un pennello, viene recuperato un handle che identifica un pennello logico. Quando l'applicazione passa questo handle alla funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) , il driver di dispositivo per la visualizzazione o la stampante corrispondente crea il pennello fisico.

Negli argomenti seguenti vengono descritti i pennelli:

-   [Origine pennello](brush-origin.md)
-   [Tipi di pennelli logici](logical-brush-types.md)
-   [Modello di trasferimento del blocco](pattern-block-transfer.md)
-   [Funzioni pennello abilitate per ICM](icm-enabled-brush-functions.md)

 

 



