---
description: Windows Installer proprietà sono variabili globali utilizzate dal programma di installazione durante un'installazione.
ms.assetid: 1c59939b-de0f-4bf4-ab1f-4f1aa2488bfa
title: Specifica delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd4294f35595e723491398172dc4c73337a1416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310792"
---
# <a name="specifying-properties"></a>Specifica delle proprietà

Windows Installer proprietà sono variabili globali utilizzate dal programma di installazione durante un'installazione. Vedere le sezioni in [Proprietà](properties.md). Se nella sezione [importazione di un database vuoto](importing-a-blank-database.md) utilizzato uisample.msi da Windows Installer SDK, la tabella delle [Proprietà](property-table.md) nella copia di MNP2000.msi contiene già molte proprietà utilizzate dall'interfaccia utente. In questa sezione vengono aggiunte informazioni aggiuntive alla tabella delle proprietà specifiche dell'installazione del blocco note. Vedere anche il [gruppo tabelle informazioni sul programma](program-information-tables-group.md).

In ogni pacchetto di installazione sono necessarie cinque proprietà, che devono essere aggiornate per l'esempio del blocco note nella tabella delle [Proprietà](property-table.md) di MNP2000.msi:

-   [**ProductCode**](productcode.md)
-   [**ProductLanguage**](productlanguage.md)
-   [**Produttore**](manufacturer.md)
-   [**ProductVersion**](productversion.md)
-   [**ProductName**](productname.md)

Sebbene non sia richiesto da tutti i pacchetti di installazione, le applicazioni che potrebbero ricevere un aggiornamento in futuro dovrebbero avere anche una proprietà [**UpgradeCode**](upgradecode.md) . Vedere [preparazione di un'applicazione per aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md).

Utilizzare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella delle proprietà. L'elenco contiene i collegamenti agli argomenti di riferimento per le proprietà predefinite del programma di installazione. I nomi di proprietà che non sono collegamenti sono proprietà definite dall'autore. Molte delle proprietà importate da uisample.msi sono per l'interfaccia utente di esempio. Nella sezione successiva interfaccia utente dell'esempio di installazione viene illustrata l'interfaccia utente.

[Tabella delle proprietà](property-table.md)



| Proprietà                                         | Valore                                     |
|--------------------------------------------------|-------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)               | https://www.microsoft.com/management       |
| BannerBitmap                                     | bannrbmp                                  |
| ButtonText \_ indietro                                 | < &indietro                                |
| ButtonText \_ Sfoglia                               | BR&owse                                   |
| \_Annullamento ButtonText                               | Annulla                                    |
| \_Uscita ButtonText                                 | Uscita &                                     |
| \_Fine ButtonText                               | Fine &                                   |
| \_Ignora ButtonText                               | Ignora &                                   |
| Installazione di ButtonText \_                              | Installazione &                                  |
| ButtonText \_ successivo                                 | &successiva >                                |
| ButtonText \_ No                                   | &No                                       |
| ButtonText \_ OK                                   | OK                                        |
| ButtonText \_ rimuovere                               | Rimozione &                                   |
| Reimpostazione ButtonText \_                                | Reimpostazione &                                    |
| Riprendi ButtonText \_                               | Riprendi &                                   |
| ButtonText \_ nuovo tentativo                                | Tentativo di &                                    |
| ButtonText \_ restituito                               | &restituito                                   |
| ButtonText \_ Sì                                  | &Sì                                      |
| CompleteSetupIcon                                | completa                                  |
| ComponentDownload                                | ftp://anonymous@microsoft.com/components/ |
| CustomSetupIcon                                  | custicon                                  |
| [**DefaultUIFont**](defaultuifont.md)           | DlgFont8                                  |
| DialogBitmap                                     | dlgbmp                                    |
| DlgTitleFont                                     | {&DlgFontBold8}                           |
| ErrorDialog                                      | ErrorDlg                                  |
| ExclamationIcon                                  | exclamic                                  |
| Falso                                            | 0                                         |
| Iagree                                           | No                                        |
| InfoIcon                                         | info                                      |
| InstallerIcon                                    | insticon                                  |
| [**INSTALLLEVEL**](installlevel.md)             | 3                                         |
| InstallMode                                      | Typical (Tipica)                                   |
| [**Produttore**](manufacturer.md)             | Microsoft                                 |
| [**PIDTemplate**](pidtemplate.md)               | 12345<\#\#\#-%%%%%%%>@@@@@          |
| [**ProductCode**](productcode.md)               | {18A9233C-0B34-4127-A966-C257386270BC}    |
| [**ProductID**](productid.md)                   | Nessuno                                      |
| [**ProductLanguage**](productlanguage.md)       | 1033                                      |
| [**ProductName**](productname.md)               | MNP2000                                   |
| [**ProductVersion**](productversion.md)         | 01.40.0000                                |
| Progress1                                        | Installazione                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | ripristino                                  |
| Configurazione                                            | Configurazione                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Procedura guidata                                           | Installazione guidata                              |



 

[Continua](importing-the-installexecutesequence.md)

 

 



