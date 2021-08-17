---
description: Se si prevede di associare uno o più tipi di file a una nuova applicazione, è necessario definire un ProgID per ogni tipo di file che si vuole associare all'applicazione.
ms.assetid: 997600C9-5264-44EC-BAEC-CB5CEEA0BD14
title: Come registrare un tipo di file per una nuova applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de165d378d27c6891b681f95da7242b026844bd7734709ebd272c06edf40e3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859661"
---
# <a name="how-to-register-a-file-type-for-a-new-application"></a>Come registrare un tipo di file per una nuova applicazione

Se si prevede di associare uno o più tipi di file a una nuova applicazione, è necessario definire un ProgID per ogni tipo di file che si vuole associare all'applicazione.

Per creare un ProgID per ogni tipo di file univoco gestito dall'applicazione, seguire questa procedura.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Si noti che alcuni tipi di file hanno più estensioni che puntano allo stesso ProgID. Per esempio:

-   **HKEY \_ CLASSES \_ ROOT** \\ **App.jpeg** (progID)
-   **HKEY \_ CLASSES \_ ROOT** \\ **.jpg** = App.jpeg (mapping dei tipi di file)
-   **HKEY \_ CLASSES \_ ROOT** \\ **.jpeg** = App.jpeg

### <a name="step-2"></a>Passaggio 2:

Rimuovere i valori ProgID quando si installa e si disinstalla il programma.

### <a name="step-3"></a>Passaggio 3:

Lasciare invariati i mapping dei tipi di file in fase di disinstallazione. Questa operazione funziona perché i mapping dei tipi di file vengono archiviati per utente in HKEY \_ CLASSES \_ ROOT .ext e il sistema identifica il caso in cui manca il valore ProgID e \\ lo ignora. Lasciare invariati i mapping dei tipi di file evita la necessità di avere codice condizionale che rimuove il mapping del tipo di file solo se il valore punta ancora al ProgID. È importante evitare questa operazione nei casi in cui potrebbe essere stata modificata da un'altra applicazione e pertanto non è possibile rimuovere facilmente il valore.

### <a name="step-4"></a>Passaggio 4:

Specificare un valore univoco per la descrizione del tipo di file progID di ogni tipo di file eseguendo una delle operazioni seguenti:

-   Lasciare vuoto il valore predefinito di ProgID, nel qual caso il sistema usa il file con estensione ext.
-   Specificare un valore localizzato tramite FriendlyTypeName e, per compatibilità con le applicazioni precedenti che leggono direttamente il Registro di sistema, assicurarsi di specificare il valore predefinito di ProgID come descrizione del tipo di file, ovvero usare lo stesso valore a cui fa riferimento FriendlyTypeName nella risorsa inglese.

## <a name="remarks"></a>Commenti

Se si prevede di associare il file a un'applicazione esistente, individuare un ProgID dell'applicazione nel Registro di sistema. Per altre informazioni, vedere [Tipi di file](fa-file-types.md).

 

 



