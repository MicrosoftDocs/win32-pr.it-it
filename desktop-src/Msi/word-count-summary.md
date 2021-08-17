---
description: Nelle informazioni di riepilogo di un pacchetto di installazione la proprietà Riepilogo conteggio parole indica il tipo di immagine del file di origine.
ms.assetid: 1eeece25-4f24-4efe-879d-66ebbb6a9391
title: Word Count Summary - proprietà
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb167c50db0894ea658bb93b97bfb9f49362d32cca8976a2ea3ec590b716450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145234"
---
# <a name="word-count-summary-property"></a>Word Count Summary - proprietà

Nelle informazioni di riepilogo di un pacchetto di installazione la proprietà **Riepilogo** conteggio parole indica il tipo di immagine del file di origine. Se questa proprietà non è presente, il valore predefinito è zero (0).

Questa proprietà è un campo di bit. In futuro potrebbero essere aggiunti nuovi bit. Attualmente sono disponibili i bit seguenti.



| bit   | Valore          | Descrizione                                                                                                                                                                                                                                      |
|-------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bit 0 | 0 1<br/> | Nomi di file lunghi. Nomi di file brevi.<br/>                                                                                                                                                                                                    |
| Bit 1 | 0 2<br/> | L'origine non è compressa. L'origine è compressa.<br/>                                                                                                                                                                                         |
| Bit 2 | 0 4<br/> | L'origine è il supporto originale. L'origine è un'immagine amministrativa creata da un'installazione amministrativa.<br/>                                                                                                                                 |
| Bit 3 | 0 8<br/> | Per installare questo pacchetto possono essere necessari privilegi elevati. Per installare questo pacchetto non sono necessari privilegi elevati.<br/> Disponibile a partire Windows Installer versione 4.0 e Windows Vista o Windows Server 2008.<br/> |



 

Questi valori vengono combinati per assegnare **alla proprietà Riepilogo conteggio** parole uno dei valori seguenti che indicano un tipo di immagine del file di origine.



| Valore | Tipo                                                                                                                                                                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Origine originale con nomi di file lunghi. Corrisponde all'albero in [Tabella directory](directory-table.md). Per installare questo pacchetto possono essere necessari privilegi elevati.                                                                                                                                     |
| 1     | Origine originale con nomi di file brevi. Corrisponde all'albero in [Tabella directory](directory-table.md). Per installare questo pacchetto possono essere necessari privilegi elevati.                                                                                                                                    |
| 2     | File di origine compressi con nomi di file lunghi. Consente di ricercare file e file in [Media Table.](media-table.md) Per installare questo pacchetto possono essere necessari privilegi elevati.                                                                                                                   |
| 3     | File di origine compressi con nomi di file brevi. Consente di ricercare file e file in [Media Table.](media-table.md) Per installare questo pacchetto possono essere necessari privilegi elevati.                                                                                                                  |
| 4     | Immagine amministrativa che usa nomi di file lunghi. Corrisponde all'albero in [Tabella directory](directory-table.md). Per installare questo pacchetto possono essere necessari privilegi elevati.                                                                                                                                |
| 5     | Immagine amministrativa con nomi di file brevi. Corrisponde all'albero in [Tabella directory](directory-table.md). Per installare questo pacchetto possono essere necessari privilegi elevati.                                                                                                                               |
| 8     | Per installare questo pacchetto non sono necessari privilegi elevati. Usare questo valore durante la [creazione di pacchetti senza la finestra di dialogo Controllo dell'account utente](authoring-packages-without-the-uac-dialog-box.md). Disponibile a partire Windows Installer versione 4.0 e Windows Vista o Windows Server 2008.<br/> |



 

Si noti che se il pacchetto è contrassegnato come compresso (bit 1 è impostato), il programma di installazione di Windows installa solo i file che si trovano nella radice dell'origine. In questo caso, anche i file contrassegnati come non compressi nella tabella [file](file-table.md) devono trovarsi nella radice per essere installati. Per specificare un'immagine di origine con un file CAB (file compressi) e file non compressi che corrispondono all'albero nella tabella [directory](directory-table.md), contrassegnare il pacchetto come non compresso lasciando bit 1 non impostato (valore =0) nella proprietà **Riepilogo** conteggio parole e impostare **msidbFileAttributesCompressed** (valore=16384) nella colonna Attributi della tabella [file](file-table.md) per ogni file nell'cabinet.

In una trasformazione la proprietà **Riepilogo conteggio** parole deve essere Null.

Nel flusso di informazioni di riepilogo di un pacchetto di patch, la proprietà **Riepilogo** conteggio parole indica la versione minima Windows installer necessaria per installare la patch.



| Valore | Significato                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Valore predefinito, che indica che MSPATCH è stato usato per creare la patch.                                                                                                        |
| 2     | Richiede almeno Windows Installer 1.2 per l'applicazione della patch. Una patch con conteggio parole "2" ha immediatamente esito negativo se usata con una versione del programma di installazione di Windows precedente alla 1.2. |
| 3     | Richiede almeno Windows Installer 2.0 per l'applicazione della patch. Una patch con conteggio parole "3" ha immediatamente esito negativo se usata con una versione del programma di installazione di Windows precedente alla 2.0. |
| 4     | Richiede almeno Windows Installer 3.0 per l'applicazione della patch. Una patch con conteggio parole "4" ha esito negativo se usata con una versione del programma di installazione di Windows precedente alla 3.0.             |
| 5     | Richiede almeno Windows Installer 3.1 per l'applicazione della patch.                                                                                                               |



 

Questa proprietà di riepilogo è REQUIRED.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




