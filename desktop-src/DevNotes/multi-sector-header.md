---
description: Rappresenta l'intestazione multisettore.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: MULTI_SECTOR_HEADER struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e34e23d3d2bf2ecfbc1c668e02c177e4d1516c73acabccc88aa7190ec33e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667218"
---
# <a name="multi_sector_header-structure"></a>Struttura MULTI \_ SECTOR \_ HEADER

\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]

Rappresenta l'intestazione multisettore.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**Firma**
</dt> <dd>

Firma. Questo valore è una comodità per l'utente.

</dd> <dt>

**UpdateSequenceArrayOffset**
</dt> <dd>

Offset della matrice della sequenza di aggiornamento, dall'inizio di questa struttura . La matrice della sequenza di aggiornamento deve terminare prima dell'ultimo valore USHORT nel primo settore.

</dd> <dt>

**UpdateSequenceArraySize**
</dt> <dd>

Dimensioni della matrice della sequenza di aggiornamento, in byte.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non è presente alcun file di intestazione associato per questa struttura.

Questa definizione di struttura è valida solo per la versione principale 3 e la versione secondaria 0 o 1, come segnalato da [**FSCTL \_ GET NTFS VOLUME \_ \_ \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

L'intestazione multisettore e la matrice della sequenza di aggiornamento forniscono il rilevamento dei trasferimenti multisettori incompleti per i dispositivi con dimensioni del settore fisico maggiori o uguali al passo del numero di sequenza (512) o che non trasferiscono i settori in ordine. Se esiste un dispositivo con una dimensione del settore inferiore a quella del numero di sequenza e talvolta trasferisce i settori non in ordine, la matrice della sequenza di aggiornamento non fornirà il rilevamento assoluto dei trasferimenti incompleti. Lo stride del numero di sequenza è impostato su un numero sufficientemente piccolo da fornire protezione assoluta per tutti i dischi rigidi noti. Non è impostato su un valore inferiore o potrebbe verificarsi un sovraccarico eccessivo in fase di esecuzione o spazio.

La matrice della sequenza di aggiornamento è costituita da una matrice di *n* **valori USHORT,** dove *n* è la dimensione della struttura protetta divisa per lo stride del numero di sequenza. La prima parola contiene il numero di sequenza di aggiornamento, ovvero un contatore ciclico del numero di volte in cui la struttura contenitore è stata scritta su disco. Vengono quindi visualizzati *i valori USHORT* salvati n che sono stati sovrascritti dal numero di sequenza di aggiornamento l'ultima volta che la struttura contenitore è stata scritta su disco. 

Ogni volta che la struttura protetta sta per essere scritta su disco, l'ultima parola in ogni stride del numero di sequenza viene salvata nella rispettiva posizione nella matrice dei numeri di sequenza, quindi viene sovrascritta con il numero di sequenza di aggiornamento successivo. Dopo la scrittura o ogni volta che la struttura viene letta, la parola salvata dalla matrice di numeri di sequenza viene ripristinata nella posizione effettiva nella struttura . Prima di ripristinare le parole salvate nelle operazioni di lettura, tutti i numeri di sequenza alla fine di ogni passo vengono confrontati con il numero di sequenza effettivo all'inizio della matrice. Se uno di questi confronti non è uguale, è stato rilevato un trasferimento a più fattori non riuscito.

Le dimensioni della matrice sono determinate dalle dimensioni della struttura contenitore. La matrice della sequenza di aggiornamento deve essere inclusa alla fine dell'intestazione della struttura protetta a causa delle dimensioni variabili. L'utente deve assicurarsi che lo spazio corretto sia riservato per la struttura contenitore: (dimensione della struttura / 512 + 1) \* sizeof(USHORT).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 
