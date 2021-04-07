---
description: Rappresenta l'intestazione multisettore.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: Struttura MULTI_SECTOR_HEADER
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
ms.openlocfilehash: ab21e17b83ae25286d2775d9dbd97dfd4cf493bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747882"
---
# <a name="multi_sector_header-structure"></a>\_Struttura di \_ intestazione multisettore

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

Firma. Questo valore rappresenta un vantaggio per l'utente.

</dd> <dt>

**UpdateSequenceArrayOffset**
</dt> <dd>

Offset della matrice della sequenza di aggiornamento, dall'inizio della struttura. La matrice di sequenza di aggiornamento deve terminare prima dell'ultimo valore USHORT nel primo settore.

</dd> <dt>

**UpdateSequenceArraySize**
</dt> <dd>

Dimensioni in byte della matrice di sequenza di aggiornamento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che non è presente alcun file di intestazione associato per questa struttura.

Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

L'intestazione multisettore e la matrice di sequenze di aggiornamento forniscono il rilevamento di trasferimenti multisettore incompleti per i dispositivi che hanno una dimensione di settore fisico maggiore o uguale a stride numero di sequenza (512) o che non trasferiscono settori fuori ordine. Se esiste un dispositivo con dimensioni di settore inferiori rispetto allo stride dei numeri di sequenza e a volte trasferisce i settori non ordinati, la matrice di sequenze di aggiornamento non fornirà il rilevamento assoluto dei trasferimenti incompleti. Lo stride numero di sequenza è impostato su un numero sufficientemente basso per garantire la protezione assoluta per tutti i dischi rigidi noti. Non viene impostata alcuna dimensione minore o potrebbe essere presente un sovraccarico eccessivo dello spazio o del tempo di esecuzione.

La matrice di sequenza di aggiornamento è costituita da una matrice di *n* valori **ushort** , dove *n* è la dimensione della struttura protetta divisa per lo stride del numero di sequenza. La prima parola contiene il numero di sequenza di aggiornamento, ovvero un contatore ciclico del numero di volte in cui la struttura contenitore è stata scritta su disco. Di seguito sono riportati i valori **ushort** *salvati che* sono stati sovrascritti dal numero di sequenza dell'aggiornamento l'ultima volta in cui la struttura contenitore è stata scritta su disco.

Ogni volta che la struttura protetta sta per essere scritta su disco, l'ultima parola in ogni stride numero di sequenza viene salvata nella rispettiva posizione nella matrice di numeri di sequenza, quindi viene sovrascritta con il numero di sequenza di aggiornamento successivo. Dopo la scrittura o ogni volta che viene letta la struttura, la parola salvata dalla matrice di numeri di sequenza viene ripristinata nella posizione effettiva nella struttura. Prima di ripristinare le parole salvate durante le operazioni di lettura, tutti i numeri di sequenza alla fine di ogni stride vengono confrontati con il numero di sequenza effettivo all'inizio della matrice. Se uno di questi confronti non è uguale, è stato rilevato un trasferimento multisettore non riuscito.

Le dimensioni della matrice sono determinate dalla dimensione della struttura che lo contiene. La matrice della sequenza di aggiornamento deve essere inclusa alla fine dell'intestazione della struttura che protegge a causa delle dimensioni della variabile. L'utente deve assicurarsi che sia riservato lo spazio corretto per la struttura che lo contiene: (dimensione della struttura/512 + 1) \* sizeof (ushort).

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tabella file master](master-file-table.md)
</dt> </dl>

 

 
