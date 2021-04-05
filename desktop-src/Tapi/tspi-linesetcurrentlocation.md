---
description: Questa \_ funzione TSPI lineSetCurrentLocation è obsoleta. TAPI ha chiamato questa funzione quando l'utente (che usa la finestra di dialogo proprietà di composizione) o un'applicazione (usando la funzione lineSetCurrentLocation) ha modificato il percorso di conversione dell'indirizzo.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2361135770ac2d3900a902e0b7fa4fecad511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757004"
---
# <a name="tspi_linesetcurrentlocation"></a>\_LINESETCURRENTLOCATION TSPI

Questa \_ funzione TSPI lineSetCurrentLocation è obsoleta. TAPI ha chiamato questa funzione quando l'utente (che usa la finestra di dialogo **proprietà di composizione** ) o un'applicazione (usando la funzione [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) ) ha modificato il percorso di conversione dell'indirizzo.

Attualmente, una modifica nella posizione di traduzione genera un \_ messaggio line DEVSTATE con *dwParam1* impostato su LINEDEVSTATE \_ TRANSLATECHANGE.

 

 
