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
# <a name="multi_sector_header-structure"></a><span data-ttu-id="64d74-103">\_Struttura di \_ intestazione multisettore</span><span class="sxs-lookup"><span data-stu-id="64d74-103">MULTI\_SECTOR\_HEADER structure</span></span>

<span data-ttu-id="64d74-104">\[Questa struttura è valida solo per la versione 3 dei volumi NTFS. potrebbe essere modificato nelle versioni future.\]</span><span class="sxs-lookup"><span data-stu-id="64d74-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="64d74-105">Rappresenta l'intestazione multisettore.</span><span class="sxs-lookup"><span data-stu-id="64d74-105">Represents the multisector header.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d74-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64d74-106">Syntax</span></span>


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a><span data-ttu-id="64d74-107">Members</span><span class="sxs-lookup"><span data-stu-id="64d74-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="64d74-108">**Firma**</span><span class="sxs-lookup"><span data-stu-id="64d74-108">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="64d74-109">Firma.</span><span class="sxs-lookup"><span data-stu-id="64d74-109">The signature.</span></span> <span data-ttu-id="64d74-110">Questo valore rappresenta un vantaggio per l'utente.</span><span class="sxs-lookup"><span data-stu-id="64d74-110">This value is a convenience to the user.</span></span>

</dd> <dt>

<span data-ttu-id="64d74-111">**UpdateSequenceArrayOffset**</span><span class="sxs-lookup"><span data-stu-id="64d74-111">**UpdateSequenceArrayOffset**</span></span>
</dt> <dd>

<span data-ttu-id="64d74-112">Offset della matrice della sequenza di aggiornamento, dall'inizio della struttura.</span><span class="sxs-lookup"><span data-stu-id="64d74-112">The offset to the update sequence array, from the start of this structure.</span></span> <span data-ttu-id="64d74-113">La matrice di sequenza di aggiornamento deve terminare prima dell'ultimo valore USHORT nel primo settore.</span><span class="sxs-lookup"><span data-stu-id="64d74-113">The update sequence array must end before the last USHORT value in the first sector.</span></span>

</dd> <dt>

<span data-ttu-id="64d74-114">**UpdateSequenceArraySize**</span><span class="sxs-lookup"><span data-stu-id="64d74-114">**UpdateSequenceArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="64d74-115">Dimensioni in byte della matrice di sequenza di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="64d74-115">The size of the update sequence array, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64d74-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="64d74-116">Remarks</span></span>

<span data-ttu-id="64d74-117">Si noti che non è presente alcun file di intestazione associato per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="64d74-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="64d74-118">Questa definizione di struttura è valida solo per la versione principale 3 e secondaria 0 o 1, come indicato [**da \_ FSCTL \_ ottenere \_ \_ i dati del volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="64d74-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="64d74-119">L'intestazione multisettore e la matrice di sequenze di aggiornamento forniscono il rilevamento di trasferimenti multisettore incompleti per i dispositivi che hanno una dimensione di settore fisico maggiore o uguale a stride numero di sequenza (512) o che non trasferiscono settori fuori ordine.</span><span class="sxs-lookup"><span data-stu-id="64d74-119">The multisector header and update sequence array provide detection of incomplete multisector transfers for devices that either have a physical sector size greater than or equal to the sequence number stride (512) or that do not transfer sectors out of order.</span></span> <span data-ttu-id="64d74-120">Se esiste un dispositivo con dimensioni di settore inferiori rispetto allo stride dei numeri di sequenza e a volte trasferisce i settori non ordinati, la matrice di sequenze di aggiornamento non fornirà il rilevamento assoluto dei trasferimenti incompleti.</span><span class="sxs-lookup"><span data-stu-id="64d74-120">If a device exists that has a sector size smaller than the sequence number stride and it sometimes transfers sectors out of order, then the update sequence array will not provide absolute detection of incomplete transfers.</span></span> <span data-ttu-id="64d74-121">Lo stride numero di sequenza è impostato su un numero sufficientemente basso per garantire la protezione assoluta per tutti i dischi rigidi noti.</span><span class="sxs-lookup"><span data-stu-id="64d74-121">The sequence number stride is set to a small enough number to provide absolute protection for all known hard disks.</span></span> <span data-ttu-id="64d74-122">Non viene impostata alcuna dimensione minore o potrebbe essere presente un sovraccarico eccessivo dello spazio o del tempo di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="64d74-122">It is not set any smaller or there might be excessive run time or space overhead.</span></span>

<span data-ttu-id="64d74-123">La matrice di sequenza di aggiornamento è costituita da una matrice di *n* valori **ushort** , dove *n* è la dimensione della struttura protetta divisa per lo stride del numero di sequenza.</span><span class="sxs-lookup"><span data-stu-id="64d74-123">The update sequence array consists of an array of *n* **USHORT** values, where *n* is the size of the structure being protected divided by the sequence number stride.</span></span> <span data-ttu-id="64d74-124">La prima parola contiene il numero di sequenza di aggiornamento, ovvero un contatore ciclico del numero di volte in cui la struttura contenitore è stata scritta su disco.</span><span class="sxs-lookup"><span data-stu-id="64d74-124">The first word contains the update sequence number, which is a cyclical counter of the number of times the containing structure has been written to disk.</span></span> <span data-ttu-id="64d74-125">Di seguito sono riportati i valori **ushort** *salvati che* sono stati sovrascritti dal numero di sequenza dell'aggiornamento l'ultima volta in cui la struttura contenitore è stata scritta su disco.</span><span class="sxs-lookup"><span data-stu-id="64d74-125">Next are the *n* saved **USHORT** values that were overwritten by the update sequence number the last time the containing structure was written to disk.</span></span>

<span data-ttu-id="64d74-126">Ogni volta che la struttura protetta sta per essere scritta su disco, l'ultima parola in ogni stride numero di sequenza viene salvata nella rispettiva posizione nella matrice di numeri di sequenza, quindi viene sovrascritta con il numero di sequenza di aggiornamento successivo.</span><span class="sxs-lookup"><span data-stu-id="64d74-126">Each time the protected structure is about to be written to disk, the last word in each sequence number stride is saved to its respective position in the sequence number array, then it is overwritten with the next update sequence number.</span></span> <span data-ttu-id="64d74-127">Dopo la scrittura o ogni volta che viene letta la struttura, la parola salvata dalla matrice di numeri di sequenza viene ripristinata nella posizione effettiva nella struttura.</span><span class="sxs-lookup"><span data-stu-id="64d74-127">After the write, or whenever the structure is read, the saved word from the sequence number array is restored to its actual position in the structure.</span></span> <span data-ttu-id="64d74-128">Prima di ripristinare le parole salvate durante le operazioni di lettura, tutti i numeri di sequenza alla fine di ogni stride vengono confrontati con il numero di sequenza effettivo all'inizio della matrice.</span><span class="sxs-lookup"><span data-stu-id="64d74-128">Before restoring the saved words on reads, all the sequence numbers at the end of each stride are compared with the actual sequence number at the start of the array.</span></span> <span data-ttu-id="64d74-129">Se uno di questi confronti non è uguale, è stato rilevato un trasferimento multisettore non riuscito.</span><span class="sxs-lookup"><span data-stu-id="64d74-129">If any of these comparisons are not equal, then a failed multisector transfer has been detected.</span></span>

<span data-ttu-id="64d74-130">Le dimensioni della matrice sono determinate dalla dimensione della struttura che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="64d74-130">The size of the array is determined by the size of the containing structure.</span></span> <span data-ttu-id="64d74-131">La matrice della sequenza di aggiornamento deve essere inclusa alla fine dell'intestazione della struttura che protegge a causa delle dimensioni della variabile.</span><span class="sxs-lookup"><span data-stu-id="64d74-131">The update sequence array should be included at the end of the header of the structure it is protecting because of its variable size.</span></span> <span data-ttu-id="64d74-132">L'utente deve assicurarsi che sia riservato lo spazio corretto per la struttura che lo contiene: (dimensione della struttura/512 + 1) \* sizeof (ushort).</span><span class="sxs-lookup"><span data-stu-id="64d74-132">The user must ensure that the correct space is reserved for the containing structure: (size of structure / 512 + 1) \* sizeof(USHORT).</span></span>

## <a name="see-also"></a><span data-ttu-id="64d74-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64d74-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d74-134">Tabella file master</span><span class="sxs-lookup"><span data-stu-id="64d74-134">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
