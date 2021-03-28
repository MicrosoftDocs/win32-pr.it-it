---
description: Se si prevede di associare uno o più tipi di file a una nuova applicazione, è necessario definire un ProgID per ogni tipo di file che si desidera associare all'applicazione.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Come registrare un tipo di file per una nuova applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728cc48075ab1c2631f0a950059da65ae326ae79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979527"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a>Come registrare un tipo di file per una nuova applicazione

Se si prevede di associare uno o più tipi di file a una nuova applicazione, è necessario definire un ProgID per ogni tipo di file che si desidera associare all'applicazione.

Per creare un ProgID per ogni tipo di file univoco gestito dall'applicazione, attenersi alla procedura riportata di seguito.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Si noti che alcuni tipi di file hanno più estensioni che puntano allo stesso ProgID; Per esempio:

-   **HKEY \_ Classe \_ radice** \\ **app. jpeg** (ProgID)
-   **HKEY \_ Classes \_ root** \\ **. jpg** = app. jpeg (mapping dei tipi di file)
-   **HKEY \_ Classe \_ root** \\ **. jpeg** = app. jpeg

### <a name="step-2"></a>Passaggio 2:

Rimuovere i valori ProgID quando si installa e disinstalla il programma.

### <a name="step-3"></a>Passaggio 3:

Lasciare invariati i mapping dei tipi di file in fase di disinstallazione. Questa operazione funziona perché i mapping dei tipi di file vengono archiviati per utente nelle \_ classi HKEY \_ root \\ . ext e il sistema identifica il caso in cui il valore ProgID è mancante e lo ignora. Se si lasciano invariati i mapping dei tipi di file, si evita di dover disporre di codice condizionale che rimuove solo il mapping dei tipi di file se il valore fa ancora riferimento al ProgID. È importante evitare di eseguire questa operazione nei casi in cui potrebbe essere stato modificato da un'altra applicazione e pertanto non è possibile rimuovere facilmente il valore.

### <a name="step-4"></a>Passaggio 4:

Specificare un valore univoco per la descrizione del tipo di file di ogni tipo di file ProgID eseguendo una delle operazioni seguenti:

-   Lasciare vuoto il valore predefinito del ProgID, nel qual caso il sistema usa il file. ext.
-   Fornire un valore localizzato tramite FriendlyTypeName e, per compatibilità con le applicazioni precedenti che leggono direttamente il registro di sistema, assicurarsi di specificare il valore predefinito del ProgID come descrizione del tipo di file, ovvero usare lo stesso valore a cui fa riferimento il FriendlyTypeName nella risorsa inglese.

## <a name="remarks"></a>Commenti

Se si prevede di associare il file a un'applicazione esistente, individuare un ProgID dell'applicazione nel registro di sistema. Per ulteriori informazioni, vedere [tipi di file](fa-file-types.md).

 

 



