---
description: Prima di poter accodare le operazioni sui file, è necessario aprire una coda di file. La chiamata della funzione SetupOpenFileQueue restituisce un handle a un file di coda. Questo handle viene usato dalle funzioni di coda successive per fare riferimento alla coda aperta e aggiungervi operazioni o eseguirne l'analisi.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Apertura e chiusura di una coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcd8ece0e09c313857da6838a09e79e23bb46a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315316"
---
# <a name="opening-and-closing-a-queue"></a>Apertura e chiusura di una coda

Prima di poter accodare le operazioni sui file, è necessario aprire una coda di file. La chiamata della funzione [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) restituisce un handle a un file di coda. Questo handle viene usato dalle funzioni di coda successive per fare riferimento alla coda aperta e aggiungervi operazioni o eseguirne l'analisi.

Dopo che tutte le operazioni sui file specificate sono state accodate e ne è stato eseguito il commit, è necessario chiamare la funzione [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) per rilasciare le risorse allocate durante la chiamata a [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).

> [!Note]  
> La funzione [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) non esegue il commit della coda di file. Tutte le operazioni di cui non è stato eseguito il commit quando viene chiamato **SetupCloseFileQueue** non verranno eseguite.

 

 

 



