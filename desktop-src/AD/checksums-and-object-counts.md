---
title: Checksum e conteggi degli oggetti
description: Checksum e conteggi di oggetti sono strategie di rilevamento che consentono a un'applicazione di rilevare uno stato di aggiornamento parziale.
ms.assetid: 14829a74-c186-4250-beac-036c5ecc5913
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc643ec7cd896a7c73df0be5738887a330392140
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470755"
---
# <a name="checksums-and-object-counts"></a><span data-ttu-id="c0551-103">Checksum e conteggi degli oggetti</span><span class="sxs-lookup"><span data-stu-id="c0551-103">Checksums and Object Counts</span></span>

<span data-ttu-id="c0551-104">Checksum e conteggi di oggetti sono strategie di rilevamento che consentono a un'applicazione di rilevare uno stato di aggiornamento parziale.</span><span class="sxs-lookup"><span data-stu-id="c0551-104">Checksums and object counts are detection strategies that allow an application to detect a partial update state.</span></span> <span data-ttu-id="c0551-105">I checksum possono anche essere usati per rilevare le incoerenze introdotte dalla risoluzione dei conflitti.</span><span class="sxs-lookup"><span data-stu-id="c0551-105">Checksums can also be used to detect inconsistencies introduced by collision resolution.</span></span> <span data-ttu-id="c0551-106">Sia i valori di checksum che i conteggi degli oggetti richiedono una posizione in cui archiviare il valore usato per verificare un checksum o un conteggio oggetti.</span><span class="sxs-lookup"><span data-stu-id="c0551-106">Both checksums and object counts require a place to store the value used for verifying a checksum or object count.</span></span> <span data-ttu-id="c0551-107">Può trovarsi in un oggetto "Master" scelto tra quelli interessati dalla relazione specifica dell'applicazione o in un oggetto padre in cui sono archiviati gli oggetti correlati.</span><span class="sxs-lookup"><span data-stu-id="c0551-107">This can be on a "master" object chosen from among those involved in the application-specific relationship or on a parent object under which the related objects are stored.</span></span>

<span data-ttu-id="c0551-108">Per i checksum, le applicazioni che leggono gli oggetti correlati verificano il checksum calcolando un risultato locale e confrontandolo con il valore archiviato.</span><span class="sxs-lookup"><span data-stu-id="c0551-108">For checksums, applications reading the related objects verify the checksum by calculating a local result and comparing it with the stored value.</span></span> <span data-ttu-id="c0551-109">Se i valori non corrispondono, la replica si trova in uno stato di aggiornamento parziale e gli oggetti non possono essere utilizzati.</span><span class="sxs-lookup"><span data-stu-id="c0551-109">If the values do not match, the replica is in a partial update state and the objects cannot be used.</span></span>

<span data-ttu-id="c0551-110">Per i conteggi di oggetti, le applicazioni contano gli oggetti correlati, in genere figli di un singolo elemento padre, e confrontano il numero con il valore archiviato.</span><span class="sxs-lookup"><span data-stu-id="c0551-110">For object counts, applications count the related objects (typically children of a single parent) and compare the count with the stored value.</span></span> <span data-ttu-id="c0551-111">Se i conteggi non corrispondono, la replica si trova in uno stato di aggiornamento parziale e gli oggetti non possono essere utilizzati.</span><span class="sxs-lookup"><span data-stu-id="c0551-111">If the counts do not match, the replica is in a partial update state and the objects cannot be used.</span></span>

<span data-ttu-id="c0551-112">Alcune considerazioni importanti:</span><span class="sxs-lookup"><span data-stu-id="c0551-112">Some important considerations:</span></span>

-   <span data-ttu-id="c0551-113">Per il corretto funzionamento dell'approccio con checksum, è necessario aggiornare uno o più attributi usati nel calcolo del checksum.</span><span class="sxs-lookup"><span data-stu-id="c0551-113">For the checksum approach to work, the one or more attributes used in computing the checksum must be updated.</span></span> <span data-ttu-id="c0551-114">L'algoritmo utilizzato per calcolare il checksum deve riflettere in modo affidabile le differenze nell'input.</span><span class="sxs-lookup"><span data-stu-id="c0551-114">The algorithm used to compute the checksum must reliably reflect differences in input.</span></span> <span data-ttu-id="c0551-115">Se molti input diversi hanno prodotto lo stesso checksum, l'algoritmo non rileva in modo affidabile gli aggiornamenti parziali.</span><span class="sxs-lookup"><span data-stu-id="c0551-115">If many different inputs product the same checksum, the algorithm will not reliably detect partial updates.</span></span> <span data-ttu-id="c0551-116">È utile anche il "salting" dell'input con valori come **objectGUID** del computer di origine e la data e l'ora dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c0551-116">"Salting" the input with values like the **objectGUID** of the source computer and the date and time of the update is also helpful.</span></span>
-   <span data-ttu-id="c0551-117">Il conteggio degli oggetti funziona meglio se usato con nuovi set di oggetti o in combinazione con GUID di coerenza (vedere la sezione successiva per altre informazioni).</span><span class="sxs-lookup"><span data-stu-id="c0551-117">Object counts work best when used with new sets of objects, or in combination with consistency GUIDs (see the next section for more information).</span></span> <span data-ttu-id="c0551-118">È necessario che l'applicazione che esegue l'aggiornamento conosca, in anticipo, il numero di oggetti che si troveranno nel contenitore quando l'aggiornamento viene completato o che usi un altro mezzo per contrassegnare il contenitore come non valido durante l'aggiornamento, ad esempio impostando il conteggio su zero.</span><span class="sxs-lookup"><span data-stu-id="c0551-118">The application performing the update must either know, in advance, the number of objects that will be in the container when the update is completed or use some other means of marking the container invalid while the update proceeds (for example, setting the count to zero).</span></span> <span data-ttu-id="c0551-119">Al termine dell'aggiornamento, l'applicazione di origine contrassegna il contenitore con il numero di oggetti contenuti.</span><span class="sxs-lookup"><span data-stu-id="c0551-119">After completing the update the source application marks the container with the count of objects contained.</span></span>

 

 




