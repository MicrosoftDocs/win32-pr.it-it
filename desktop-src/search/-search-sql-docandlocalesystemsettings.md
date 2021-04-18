---
description: Quando il sistema operativo, o anche un'applicazione, è impostato per l'utilizzo di una lingua e delle impostazioni locali specifiche, sono interessate molte impostazioni.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Impostazioni locali documento e sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9408093a8583a4b17566b5fcd118b30439c0ebda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306132"
---
# <a name="document-and-system-locale-settings"></a>Impostazioni locali documento e sistema

Quando il sistema operativo, o anche un'applicazione, è impostato per l'utilizzo di una lingua e delle impostazioni locali specifiche, sono interessate molte impostazioni. Queste impostazioni includono formato numerico, formato data, formato valuta, mapping maiuscolo e minuscolo, ordinamento dizionario, token e altro. Anche se queste impostazioni consentono a Windows Search di fornire un supporto localizzato eccellente, possono verificarsi risultati imprevisti quando viene eseguita una ricerca nei documenti di un'impostazione locale usando un sistema impostato su altre impostazioni locali.

Quando l'oggetto [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) elabora le proprietà e il contenuto di testo di un documento, segnala la lingua del documento all'indicizzatore di contenuto. Utilizzando queste informazioni, Windows Search può applicare il Word breaker appropriato.

 

 
