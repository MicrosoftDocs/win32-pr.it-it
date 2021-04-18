---
description: In questo argomento viene descritta la struttura di un file di formato Advanced Systems (ASF).
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Struttura di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524673"
---
# <a name="asf-file-structure"></a>Struttura di file ASF

In questo argomento viene descritta la struttura di un file di formato Advanced Systems (ASF).

Per informazioni dettagliate sui file ASF, scaricare la [specifica ASF](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea). È inoltre possibile utilizzare lo strumento [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) per visualizzare la struttura di un file ASF esistente.

L'unità di base dell'organizzazione per i file ASF è denominata *oggetto*. Un oggetto file ASF contiene i dati seguenti.



| Data                                                        | Dimensione     |
|-------------------------------------------------------------|----------|
| GUID che identifica l'oggetto.                          | 128 bit |
| Dimensione dell'oggetto.                                     | 64 bit. |
| Dati dell'oggetto. I dati dell'oggetto possono contenere altri oggetti ASF. | Variabile.  |



 

> [!Note]  
> Un oggetto file ASF è semplicemente un blocco di dati. Non si tratta di un oggetto nel senso della programmazione del computer.

 

Un file ASF contiene tre tipi di oggetti file di primo livello.



| Oggetto file ASF                                                                                                                      | Descrizione                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Oggetto Header<br/>         | Contiene informazioni sul file ASF.<br/>  |
| <span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Oggetto dati<br/>                     | Contiene pacchetti di dati multimediali.<br/>           |
| <span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Oggetti indice<br/> | Contiene uno o più indici. Facoltativo.<br/> |



 

Nel diagramma seguente viene illustrata la struttura del file ASF.

![diagramma che illustra la struttura dei file ASF, inclusi gli elementi all'interno dell'intestazione, dei dati e dell'indice](images/asf-components04.png)

Il diagramma non viene disegnato per la scalabilità. in genere l'oggetto dati comprende la maggior parte del file.

### <a name="header-object"></a>Oggetto Header

L'oggetto Header è obbligatorio e viene visualizzato all'inizio di ogni file ASF. Contiene attributi di file globali e informazioni sui flussi nel file ASF. Queste informazioni vengono usate per interpretare e riprodurre i dati nel file.

L'oggetto header contiene diversi oggetti secondari madatory:

-   L'oggetto proprietà file descrive gli attributi globali del file, ad esempio le dimensioni del file, la durata della riproduzione, il numero di pacchetti di dati, le dimensioni minime e massime del pacchetto e la velocità in bit massima.
-   L'oggetto estensione dell'intestazione consente di aggiungere funzionalità aggiuntive a un file ASF mantenendo la compatibilità con le versioni precedenti.
-   L'oggetto proprietà del flusso descrive un flusso nel file. Un file ASF deve contenere almeno un flusso e pertanto almeno un oggetto proprietà del flusso.

L'oggetto Header può contenere informazioni facoltative aggiuntive, inclusi i metadati sul file (ad esempio titolo e autore), un elenco dei codec usati per codificare il file e le informazioni sulla protezione del contenuto.

### <a name="data-object"></a>Oggetto dati

L'oggetto dati ASF contiene tutti i dati multimediali per il file ASF. Questo oggetto è obbligatorio e deve seguire l'oggetto intestazione ASF.

L'oggetto dati è suddiviso in *pacchetti* di dati. Ogni pacchetto contiene dati per uno o più flussi del file. Un pacchetto di dati contiene un'intestazione del pacchetto di dati che fornisce informazioni sull'analisi dei pacchetti, seguite dai dati del payload, ovvero i dati effettivi dei supporti digitali. A tutti i pacchetti di dati è associato un tempo di presentazione e sono disposti nell'ordine in cui sono stati ricevuti.

Le informazioni sul contenuto dell'oggetto dati, ad esempio le dimensioni del pacchetto e il numero di pacchetti, vengono archiviate nell'oggetto intestazione.

### <a name="index-object"></a>Oggetto index

L'oggetto index è facoltativo ed è l'ultimo oggetto nel file ASF. Un file ASF può contenere più di un oggetto index. L'oggetto index fornisce accesso casuale basato sul tempo nell'oggetto dati ASF.

Un oggetto indice semplice è un altro tipo di indice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




