---
description: Gli sviluppatori di database di installazione devono essere a conoscenza di due limitazioni sulla gestione dei flussi da parte dell'implementazione dell'archiviazione strutturata OLE Win32.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Limitazioni OLE sui flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226446"
---
# <a name="ole-limitations-on-streams"></a><span data-ttu-id="8a449-103">Limitazioni OLE sui flussi</span><span class="sxs-lookup"><span data-stu-id="8a449-103">OLE Limitations on Streams</span></span>

<span data-ttu-id="8a449-104">Gli sviluppatori di database di installazione devono essere a conoscenza di due limitazioni sulla gestione dei flussi da parte dell'implementazione dell'archiviazione strutturata OLE Win32.</span><span class="sxs-lookup"><span data-stu-id="8a449-104">Developers of installation databases need to be aware of two limitations on the handling of streams by the Win32 OLE structured storage implementation.</span></span> <span data-ttu-id="8a449-105">Queste limitazioni possono influenzare indirettamente le funzioni del programma di installazione tramite trasformazioni e altri dati che possono essere archiviati nel database come flusso.</span><span class="sxs-lookup"><span data-stu-id="8a449-105">These limitations can affect installer functions indirectly through transforms and other data that may be stored in the database as a stream.</span></span>

<span data-ttu-id="8a449-106">Esistono due limitazioni rilevanti:</span><span class="sxs-lookup"><span data-stu-id="8a449-106">There are two relevant limitations:</span></span>

-   <span data-ttu-id="8a449-107">I dati binari vengono archiviati con un nome di indice creato concatenando il nome della tabella e i valori delle chiavi primarie del record utilizzando un delimitatore di punto.</span><span class="sxs-lookup"><span data-stu-id="8a449-107">Binary data is stored with an index name created by concatenating the table name and the values of the record's primary keys using a period delimiter.</span></span> <span data-ttu-id="8a449-108">OLE limita i nomi di flusso a 32 caratteri (31 + terminatore null).</span><span class="sxs-lookup"><span data-stu-id="8a449-108">OLE limits stream names to 32 characters (31 + null terminator).</span></span> <span data-ttu-id="8a449-109">Windows Installer usa un algoritmo di compressione che può espandere il limite di 62 caratteri a seconda del carattere.</span><span class="sxs-lookup"><span data-stu-id="8a449-109">Windows Installer uses a compression algorithm that can expand the limit to 62 characters depending upon the character.</span></span> <span data-ttu-id="8a449-110">Si noti che i caratteri a byte doppio vengono conteggiati come 2.</span><span class="sxs-lookup"><span data-stu-id="8a449-110">Note that double-byte characters count as 2.</span></span>
-   <span data-ttu-id="8a449-111">Sebbene sia possibile avere più flussi aperti contemporaneamente, non è possibile aprire un flusso una seconda volta fino a quando non viene chiuso il primo riferimento.</span><span class="sxs-lookup"><span data-stu-id="8a449-111">Although you can have multiple streams open at one time, you cannot open a stream a second time until the first reference is closed.</span></span> <span data-ttu-id="8a449-112">Ciò significa che non è possibile selezionare lo stesso flusso di dati binario da aprire simultaneamente in più record.</span><span class="sxs-lookup"><span data-stu-id="8a449-112">This means you cannot select the same binary data stream to be open in multiple records simultaneously.</span></span> <span data-ttu-id="8a449-113">Il tentativo di leggere i dati binari dal secondo record ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8a449-113">Attempts to read the binary data from the second record fail.</span></span> <span data-ttu-id="8a449-114">Non è inoltre possibile rinominare le chiavi primarie di un record mentre un flusso di dati binari in tale record è aperto.</span><span class="sxs-lookup"><span data-stu-id="8a449-114">Also you cannot rename the primary keys of a record while a binary data stream in that record is open.</span></span>

 

 



