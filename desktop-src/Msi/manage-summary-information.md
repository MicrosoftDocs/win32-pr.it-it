---
description: Il file VBScript WiSumInf.vbs disponibile in Windows SDK Components for Windows Installer Developers. Questo script di esempio può essere usato per gestire il flusso di informazioni di riepilogo di un pacchetto Windows Installer.
ms.assetid: f7f1cf89-f211-4511-8260-b48c898c1cf6
title: Gestire le informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf5ad72ee4f308831077ec2f732b92a70f407c560b204d10f2d3db63d1bb9bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926971"
---
# <a name="manage-summary-information"></a>Gestire le informazioni di riepilogo

Il file VBScript WiSumInf.vbs in Windows [SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio può essere usato per gestire il flusso [di informazioni di riepilogo](summary-information-stream.md) di un pacchetto Windows Installer.

L'esempio illustra l'uso di:

-   [**Proprietà SummaryInformation (oggetto Installer)**](installer-summaryinformation.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) [ **dell'oggetto Installer**](installer-object.md)

L'uso di questo esempio richiede CScript.exe o WScript.exe versione di Windows Script Host. Per usare CScript.exe eseguire questo esempio, digitare un comando al prompt dei comandi usando la sintassi seguente. La Guida viene visualizzata se il primo argomento è /? o se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con vbs > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se viene richiamata la Guida e 2 se lo script non riesce.

**cscript WiSumInf.vbs \[ percorso del database \] \[ Property=value\]**

Specificare il percorso del database Windows Installer. Se non vengono specificati altri argomenti, lo script elenca tutte le proprietà di riepilogo per il pacchetto. Specificare un elenco di proprietà e valori di riepilogo da aggiornare usando il formato Property=value. È possibile specificare la proprietà con il nome o il valore PID illustrato di seguito. I campi di data e ora usano il formato delle impostazioni locali correnti oppure "Now" o "Date". Per altre informazioni, vedere [Summary Information Stream Property Set](summary-information-stream-property-set.md).



| PID | Nome        | Descrizione                                                                                                                                                                                                                                                                                      |
|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | codepage    | Tabella codici ANSI delle stringhe di testo nelle informazioni di riepilogo. Per altre informazioni, vedere [**Proprietà Summary della tabella**](codepage-summary.md) codici.                                                                                                                                                           |
| 2   | Titolo       | Tipo di Windows programma di installazione. Per altre informazioni, vedere [**Proprietà Riepilogo titolo.**](title-summary.md)                                                                                                                                                                                    |
| 3   | Oggetto     | Nome completo del prodotto . Per altre informazioni, vedere [**Proprietà riepilogo oggetto.**](subject-summary.md)                                                                                                                                                                                               |
| 4   | Autore      | Autore, in genere il nome del fornitore. Per altre informazioni, vedere [**Author Summary Property**](author-summary.md).                                                                                                                                                                                     |
| 5   | Parole chiave    | Elenco di parole chiave per l'uso da parte del browser di file. Per altre informazioni, vedere [**Proprietà Di riepilogo delle parole chiave.**](keywords-summary.md)                                                                                                                                                                       |
| 6   | Commenti    | Descrizione dello scopo o dell'uso del pacchetto. Per altre informazioni, vedere [**Comments Summary Property**](comments-summary.md).                                                                                                                                                                       |
| 7   | Modello    | Piattaforme e linguaggi supportati. Per altre informazioni, vedere [**Proprietà riepilogo modello.**](template-summary.md)                                                                                                                                                                              |
| 8   | LastAuthor  | Impostato solo dal programma di installazione. Per altre informazioni, vedere [**Last Saved By Summary Property**](last-saved-by-summary.md).                                                                                                                                                                            |
| 9   | Revisione    | GUID del codice del pacchetto. Per altre informazioni, vedere [**Proprietà Riepilogo numero revisione**](revision-number-summary.md).                                                                                                                                                                                |
| 11  | Stampato     | Data e ora dell'immagine di installazione. Per altre informazioni, vedere [**Last Printed Summary Property**](last-printed-summary.md).                                                                                                                                                                    |
| 12  | Data di creazione     | Data e ora di creazione del pacchetto. Per altre informazioni, vedere [**Create Time/Date Summary Property**](create-time-date-summary.md).                                                                                                                                                              |
| 13  | Salvato       | Data e ora dell'ultima modifica del pacchetto. Per altre informazioni, vedere [**Last Saved Time/Date Summary Property**](last-saved-time-date-summary.md).                                                                                                                                             |
| 14  | Pagine       | Versione minima del programma di Windows necessario per questo pacchetto. Per altre informazioni, vedere [**Page Count Summary Property**](page-count-summary.md).                                                                                                                                             |
| 15  | Parole       | Tipo di immagine del file di origine. Per altre informazioni, vedere [**Proprietà Riepilogo conteggio parole**](word-count-summary.md). A partire da Windows Installer versione 4.0 in Windows Vista e Windows Server 2008, questa proprietà include bit per specificare se sono necessari privilegi elevati.<br/> |
| 16  | Caratteri  | Usato solo per le trasformazioni. [**Numero di caratteri**](character-count-summary.md).                                                                                                                                                                                                                    |
| 18  | Applicazione | Applicazione associata a questo file, ad esempio "Windows installer". Per altre informazioni, vedere Creazione [**di una proprietà di riepilogo dell'applicazione.**](creating-application-summary.md)                                                                                                                        |
| 19  | Sicurezza    | Impostazione di sicurezza. Per altre informazioni, vedere [**Proprietà Riepilogo sicurezza**](security-summary.md).                                                                                                                                                                                               |



 

Per altri esempi di scripting, vedere Windows [di script del programma di installazione](windows-installer-scripting-examples.md). Per le utilità di esempio che non richiedono Windows Script Host, vedere Windows [Installer Development Tools](windows-installer-development-tools.md).

 

 




