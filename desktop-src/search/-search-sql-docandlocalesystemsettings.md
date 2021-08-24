---
description: Quando il sistema operativo, o anche un'applicazione, è impostato per l'uso di una lingua e di impostazioni locali specifiche, sono interessate molte impostazioni.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Documenti e impostazioni locali del sistema Impostazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed43ae52d7626b759563069b05fe4ae03649feb63fd1af8dab1b80cfd4d558a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594781"
---
# <a name="document-and-system-locale-settings"></a>Documenti e impostazioni locali del sistema Impostazioni

Quando il sistema operativo, o anche un'applicazione, è impostato per l'uso di una lingua e di impostazioni locali specifiche, sono interessate molte impostazioni. Queste impostazioni includono formato numerico, formato di data, formato di valuta, mapping di maiuscole e minuscole, ordinamento del dizionario, tokenizzazione e altro ancora. Anche se queste impostazioni consentono Windows ricerca offre un eccellente supporto localizzato, possono verificarsi risultati imprevisti quando la ricerca viene eseguita nei documenti di una delle impostazioni locali usando un sistema impostato su un'altra impostazione locale.

Quando [**l'oggetto IFilter**](/windows/win32/api/filter/nn-filter-ifilter) elabora le proprietà di testo e il contenuto di un documento, segnala la lingua del documento all'indicizzatore di contenuto. Usando queste informazioni, Windows ricerca può applicare il word breaker appropriato.

 

 
