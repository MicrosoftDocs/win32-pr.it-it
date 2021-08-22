---
description: Se dopo l'esecuzione di un'installazione è necessario verificare che sia stata installata una particolare funzionalità, componente o file, attivare l'opzione di registrazione dettagliata durante l'installazione. Vedere Windows registrazione del programma di installazione e Opzioni della riga di comando.
ms.assetid: c4547e5d-ea71-494f-9d92-c7fef23bcc0f
title: Controllo dell'installazione di funzionalità, componenti e file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866b4f7b042c97660e43a92fc55eeb99e2f1e9f3574a9b03c4d3d6e6096504c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145607"
---
# <a name="checking-the-installation-of-features-components-files"></a>Controllo dell'installazione di funzionalità, componenti e file

Se dopo l'esecuzione di un'installazione è necessario verificare che sia stata installata una particolare funzionalità, componente o file, attivare l'opzione di registrazione dettagliata durante l'installazione. Vedere [Windows Installer Logging (Registrazione del programma di installazione)](windows-installer-logging.md) e Command Line Options [(Opzioni della riga di comando).](command-line-options.md)

Il log dettagliato include una voce per ogni funzionalità e componente che il pacchetto di installazione può installare. Il log indica lo stato di tale funzionalità o componente prima dell'installazione, lo stato richiesto dall'installazione e lo stato in cui il programma di installazione ha lasciato la funzionalità o il componente. Le voci relative a funzionalità e componenti nel log vengono visualizzate come negli esempi seguenti.

``` syntax
MSI (s) (40:A4): Feature: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
MSI (s) (40:A4): Component: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
```

Questo log dettagliato indica che:

-   Lo stato di installazione della funzionalità QuickTest e del componente era assente prima dell'esecuzione del pacchetto
-   il pacchetto ha richiesto un'installazione locale di questi
-   La funzionalità e il componente sono stati entrambi lasciati nello stato installato localmente dopo l'esecuzione del pacchetto.

L'etichetta "Installato" nel log si riferisce allo stato di installazione corrente della funzionalità o del componente, "Richiesta" si riferisce allo stato di installazione richiesto della funzionalità o del componente. "Azione" si riferisce allo stato effettivo dell'azione della funzionalità o del componente.

Nella tabella seguente sono elencati i possibili stati dei componenti o delle funzionalità che possono essere visualizzati nel log.



| Voce registro              | Descrizione                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Richiesta: Null          | Nessuna richiesta.                                                                                                     |
| Azione: Null           | Nessuna azione eseguita.                                                                                                |
| Installato: Assente      | Il componente o la funzionalità non è attualmente installata.                                                                |
| Richiesta: Absent        | L'installazione richiede la disinstallazione del componente o della funzionalità.                                                      |
| Azione: Absent         | Il programma di installazione disinstalla effettivamente il componente o la funzionalità.                                                             |
| Installato: Locale       | Il componente o la funzionalità è attualmente installata per l'esecuzione in locale.                                                       |
| Richiesta: Locale         | L'installazione richiede l'installazione del componente o della funzionalità per l'esecuzione in locale.                                           |
| Azione: Locale          | Il programma di installazione installa effettivamente il componente o la funzionalità per l'esecuzione locale.                                                  |
| Installato: Origine      | Il componente o la funzionalità è attualmente installata per l'esecuzione dall'origine.                                                 |
| Richiesto: Origine      | L'installazione richiede che il componente o la funzionalità siano installati per l'esecuzione dall'origine.                                |
| Azione: Origine         | Il programma di installazione installa effettivamente il componente o la funzionalità da eseguire dall'origine.                                        |
| Installato: Annunciare   | La funzionalità è attualmente annunciata. I componenti non vengono mai annunciati.                                               |
| Richiesta: Annunciare     | Le richieste di installazione devono essere installate come funzionalità annunciate.                                            |
| Azione: Annunciare      | Il programma di installazione installa effettivamente la funzionalità come funzionalità annunciata.                                               |
| Richiesta: Reinstalla     | Le richieste di installazione devono essere reinstallate. I componenti non usano lo stato di reinstallazione.                            |
| Azione: Reinstalla      | Il programma di installazione reinstalla effettivamente la funzionalità .                                                                          |
| Installato: Corrente     | La funzionalità è attualmente installata nello stato di installazione predefinito creato.                                           |
| Richiesta: Corrente       | Le richieste di installazione devono essere installate nello stato di installazione predefinito creato.                               |
| Azione: Corrente        | Il programma di installazione installa effettivamente la funzionalità nello stato di installazione predefinito creato.                                  |
| Azione: FileAbsent     | Il programma di installazione disinstalla effettivamente i file del componente e lascia installate tutte le altre risorse del componente.      |
| Azione: HKCRAbsent     | Il programma di installazione rimuove effettivamente le informazioni HKCR del componente. Rimangono informazioni su file e non HKCR.                  |
| Azione: HKCRFileAbsent | Il programma di installazione rimuove effettivamente le informazioni e i file HKCR del componente. Tutte le altre risorse del componente rimangono. |



 

Il log dettagliato contiene una voce per ogni file che può essere installato dal pacchetto. Il log indica le attività eseguite nel file e fornisce una spiegazione. Le voci del file nel log vengono visualizzate come nell'esempio seguente.

``` syntax
MSI (s) (40:A4): File: C:\Test\TESTDB.EXE;  Won't Overwrite;  Existing
 file is of an equal version
```

Questo log indica che il programma di installazione non sovrascriverà il file Testdb.exe esistente perché il file esistente corrisponde alla versione installata.

> [!Note]  
> Se è necessario creare un pacchetto di installazione che cerca un file o una directory esistente nel computer dell'utente durante un'installazione, usare il metodo descritto in Ricerca di [applicazioni, file,](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)voci del Registro di sistema o voci di file .ini esistenti .

 

 

 



