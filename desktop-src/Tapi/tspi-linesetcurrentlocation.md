---
description: Questa funzione \_ lineSetCurrentLocation TSPI è obsoleta. TAPI ha chiamato questa funzione quando l'utente (usando la finestra di dialogo Proprietà di composizione) o un'applicazione (usando la funzione lineSetCurrentLocation) ha modificato il percorso di conversione degli indirizzi.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa78427bc4892fd0460b60bcb90f5fef43a38f002368c7ca7251cb1ce611c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012121"
---
# <a name="tspi_linesetcurrentlocation"></a>Riga \_ TSPISetCurrentLocation

Questa funzione \_ lineSetCurrentLocation TSPI è obsoleta. TAPI ha chiamato questa funzione  quando l'utente (usando la finestra di dialogo Proprietà di composizione) o un'applicazione (usando la [**funzione lineSetCurrentLocation)**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) ha modificato il percorso di conversione degli indirizzi.

Attualmente, una modifica della posizione di traduzione comporta un messaggio LINE DEVSTATE con \_ *dwParam1* impostato su LINEDEVSTATE \_ TRANSLATECHANGE.

 

 
