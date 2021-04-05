---
description: Rappresentazione della funzionalità
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Rappresentazione della funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883149"
---
# <a name="representing-functionality"></a>Rappresentazione della funzionalità

Gli oggetti funzionali sono disponibili per identificare o raggruppare logicamente le funzionalità di un dispositivo. Ad esempio, un'applicazione può vedere che un dispositivo supporta SMS cercando l'oggetto funzionale SMS. Analogamente, l'applicazione può verificare che un dispositivo disponga di funzionalità della fotocamera cercando l'oggetto funzionale Acquisisci immagine ancora.

Questa rappresentazione flessibile degli oggetti consente un supporto semplice per i dispositivi con funzionalità multifunzione. I driver possono semplicemente esporre gli oggetti funzionali che rappresentano il dispositivo, più granulare rispetto all'uso delle classi di dispositivi tradizionali. La rappresentazione dell'oggetto consente inoltre di isolare le parti funzionali sovrapposte; ad esempio, alcuni telefoni possono avere due fotocamere o quattro archivi.

Nel sistema operativo Windows 7 i servizi estendono gli oggetti funzionali fornendo query complete sulle funzionalità e un raggruppamento astratto di contenuti. Le applicazioni possono usare i servizi per individuare le funzionalità del dispositivo e interagire con il contenuto in modo più efficiente. Ad esempio, un'applicazione può verificare che un dispositivo supporti le funzionalità di sincronizzazione dei contatti cercando un oggetto servizio contatti e possa trovare tutti i contatti come oggetti figlio dell'oggetto servizio, senza dover eseguire ricerche ricorsive nella gerarchia di archiviazione.

I servizi consentono inoltre alle applicazioni di individuare e richiamare un comportamento personalizzato in un dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'applicazione**](application-overview.md)
</dt> </dl>

 

 



