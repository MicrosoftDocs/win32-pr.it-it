---
description: Il file VBScript WiSumInf.vbs viene fornito nei componenti Windows SDK per Windows Installer sviluppatori. Questo script di esempio può essere utilizzato per gestire il flusso di informazioni di riepilogo di un pacchetto di Windows Installer.
ms.assetid: f7f1cf89-f211-4511-8260-b48c898c1cf6
title: Gestione delle informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02ff360bd56dabc57b3a7ffccdba8c4f90346193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049591"
---
# <a name="manage-summary-information"></a>Gestione delle informazioni di riepilogo

Il file VBScript WiSumInf.vbs viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Questo script di esempio può essere utilizzato per gestire il [flusso di informazioni di riepilogo](summary-information-stream.md) di un pacchetto di Windows Installer.

Nell'esempio viene illustrato l'utilizzo di:

-   [**Proprietà SummaryInformation (oggetto Installer)**](installer-summaryinformation.md)
-   [**Metodo LastErrorRecord**](installer-lasterrorrecord.md) dell' [ **oggetto Installer**](installer-object.md)

Per usare questo esempio è necessaria la versione CScript.exe o WScript.exe di Windows script host. Per utilizzare CScript.exe per eseguire questo esempio, digitare un comando al prompt dei comandi utilizzando la sintassi seguente. La guida viene visualizzata se il primo argomento è/? oppure se vengono specificati troppi argomenti. Per reindirizzare l'output a un file, terminare la riga di comando con VBS > \[ *percorso del file* \] . Nell'esempio viene restituito il valore 0 per l'esito positivo, 1 se la guida viene richiamata e 2 se lo script ha esito negativo.

**cscript WiSumInf.vbs \[ percorso della proprietà del database \] \[ = value\]**

Consente di specificare il percorso del database di Windows Installer. Se non viene specificato alcun altro argomento, lo script elenca tutte le proprietà di riepilogo per il pacchetto. Specificare un elenco di proprietà e valori di riepilogo da aggiornare utilizzando il formato Property = Value. È possibile specificare la proprietà in base al nome o al valore PID mostrato di seguito. I campi di data e ora usano il formato delle impostazioni locali corrente oppure "ora" o "data". Per ulteriori informazioni, vedere [set di proprietà del flusso di informazioni di riepilogo](summary-information-stream-property-set.md).



| PID | Nome        | Descrizione                                                                                                                                                                                                                                                                                      |
|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | codepage    | Tabella codici ANSI delle stringhe di testo nelle informazioni di riepilogo. Per ulteriori informazioni, vedere la pagina relativa alla proprietà di [**Riepilogo codepage**](codepage-summary.md) .                                                                                                                                                           |
| 2   | Titolo       | Tipo di pacchetto di Windows Installer. Per altre informazioni, vedere [**proprietà di riepilogo del titolo**](title-summary.md).                                                                                                                                                                                    |
| 3   | Oggetto     | Nome completo del prodotto. Per ulteriori informazioni, vedere [**proprietà Summary**](subject-summary.md).                                                                                                                                                                                               |
| 4   | Autore      | Creator, in genere il nome del fornitore. Per altre informazioni, vedere [**proprietà di riepilogo dell'autore**](author-summary.md).                                                                                                                                                                                     |
| 5   | Parole chiave    | Elenco di parole chiave utilizzabili dal browser file. Per altre informazioni, vedere la [**proprietà Summary di Keywords**](keywords-summary.md).                                                                                                                                                                       |
| 6   | Commenti    | Descrizione dello scopo o dell'utilizzo del pacchetto. Per ulteriori informazioni, vedere la [**proprietà di riepilogo dei commenti**](comments-summary.md).                                                                                                                                                                       |
| 7   | Modello    | Piattaforme e linguaggi supportati. Per altre informazioni, vedere [**proprietà di riepilogo del modello**](template-summary.md).                                                                                                                                                                              |
| 8   | LastAuthor  | Impostato solo dal programma di installazione. Per ulteriori informazioni, vedere [**l'ultimo salvataggio per proprietà di riepilogo**](last-saved-by-summary.md).                                                                                                                                                                            |
| 9   | Revisione    | GUID del codice del pacchetto. Per ulteriori informazioni, vedere la pagina relativa alla [**Proprietà Riepilogo dei numeri di revisione**](revision-number-summary.md).                                                                                                                                                                                |
| 11  | Stampato     | Data e ora dell'immagine di installazione. Per ulteriori informazioni, vedere [**l'ultima proprietà di riepilogo stampata**](last-printed-summary.md).                                                                                                                                                                    |
| 12  | Data di creazione     | Data e ora di creazione del pacchetto. Per altre informazioni, vedere [**creare una proprietà di riepilogo di data e ora**](create-time-date-summary.md).                                                                                                                                                              |
| 13  | Salvato       | Data e ora dell'Ultima modifica del pacchetto. Per ulteriori informazioni, vedere [**proprietà di riepilogo Data e ora dell'ultimo salvataggio**](last-saved-time-date-summary.md).                                                                                                                                             |
| 14  | Pagine       | La versione minima di Windows Installer obbligatoria per il pacchetto. Per altre informazioni, vedere [**proprietà di riepilogo del conteggio delle pagine**](page-count-summary.md).                                                                                                                                             |
| 15  | Parole       | Tipo di immagine del file di origine. Per altre informazioni, vedere [**proprietà di riepilogo dei conteggi di parole**](word-count-summary.md). A partire da Windows Installer versione 4,0 in Windows Vista e Windows Server 2008, questa proprietà include BITS per specificare se sono necessari privilegi elevati.<br/> |
| 16  | Caratteri  | Utilizzato solo per le trasformazioni. [**Numero di caratteri**](character-count-summary.md).                                                                                                                                                                                                                    |
| 18  | Applicazione | Applicazione associata a questo file, ad esempio "Windows Installer". Per altre informazioni, vedere [**creazione**](creating-application-summary.md)di una proprietà di riepilogo delle applicazioni.                                                                                                                        |
| 19  | Sicurezza    | Impostazione di sicurezza. Per ulteriori informazioni, vedere [**Proprietà Riepilogo sicurezza**](security-summary.md).                                                                                                                                                                                               |



 

Per altri esempi di script, vedere [Windows Installer esempi di scripting](windows-installer-scripting-examples.md). Per utilità di esempio che non richiedono Windows script host, vedere [Windows Installer strumenti di sviluppo](windows-installer-development-tools.md).

 

 




