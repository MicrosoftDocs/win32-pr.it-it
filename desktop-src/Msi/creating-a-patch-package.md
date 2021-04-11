---
description: Gli sviluppatori creano un pacchetto di patch generando un file di creazione della patch e usando Msimsp.exe per chiamare la funzione UiCreatePatchPackageEx in Patchwiz.dll.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Creazione di un pacchetto di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231883"
---
# <a name="creating-a-patch-package"></a>Creazione di un pacchetto di patch

Gli sviluppatori creano un pacchetto di patch generando un file di creazione della patch e usando [Msimsp.exe](msimsp-exe.md) per chiamare la funzione [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md). In Windows Installer SDK sono disponibili Msimsp.exe e Patchwiz.dll. Per ulteriori informazioni, vedere [un esempio di patch per l'aggiornamento di piccole dimensioni](a-small-update-patching-example.md).

Poiché l'applicazione di una patch a un pacchetto di Windows Installer comporta l'installazione delle origini originali utilizzando un nuovo file con estensione msi, il nuovo file con estensione msi deve rimanere compatibile con il layout dell'origine originale.

Quando si crea un pacchetto di patch, è necessario utilizzare un'immagine di installazione non compressa per creare una patch, ad esempio un'immagine amministrativa o un'immagine di configurazione non compressa da un CD-ROM. È necessario inoltre rispettare le restrizioni seguenti:

-   Non spostare i file da una cartella a un'altra.
-   Non spostare i file da un file CAB a un altro.
-   Non modificare l'ordine dei file in un file CAB.
-   Non modificare il numero di sequenza dei file esistenti. Il numero di sequenza è il valore specificato nella colonna sequenza della [tabella file](file-table.md).
-   Tutti i nuovi file aggiunti dalla patch devono essere inseriti alla fine della sequenza di file esistente. Il numero di sequenza di un nuovo file nell'immagine aggiornata deve essere maggiore del numero di sequenza più grande dei file esistenti nell'immagine di destinazione.
-   Non modificare le chiavi primarie nella [tabella file](file-table.md) tra le versioni originali e nuove del file con estensione msi.
    > [!Note]  
    > Il file deve avere la stessa chiave nella [tabella file](file-table.md) dell'immagine di destinazione e dell'immagine aggiornata. I valori stringa nella colonna file di entrambe le tabelle devono essere identici, inclusa la distinzione tra maiuscole e minuscole.

     

-   Non creare un pacchetto con chiavi della [tabella file](file-table.md) che differiscono solo per le maiuscole/minuscole, ad esempio, evitare l'esempio di tabella seguente.

    

    | File       | Componente\_ | FileName   |
    |------------|-------------|------------|
    | readme.txt | Comp1       | readme.txt |
    | ReadMe.txt | Comp2       | readme.txt |

    

     

    Il Windows Installer può consentire l'esempio di tabella precedente quando comp1 e comp2 sono installati in directory diverse, ma non è possibile usare [Msimsp.exe](msimsp-exe.md) o [Patchwiz.dll](patchwiz-dll.md) per generare una patch per il pacchetto. Msimsp.exe e Patchwiz.dll chiamano Makecab.exe, senza distinzione tra maiuscole e minuscole e con esito negativo.

    Quando si usano i modelli merge nel programma di installazione, assicurarsi che i numeri di sequenza e il layout dei file rispettino le linee guida indicate sopra.

 

 



