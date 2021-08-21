---
title: La nuova API consente alle app di inviare suggerimenti "TRIM e Unmap" ai supporti di archiviazione
description: La nuova API consente alle app di inviare \ 0034; TRIM e Unmap \ 0034; hint per i supporti di archiviazione
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d79d47dceb5c8bf2e7575836c9a40ddf0347b7e5c616ab4b7196b547742c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028829"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a>La nuova API consente alle app di inviare suggerimenti "TRIM e Unmap" ai supporti di archiviazione

## <a name="platforms"></a>Piattaforme

**Client** : Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

Gli hint TRIM notificano all'unità che determinati settori allocati in precedenza non sono più necessari per l'app e possono essere eliminati. Viene in genere usato quando un'app esegue allocazioni di spazio di grandi dimensioni tramite un file e quindi gestisce automaticamente le allocazioni al file , ad esempio i file del disco rigido virtuale.

**Che cos'è TRIM?**

Le unità SSD sono in genere dispositivi con cancellazione a blocchi basati su memoria flash. Ciò significa che quando i dati vengono scritti nell'SSD, non possono essere sovrascritti e devono essere scritti altrove fino a quando il blocco non può essere sottoposto a Garbage Collection. Poiché l'unità SSD non dispone di un meccanismo interno per determinare che determinati blocchi vengono rimossi e altri sono necessari. L'unica volta che l'SSD può contrassegnare un settore come "dirty" è quando viene sovrascritto. In altri casi, ad esempio quando un file viene eliminato, l'SSD mantiene questi settori perché l'eliminazione viene eseguita solo come modifica della tabella del file master (MFT) e non come operazione per tutti i settori del file. In Windows 7 è stato introdotto un modo standard per comunicare con le SSD i settori che non sono più necessari. Questo comando è definito nella specifica [T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) come comando TRIM. NTFS invia il comando TRIM per alcune normali operazioni inline, ad esempio "deletefile".

**Altri usi di TRIM nel mondo dell'archiviazione**

Come le unità SSD, le reti SAN (Storage Area Network) e le nuove implementazioni di Spazi software di Windows 8 utilizzano hint di comando TRIM per gestire i propri spazi in ambienti con thin provisioning. Le reti SAN e Spazi software allocano aree di archiviazione in dimensioni maggiori di settori o cluster (da 1 MB a 1 GB). Quando ricevono hint TRIM per le dimensioni di allocazione (o superiori alle dimensioni di allocazione), il san/SSD può deallocare un'area per liberare spazio per altri file. In genere passano tutti i suggerimenti TRIM al supporto sottostante (SSD o HDD) in modo che possano utilizzare lo spazio liberato in base alle esigenze. In genere non spostano i dati nelle aree deallocate, né tengono traccia delle aree TRIM in aree deallocate (quando l'area è vuota).

Le reti SAN con thin provisioning usano gli hint TRIM passati per ridurre il footprint complessivo dell'archiviazione fisica, riducendo i costi. La [specifica SCSI T10](https://www.t10.org) definisce il comando "Unmap" (simile al comando TRIM). In questo caso il comando è applicabile a tutti i tipi di archiviazione, inclusi hdd, unità SSD e altri. Il comando UnMap consente di rimuovere i blocchi fisici dall'allocazione della SAN.

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



Il file TRIM viene passato tramite il buffer, se possibile o in modo asincrono (non memorizzato nel buffer) al comando TRIM del DSM IOCTL del dispositivo. Viene eseguito il mapping al comando TRIM per i dispositivi ATA e al comando UnMap per i dispositivi SCSI. Il codice TRIM del file invia le aree una alla volta come specificato dagli extent precedenti.

Il comando TRIM del file non attende i risultati dal dispositivo, perché i comandi TRIM e Unmap sono definiti come hint per i supporti di archiviazione sottostanti e i codici restituiti non sono previsti.

**Flusso di lavoro end-to-end:**

1.  Taglia del file di chiamata
    1.  Il file TRIM esamina gli input per verificare la presenza di errori
    2.  Il comando TRIM del file suddivide gli extent in aree LCN
    3.  Il comando TRIM del file arrotonda per esere le aree non allineate correttamente che vengono passate a TRIM
    4.  Il comando TRIM del file elimina le voci della cache correlate alle aree TRIM
    5.  Il file TRIM passa il DSM IOCTL \_ (Trim) per area
2.  File TRIM restituisce o errori
    1.  Il controllo degli errori viene eseguito sulla validità dell'input
    2.  Se solo alcuni degli extent sono validi, viene restituito un errore per la chiamata API completa

**Casi d'uso**

**Disco rigido virtuale consumer (VHD) montato in un'unità SSD:**

Il disco rigido virtuale viene inizialmente montato su supporti inutilizzati "puliti". Quando viene usato il disco rigido virtuale, il disco rigido virtuale utilizza parti del supporto di archiviazione per i file e così via. Quando elimina i file nel supporto di archiviazione, questi file non vengono rimossi dall'unità SSD perché il disco rigido virtuale completo viene archiviato come un file nel disco SSD. L'ambiente Hyper-V chiama TRIM file per tutte le aree eliminate quando si verifica delete-file nell'ambiente VHD. I \_ TRIM di file vengono convertiti nell'SSD in modo che le prestazioni dell'SSD possano essere ottimizzate.

**Disco rigido virtuale consumer montato in una SAN con thin provisioning:**

Il disco rigido virtuale viene inizialmente montato in una lastra minima di un ambiente con thin provisioning. Man mano che i file vengono archiviati nel disco rigido virtuale, il footprint di archiviazione del disco rigido virtuale aumenta in multipli di dischi rigidi virtuali. Quando i file vengono rimossi nel disco rigido virtuale, Hyper-V chiama TRIM file alla SAN sottostante \_ con thin provisioning. Se i TRIM sono più grandi della granularità SLAB, la san può ora rimuovere una SLAB e di conseguenza ridurre il footprint del disco rigido virtuale su tale SAN.

Se il disco rigido virtuale si trova in un server basato su Windows 8, l'utilità di ottimizzazione di Archiviazione invierà anche LEMS per ridurre il footprint della lastra del disco rigido virtuale dall'interno del disco rigido virtuale montato.

## <a name="tests"></a>Test

Non sono disponibili API simili nelle versioni precedenti del sistema operativo. L'API stessa non dovrebbe avere alcun impatto sulle prestazioni, anche se i supporti di archiviazione (se implementati correttamente) possono mostrare prestazioni di scrittura migliori. L'API deve essere usata con molta attenzione. Solo gli extent non più necessari devono essere passati perché tali extent verranno rimossi definitivamente dal supporto di archiviazione.

## <a name="resources"></a>Risorse

-   [Specifica T13](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [Specifica SCSI T10](https://www.t10.org/)

 

 




