---
description: Poiché l'aggiornamento modifica il nome del file .msi e modifica il codice del componente di alcuni componenti, il codice prodotto dell'aggiornamento deve essere modificato da quello del prodotto originale.
ms.assetid: ebb1a217-fce6-43f0-9139-c0f4422c8fc4
title: Aggiornamento delle proprietà per un aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d340f56eaf78c585e28a52dc7b310bf1af047d7530e61b841267bc0b83251a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039181"
---
# <a name="updating-properties-for-an-upgrade"></a>Aggiornamento delle proprietà per un aggiornamento

Poiché l'aggiornamento modifica il nome del file .msi e modifica il codice del componente di alcuni componenti, il codice prodotto dell'aggiornamento deve essere modificato da quello del prodotto originale. Per una descrizione dei casi in cui è necessario un aggiornamento per modificare la [**proprietà ProductCode,**](productcode.md) vedere [Modifica del codice prodotto](changing-the-product-code.md). Un aggiornamento che modifica ProductCode viene definito [aggiornamento principale.](major-upgrades.md)

La proprietà [**ProductName**](productname.md) del pacchetto di aggiornamento, la proprietà [**ProductVersion,**](productversion.md) la proprietà [**ProductLanguage**](productlanguage.md) e [**la proprietà UpgradeCode**](upgradecode.md) possono essere modificate o non modificate dal prodotto originale. In base ai valori di queste proprietà, Windows programma di installazione può determinare se applicare pacchetti di aggiornamento futuri all'aggiornamento corrente.

La proprietà specificata nella colonna ActionProperty della [tabella Upgrade](upgrade-table.md) deve essere aggiunta alla [**proprietà SecureCustomProperties.**](securecustomproperties.md)

Usare l'editor di database per aprire MNP2001.msi e immettere i dati seguenti nella [tabella Proprietà](property-table.md). L'elenco fornisce collegamenti agli argomenti di riferimento per le proprietà predefinite del programma di installazione. I nomi delle proprietà che non sono collegamenti sono proprietà definite dall'autore. Molte delle proprietà sono state importate dal Uisample.msi fornito con l'SDK. Per informazioni dettagliate, vedere [Importazione del Interfaccia utente](importing-the-user-interface.md).

[Tabella delle proprietà](property-table.md)



| Proprietà                                         | Valore                                     |
|--------------------------------------------------|-------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)               | https://www.microsoft.com/management       |
| BannerBitmap                                     | bannrbmp                                  |
| ButtonText \_ Indietro                                 | < &indietro                                |
| PulsanteText \_ Browse                               | Br&owse                                   |
| ButtonText \_ Cancel                               | Annulla                                    |
| Uscita \_ di ButtonText                                 | &esci                                     |
| ButtonText \_ Finish                               | &fine                                   |
| ButtonText \_ Ignore                               | &ignorare                                   |
| Installazione \_ di ButtonText                              | &installazione                                  |
| ButtonText \_ Next                                 | &successivo >                                |
| ButtonText \_ No                                   | &No                                       |
| ButtonText \_ OK                                   | OK                                        |
| ButtonText \_ Remove                               | &rimuovere                                   |
| ButtonText \_ Reset                                | &reimpostazione                                    |
| Ripresa \_ di ButtonText                               | &ripresa                                   |
| ButtonText \_ Retry                                | &nuovo tentativo                                    |
| ButtonText \_ Return                               | &return                                   |
| ButtonText \_ Sì                                  | &Sì                                      |
| CompleteSetupIcon                                | completi                                  |
| ComponentDownload                                | ftp://anonymous@microsoft.com/components/ |
| CustomSetupIcon                                  | custicon                                  |
| [**DefaultUIFont**](defaultuifont.md)           | DlgFont8                                  |
| DialogBitmap                                     | dlgbmp                                    |
| DlgTitleFont                                     | {&DlgFontBold8}                           |
| ErrorDialog                                      | ErrorDlg                                  |
| Punto esclamativoIcon                                  | esclamamic                                  |
| Falso                                            | 0                                         |
| Iagree                                           | No                                        |
| InfoIcon                                         | info                                      |
| InstallerIcon                                    | insticon                                  |
| [**INSTALLLEVEL**](installlevel.md)             | 3                                         |
| InstallMode                                      | Typical (Tipica)                                   |
| [**Produttore**](manufacturer.md)             | Microsoft                                 |
| [**PIDTemplate**](pidtemplate.md)               | 12345<\#\#\#-%%%%%%%>@@@@@          |
| [**ProductCode**](productcode.md)               | {34CF587C-1D8F-4DD5-ADFE-440F4B593987}    |
| [**Productid**](productid.md)                   | Nessuno                                      |
| [**ProductLanguage**](productlanguage.md)       | 1033                                      |
| [**ProductName**](productname.md)               | MNP2001                                   |
| [**ProductVersion**](productversion.md)         | 01.50.0000                                |
| Stato1                                        | Installazione                                |
| Stato2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | repairic                                  |
| Eseguire la configurazione                                            | Eseguire la configurazione                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Procedura guidata                                           | Installazione guidata                              |
| SecureCustomProperties                           | OLDAPPFOUND                               |



 

[Continua](updating-sequence-tables-for-an-upgrade.md)

 

 



