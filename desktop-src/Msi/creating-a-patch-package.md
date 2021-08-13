---
description: Gli sviluppatori creano un pacchetto di patch generando un file di creazione di patch e usando Msimsp.exe per chiamare la funzione UiCreatePatchPackageEx in Patchwiz.dll.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Creazione di un pacchetto patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2d784e02374eeee84a0c8b047e5a7b4db31f9c2b3090a68c31f35dece8c978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638291"
---
# <a name="creating-a-patch-package"></a>Creazione di un pacchetto patch

Gli sviluppatori creano un pacchetto di patch generando un file [ di creazione ](msimsp-exe.md) di patch e usandoMsimsp.exeper chiamare la funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md). Msimsp.exe e Patchwiz.dll sono disponibili in Windows Installer SDK. Per altre informazioni, vedere [A Small Update Patching Example](a-small-update-patching-example.md).

Poiché l'applicazione di una patch a un pacchetto del programma di installazione di Windows comporta l'installazione delle origini originali usando un nuovo file .msi, il nuovo file .msi deve rimanere compatibile con il layout dell'origine originale.

Quando si crea un pacchetto di patch, è necessario usare un'immagine di installazione non compressa per creare una patch, ad esempio un'immagine amministrativa o un'immagine di installazione non compressa da un CD-ROM. È inoltre necessario rispettare le restrizioni seguenti:

-   Non spostare i file da una cartella a un'altra.
-   Non spostare i file da un archivio a un altro.
-   Non modificare l'ordine dei file in un file CAB.
-   Non modificare il numero di sequenza dei file esistenti. Il numero di sequenza è il valore specificato nella colonna Sequenza della [tabella File](file-table.md).
-   Tutti i nuovi file aggiunti dalla patch devono essere inseriti alla fine della sequenza di file esistente. Il numero di sequenza di qualsiasi nuovo file nell'immagine aggiornata deve essere maggiore del numero di sequenza più elevato di file esistenti nell'immagine di destinazione.
-   Non modificare le chiavi primarie nella [tabella file tra](file-table.md) la versione originale e quella .msi file.
    > [!Note]  
    > Il file deve avere la stessa chiave nella tabella [file dell'immagine](file-table.md) di destinazione e dell'immagine aggiornata. I valori stringa nella colonna File di entrambe le tabelle devono essere identici, incluso il caso.

     

-   Non creare un pacchetto con chiavi [tabella file](file-table.md) che differiscono solo nel caso, ad esempio, evitare l'esempio di tabella seguente.

    

    | File       | Componente\_ | FileName   |
    |------------|-------------|------------|
    | readme.txt | Comp1       | readme.txt |
    | ReadMe.txt | Comp2       | readme.txt |

    

     

    Il programma di installazione di Windows può consentire l'esempio di tabella precedente quando Comp1 e Comp2 sono installati in directory diverse, ma non è possibile usare [Msimsp.exe](msimsp-exe.md) o [Patchwiz.dll](patchwiz-dll.md) per generare una patch per il pacchetto. Msimsp.exe e Patchwiz.dll chiamare Makecab.exe, che non fa distinzione tra maiuscole e minuscole e ha esito negativo.

    Quando si usano i moduli unione nel programma di installazione, assicurarsi che i numeri di sequenza di file e il layout siano conformi alle linee guida precedenti.

 

 



