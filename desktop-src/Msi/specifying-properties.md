---
description: Windows Le proprietà del programma di installazione sono variabili globali utilizzate dal programma di installazione durante un'installazione.
ms.assetid: 1c59939b-de0f-4bf4-ab1f-4f1aa2488bfa
title: Specifica delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f538bb354ef793a54f3eb60ddfe7b75b2aa96310abdd8a7331813d887433816
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627801"
---
# <a name="specifying-properties"></a>Specifica delle proprietà

Windows Le proprietà del programma di installazione sono variabili globali utilizzate dal programma di installazione durante un'installazione. Vedere le sezioni in [Proprietà](properties.md). Se nella sezione Importazione di un [database](importing-a-blank-database.md) vuoto è stato usato uisample.msi da Windows Installer SDK, la tabella [Proprietà](property-table.md) nella copia di MNP2000.msi contiene già molte proprietà usate dall'interfaccia utente. In questa sezione si aggiungono altre informazioni alla tabella Proprietà specifica per l'installazione del Blocco note esempio. Vedere anche il [gruppo Tabelle informazioni programma](program-information-tables-group.md).

In ogni pacchetto di installazione sono necessarie cinque proprietà che devono essere aggiornate per l'esempio Blocco note nella tabella [Proprietà](property-table.md) di MNP2000.msi:

-   [**ProductCode**](productcode.md)
-   [**ProductLanguage**](productlanguage.md)
-   [**Produttore**](manufacturer.md)
-   [**ProductVersion**](productversion.md)
-   [**ProductName**](productname.md)

Anche se non è richiesto da tutti i pacchetti di installazione, anche le applicazioni che potrebbero ricevere un aggiornamento in futuro devono avere [**una proprietà UpgradeCode.**](upgradecode.md) Vedere [Preparazione di un'applicazione per gli aggiornamenti principali futuri](preparing-an-application-for-future-major-upgrades.md).

Usare l'editor di database per aprire MNP2000.msi e immettere i dati seguenti nella tabella Proprietà. L'elenco fornisce collegamenti agli argomenti di riferimento per le proprietà predefinite del programma di installazione. I nomi delle proprietà che non sono collegamenti sono proprietà definite dall'autore. Molte delle proprietà importate da uisample.msi sono per l'interfaccia utente di esempio. La sezione successiva Interfaccia utente'esempio di installazione illustra l'interfaccia utente.

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
| [**ProductCode**](productcode.md)               | {18A9233C-0B34-4127-A966-C257386270BC}    |
| [**Productid**](productid.md)                   | Nessuno                                      |
| [**ProductLanguage**](productlanguage.md)       | 1033                                      |
| [**ProductName**](productname.md)               | MNP2000                                   |
| [**ProductVersion**](productversion.md)         | 01.40.0000                                |
| Stato1                                        | Installazione                                |
| Stato2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | repairic                                  |
| Eseguire la configurazione                                            | Eseguire la configurazione                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Procedura guidata                                           | Installazione guidata                              |



 

[Continua](importing-the-installexecutesequence.md)

 

 



