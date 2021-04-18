---
description: Se dopo l'esecuzione di un'installazione di, è necessario verificare che sia stata installata una particolare funzionalità, componente o file, attivare l'opzione di registrazione dettagliata durante l'installazione. Vedere Windows Installer opzioni per la registrazione e la riga di comando.
ms.assetid: c4547e5d-ea71-494f-9d92-c7fef23bcc0f
title: Verifica dell'installazione di funzionalità, componenti, file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cab15b4f0590ee5613865d4b7c21439eec6dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310984"
---
# <a name="checking-the-installation-of-features-components-files"></a>Verifica dell'installazione di funzionalità, componenti, file

Se dopo l'esecuzione di un'installazione di, è necessario verificare che sia stata installata una particolare funzionalità, componente o file, attivare l'opzione di registrazione dettagliata durante l'installazione. Vedere [Windows Installer](windows-installer-logging.md) opzioni per la registrazione e la [riga di comando](command-line-options.md).

Il log dettagliato include una voce per ogni funzionalità e componente che può essere installato dal pacchetto di installazione. Il log indica lo stato della funzionalità o del componente precedente all'installazione, lo stato richiesto dall'installazione e lo stato in cui il programma di installazione ha lasciato la funzionalità o il componente. Le voci relative a funzionalità e componenti nel log vengono visualizzate come gli esempi seguenti.

``` syntax
MSI (s) (40:A4): Feature: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
MSI (s) (40:A4): Component: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
```

Questo log dettagliato indica che:

-   lo stato di installazione della funzionalità e del componente QuickTest è assente prima di eseguire il pacchetto
-   il pacchetto ha richiesto un'installazione locale di questi
-   la funzionalità e il componente sono rimasti nello stato installato localmente dopo l'esecuzione del pacchetto.

L'etichetta "installato" nel log si riferisce allo stato di installazione corrente della funzionalità o del componente, "richiesta" si riferisce allo stato di installazione richiesto della funzionalità o del componente. "Action" si riferisce allo stato dell'azione effettivo della funzionalità o del componente.

Nella tabella seguente sono elencati i possibili stati del componente o della funzionalità che possono essere visualizzati nel log.



| Voce registro              | Descrizione                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Richiesta: null          | Nessuna richiesta.                                                                                                     |
| Azione: null           | Non viene eseguita alcuna azione.                                                                                                |
| Installato: assente      | Componente o funzionalità non attualmente installata.                                                                |
| Richiesta: assente        | Il componente o la funzionalità delle richieste di installazione deve essere disinstallata.                                                      |
| Azione: assente         | Il programma di installazione Disinstalla effettivamente il componente o la funzionalità.                                                             |
| Installato: locale       | Il componente o la funzionalità è attualmente installato per l'esecuzione locale.                                                       |
| Richiesta: locale         | Per l'esecuzione locale, è necessario installare il componente o la funzionalità delle richieste di installazione.                                           |
| Azione: locale          | Il programma di installazione installa effettivamente il componente o la funzionalità per l'esecuzione locale.                                                  |
| Installato: origine      | Componente o funzionalità attualmente installato per l'esecuzione dall'origine.                                                 |
| Richiesta: origine      | L'installazione richiede l'installazione del componente o della funzionalità per l'esecuzione dall'origine.                                |
| Azione: origine         | Il programma di installazione installa effettivamente il componente o la funzionalità per l'esecuzione dall'origine.                                        |
| Installato: annuncio   | La funzionalità è attualmente annunciata. I componenti non vengono mai annunciati.                                               |
| Richiesta: annuncio     | La funzionalità richieste di installazione deve essere installata come funzionalità annunciata.                                            |
| Azione: annuncio      | Il programma di installazione installa effettivamente la funzionalità come funzionalità annunciata.                                               |
| Richiesta: reinstallare     | La funzionalità richieste di installazione verrà reinstallata. I componenti non utilizzano lo stato REINSTALL.                            |
| Azione: Reinstalla      | Il programma di installazione Reinstalla effettivamente la funzionalità.                                                                          |
| Installato: corrente     | La funzionalità è attualmente installata nello stato di installazione predefinito creato.                                           |
| Richiesta: corrente       | La funzionalità richieste di installazione verrà installata nello stato di installazione predefinito creato.                               |
| Azione: corrente        | Il programma di installazione installa effettivamente la funzionalità nello stato di installazione predefinito creato.                                  |
| Azione: Assent     | Il programma di installazione Disinstalla effettivamente i file del componente e lascia installate tutte le altre risorse del componente.      |
| Azione: HKCRAbsent     | Il programma di installazione rimuove effettivamente le informazioni HKCR del componente. Rimangono le informazioni su file e non HKCR.                  |
| Azione: HKCRFileAbsent | Il programma di installazione rimuove effettivamente le informazioni e i file HKCR del componente. Tutte le altre risorse del componente rimangono. |



 

Il log dettagliato include una voce per ogni file che può essere installato dal pacchetto. Il log indica cosa è stato fatto al file e fornisce una spiegazione. Le voci di file nel log vengono visualizzate come nell'esempio seguente.

``` syntax
MSI (s) (40:A4): File: C:\Test\TESTDB.EXE;  Won't Overwrite;  Existing
 file is of an equal version
```

Questo log indica che il programma di installazione non sovrascrive il file di Testdb.exe esistente perché il file esistente corrisponde alla versione installata.

> [!Note]  
> Se è necessario creare un pacchetto di installazione che cerca un file o una directory esistente nel computer dell'utente durante un'installazione, usare il metodo descritto in [ricerca di applicazioni, file, voci del registro di sistema o voci di file ini esistenti](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

 

 

 



