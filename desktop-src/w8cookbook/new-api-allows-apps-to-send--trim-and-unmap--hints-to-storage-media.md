---
title: Nuova API consente alle app di inviare hint "TRIM e annullare" ai supporti di archiviazione
description: La nuova API consente alle app di inviare \ 0034; TRIM e annullare \ 0034; Suggerimenti per i supporti di archiviazione
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300562"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a>Nuova API consente alle app di inviare hint "TRIM e annullare" ai supporti di archiviazione

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

Gli hint TRIM segnalano all'unità che determinati settori precedentemente allocati non sono più necessari per l'app e possono essere eliminati. Questa operazione viene in genere usata quando un'app esegue allocazioni di spazio di grandi dimensioni tramite un file e quindi gestisce automaticamente le allocazioni al file, ad esempio i file del disco rigido virtuale.

**Che cos'è TRIM?**

Le unità SSD (Solid State Drive) sono in genere dispositivi con cancellazione blocchi basata sulla memoria flash; Ciò significa che quando i dati vengono scritti nell'unità SSD, non possono essere sovrascritti sul posto e devono essere scritti altrove fino a quando il blocco non può essere sottoposto a Garbage Collection. Poiché l'unità SSD non dispone di un meccanismo interno per determinare che determinati blocchi sono stati rimossi e ne sono necessari altri. L'unica volta in cui l'unità SSD può contrassegnare un settore ' Dirty ' è quando viene sovrascritta. In altri casi, ad esempio quando un file viene eliminato, l'unità SSD mantiene questi settori perché l'eliminazione viene eseguita come solo modifica della tabella file master (MFT) e non come operazione a tutti i settori del file. In Windows 7 è stato introdotto un modo standard per comunicare con le unità SSD sui settori che non sono più necessari. Questo comando è definito nella [specifica T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) come comando Trim; NTFS invia il comando TRIM per alcune operazioni inline normali, ad esempio "DeleteFile".

**Altri usi del TRIM nell'ambiente di archiviazione**

Come le unità SSD, le reti San (Storage Area Network) e le nuove implementazioni di spazi software per le funzionalità di Windows 8 utilizzano hint di comando TRIM per gestire gli spazi in ambienti con thin provisioning. Gli spazi San e software allocano le aree di archiviazione in dimensioni maggiori di settori o cluster (da 1 MB a 1 GB). Quando ricevono hint TRIM per la dimensione di allocazione (o maggiore delle dimensioni di allocazione), la SAN/unità SSD può deallocare un'area per liberare spazio per gli altri file. In genere passano tutti gli hint TRIM ai supporti sottostanti (SSD o HDD), in modo che possano utilizzare lo spazio liberato in base alle esigenze. In genere non spostano i dati nelle aree deallocate, né tengono traccia delle aree di riduzione delle aree deallocate (quando l'area è vuota).

Le reti San con thin provisioning usano gli hint TRIM che vengono passati per ridurre il footprint di archiviazione fisico complessivo, riducendo di conseguenza i costi. La [specifica SCSI T10](https://www.t10.org) definisce il comando ' annullare ' (simile al comando Trim); qui il comando è applicabile a tutti i tipi di archiviazione, tra cui HDD, SSD e altri. Il comando annullare consente di rimuovere i blocchi fisici dall'allocazione della SAN.

## <a name="how-to-use-the-new-api"></a>Come usare la nuova API


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



L'eliminazione dei file viene passata tramite il buffer, se possibile, o in modo asincrono (non memorizzato nel buffer) al TRIM del comando IOCTL del dispositivo. Viene eseguito il mapping al comando TRIM per i dispositivi ATA e il comando annullare per i dispositivi SCSI. Il codice per l'eliminazione dei file Invia le aree una alla volta come specificato dagli extent precedenti.

Il TRIM del file non attende il ritorno dal dispositivo, perché i comandi TRIM e annullare sono definiti come hint per il supporto di archiviazione sottostante e i codici restituiti non sono previsti.

**Flusso di lavoro end-to-end:**

1.  Taglia file di chiamata
    1.  TRIM file esamina gli input per gli errori
    2.  Il TRIM del file suddivide gli extent nelle aree LCN
    3.  Il TRIM del file viene arrotondato per eccesso per le aree allineate a mis che vengono passate in TRIM
    4.  Il TRIM del file Elimina le voci della cache correlate alle aree di taglio
    5.  Il TRIM file passa il \_ DSM IOCTL (Trim) per area
2.  Restituzione o errori di eliminazione file
    1.  Il controllo degli errori viene eseguito sulla validità dell'input
    2.  Se solo alcuni degli extent sono validi, viene restituito un errore per la chiamata API completa

**Casi d'uso**

**Disco rigido virtuale (VHD) del consumer montato su un'unità SSD:**

Il disco rigido virtuale viene inizialmente montato sul supporto inutilizzato ' clean '. Quando si usa il disco rigido virtuale, il disco rigido virtuale utilizza parti del supporto di archiviazione per i file e così via. Quando elimina i file nei supporti di archiviazione, questi file non vengono rimossi dall'unità SSD poiché il VHD completo viene archiviato come un unico file nell'unità SSD. L'ambiente Hyper-V chiama il TRIM dei file per tutte le aree eliminate quando si verifica delete-file nell'ambiente VHD. I trim dei file \_ vengono convertiti nell'unità SSD in modo da ottimizzare le prestazioni dell'unità SSD.

**VHD del consumer montato su una SAN con thin provisioning:**

Il disco rigido virtuale viene inizialmente montato in una lastra minima di un ambiente con thin provisioning. Man mano che i file vengono archiviati nel disco rigido virtuale, il footprint di archiviazione del disco rigido virtuale cresce in multipli di lastre. Quando i file vengono rimossi nel disco rigido virtuale, Hyper-V chiama il trim del file alla SAN sottoposta \_ a thin provisioning sottostante. Se i TRIM sono più grandi della granularità di lastra, la SAN può ora rimuovere una lastra e quindi ridurre il footprint del disco rigido virtuale su tale SAN.

Se il disco rigido virtuale è residente in un server basato su Windows 8, l'utilità di ottimizzazione dell'archiviazione invierà anche i TRIM per ridurre il footprint del disco rigido virtuale dall'interno del VHD montato.

## <a name="tests"></a>Test

Nelle versioni precedenti del sistema operativo non sono presenti API confrontabili. L'API effettiva non dovrebbe avere alcun effetto sulle prestazioni, anche se il supporto di archiviazione (se implementato correttamente) può mostrare migliori prestazioni di scrittura. L'API deve essere usata con molta attenzione. solo gli extent non più necessari devono essere passati perché tali extent verranno rimossi definitivamente dal supporto di archiviazione.

## <a name="resources"></a>Risorse

-   [Specifica T13](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [Specifica SCSI T10](https://www.t10.org/)

 

 




