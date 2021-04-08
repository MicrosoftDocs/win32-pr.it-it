---
description: Poiché l'aggiornamento modifica il nome del file con estensione msi e modifica il codice componente di alcuni componenti, è necessario modificare il codice del prodotto dell'aggiornamento rispetto a quello del prodotto originale.
ms.assetid: ebb1a217-fce6-43f0-9139-c0f4422c8fc4
title: Aggiornamento delle proprietà per un aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750c30a75650ff4009dda799b0542f41f535481f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058231"
---
# <a name="updating-properties-for-an-upgrade"></a>Aggiornamento delle proprietà per un aggiornamento

Poiché l'aggiornamento modifica il nome del file con estensione msi e modifica il codice componente di alcuni componenti, è necessario modificare il codice del prodotto dell'aggiornamento rispetto a quello del prodotto originale. Per una descrizione dei casi in cui è necessario un aggiornamento per modificare la proprietà [**ProductCode**](productcode.md) , vedere [modifica del codice del prodotto](changing-the-product-code.md). Un aggiornamento che modifica ProductCode viene definito [aggiornamento principale](major-upgrades.md).

La proprietà [**ProductName**](productname.md) del pacchetto di aggiornamento, la proprietà [**ProductVersion**](productversion.md) , la proprietà [**ProductLanguage**](productlanguage.md) e la proprietà [**UpgradeCode**](upgradecode.md) possono essere modificate o lasciate invariate dal prodotto originale. In base ai valori di queste proprietà, Windows Installer possibile determinare se applicare i pacchetti di aggiornamento futuri all'aggiornamento corrente.

È necessario aggiungere la proprietà specificata nella colonna ActionProperty della [tabella di aggiornamento](upgrade-table.md) alla proprietà [**SecureCustomProperties**](securecustomproperties.md) .

Utilizzare l'editor di database per aprire MNP2001.msi e immettere i dati seguenti nella [tabella delle proprietà](property-table.md). L'elenco contiene i collegamenti agli argomenti di riferimento per le proprietà predefinite del programma di installazione. I nomi di proprietà che non sono collegamenti sono proprietà definite dall'autore. Molte delle proprietà sono state importate da Uisample.msi fornita con l'SDK. Per informazioni dettagliate, vedere [importazione dell'interfaccia utente](importing-the-user-interface.md).

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
| [**ProductCode**](productcode.md)               | {34CF587C-1D8F-4DD5-ADFE-440F4B593987}    |
| [**ProductID**](productid.md)                   | Nessuno                                      |
| [**ProductLanguage**](productlanguage.md)       | 1033                                      |
| [**ProductName**](productname.md)               | MNP2001                                   |
| [**ProductVersion**](productversion.md)         | 01.50.0000                                |
| Progress1                                        | Installazione                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | ripristino                                  |
| Configurazione                                            | Configurazione                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Procedura guidata                                           | Installazione guidata                              |
| SecureCustomProperties                           | OLDAPPFOUND                               |



 

[Continua](updating-sequence-tables-for-an-upgrade.md)

 

 



