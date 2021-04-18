---
description: Nelle informazioni di riepilogo di un pacchetto di installazione, la proprietà riepilogo Conteggio parole indica il tipo di immagine del file di origine.
ms.assetid: 1eeece25-4f24-4efe-879d-66ebbb6a9391
title: Proprietà riepilogo Conteggio parole
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4200cb946f6948770d0c900c2df651b8fbff11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328747"
---
# <a name="word-count-summary-property"></a>Proprietà riepilogo Conteggio parole

Nelle informazioni di riepilogo di un pacchetto di installazione, la proprietà **riepilogo Conteggio parole** indica il tipo di immagine del file di origine. Se questa proprietà non è presente, il valore predefinito è zero (0).

Questa proprietà è un campo di bit. È possibile aggiungere nuovi bit in futuro. Al momento sono disponibili i seguenti bit.



| bit   | Valore          | Descrizione                                                                                                                                                                                                                                      |
|-------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bit 0 | 0 1<br/> | Nomi file lunghi. Nomi di file brevi.<br/>                                                                                                                                                                                                    |
| Bit 1 | 0 2<br/> | L'origine non è compressa. L'origine è compressa.<br/>                                                                                                                                                                                         |
| Bit 2 | 0 4<br/> | L'origine è il supporto originale. L'origine è un'immagine amministrativa creata da un'installazione amministrativa.<br/>                                                                                                                                 |
| Bit 3 | 0 8<br/> | Per installare il pacchetto, è possibile che siano necessari privilegi elevati. Per installare questo pacchetto non è necessario disporre di privilegi elevati.<br/> Disponibile a partire da Windows Installer versione 4,0, Windows Vista o Windows Server 2008.<br/> |



 

Questi vengono combinati per assegnare alla proprietà di **Riepilogo di Word Count** uno dei valori seguenti che indicano un tipo di immagine del file di origine.



| Valore | Tipo                                                                                                                                                                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Origine originale con nomi di file lunghi. Corrisponde alla struttura ad albero nella [tabella di directory](directory-table.md). Per installare il pacchetto, è possibile che siano necessari privilegi elevati.                                                                                                                                     |
| 1     | Origine originale con nomi di file brevi. Corrisponde alla struttura ad albero nella [tabella di directory](directory-table.md). Per installare il pacchetto, è possibile che siano necessari privilegi elevati.                                                                                                                                    |
| 2     | File di origine compressi con nomi di file lunghi. Corrisponde a file CAB e file nella [tabella dei supporti](media-table.md). Per installare il pacchetto, è possibile che siano necessari privilegi elevati.                                                                                                                   |
| 3     | File di origine compressi con nomi di file brevi. Corrisponde a file CAB e file nella [tabella dei supporti](media-table.md). Per installare il pacchetto, è possibile che siano necessari privilegi elevati.                                                                                                                  |
| 4     | Immagine amministrativa con nomi di file lunghi. Corrisponde alla struttura ad albero nella [tabella di directory](directory-table.md). Per installare il pacchetto, è possibile che siano necessari privilegi elevati.                                                                                                                                |
| 5     | Immagine amministrativa con nomi di file brevi. Corrisponde alla struttura ad albero nella [tabella di directory](directory-table.md). Per installare il pacchetto, è possibile che siano necessari privilegi elevati.                                                                                                                               |
| 8     | Per installare questo pacchetto non è necessario disporre di privilegi elevati. Utilizzare questo valore per [la creazione di pacchetti senza la finestra di dialogo controllo dell'account utente](authoring-packages-without-the-uac-dialog-box.md). Disponibile a partire da Windows Installer versione 4,0, Windows Vista o Windows Server 2008.<br/> |



 

Si noti che se il pacchetto è contrassegnato come compresso (il bit 1 è impostato), il Windows Installer installa solo i file che si trovano nella radice dell'origine. In questo caso, anche i file contrassegnati come non compressi nella [tabella file](file-table.md) devono trovarsi nella radice da installare. Per specificare un'immagine di origine che include sia un file CAB (file compressi) che file non compressi che corrispondono alla struttura ad albero nella [tabella di directory](directory-table.md), contrassegnare il pacchetto come non compresso lasciando il bit 1 non impostato (valore = 0) nella proprietà di riepilogo del **conteggio delle parole** e impostare **msidbFileAttributesCompressed** (valore = 16384) nella colonna attributi della [tabella file](file-table.md) per ogni file nel file CAB.

In una trasformazione la proprietà di **Riepilogo di Word Count** deve essere null.

Nel flusso di informazioni di riepilogo di un pacchetto di patch, la proprietà di **Riepilogo di Word Count** indica la versione minima di Windows Installer necessaria per installare la patch.



| Valore | Significato                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Il valore predefinito, che indica che MSPATCH è stato utilizzato per creare la patch.                                                                                                        |
| 2     | Richiede almeno Windows Installer 1,2 per applicare la patch. Una patch con un numero di parole pari a "2" ha esito negativo immediatamente se utilizzata con una versione Windows Installer precedente alla 1,2. |
| 3     | Richiede almeno Windows Installer 2,0 per applicare la patch. Una patch con un conteggio di parole di "3" ha esito negativo immediatamente se utilizzata con una versione Windows Installer precedente alla 2,0. |
| 4     | Richiede almeno Windows Installer 3,0 per applicare la patch. Una patch con un numero di parole pari a "4" ha esito negativo se utilizzata con una versione di Windows Installer precedente alla 3,0.             |
| 5     | Richiede almeno Windows Installer 3,1 per applicare la patch.                                                                                                               |



 

Questa proprietà di riepilogo è obbligatoria.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Descrizioni delle proprietà di riepilogo](summary-property-descriptions.md)
</dt> </dl>

 

 




