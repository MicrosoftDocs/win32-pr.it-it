---
description: Le azioni personalizzate del ghiaccio comunicano chiamando MsiProcessMessage e inviando un \_ messaggio di tipo utente INSTALLMESSAGE.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Linee guida per i messaggi di ghiaccio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4bee7dbf22184883e49da4d5a5f66f9debb577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966639"
---
# <a name="ice-message-guidelines"></a><span data-ttu-id="2a568-103">Linee guida per i messaggi di ghiaccio</span><span class="sxs-lookup"><span data-stu-id="2a568-103">ICE Message Guidelines</span></span>

<span data-ttu-id="2a568-104">Le azioni personalizzate del ghiaccio comunicano chiamando [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e inviando un \_ messaggio di tipo utente INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="2a568-104">ICE custom actions communicate by calling [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and posting an INSTALLMESSAGE\_USER type message.</span></span>

<span data-ttu-id="2a568-105">Quando si crea una stringa di messaggio per un'azione personalizzata ICE, formattare la stringa come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="2a568-105">When authoring a message string for an ICE custom action, format the string as follows.</span></span>

<span data-ttu-id="2a568-106">*Nome del ghiaccio* <tab> *Tipo* <tab> di messaggio *Descrizione* <tab> di *URL o percorso* <tab> della Guida *Nome tabella* <tab> *Nome colonna* <tab> *Chiave primaria* <tab> *Chiave primaria* <tab> *Chiave primaria* .</span><span class="sxs-lookup"><span data-stu-id="2a568-106">*Name of ICE* <tab> *Message Type* <tab> *Description* <tab> *Help URL or location* <tab> *Table Name* <tab> *Column Name* <tab> *Primary Key* <tab> *Primary Key* <tab> *Primary Key* .</span></span> <span data-ttu-id="2a568-107">.</span><span class="sxs-lookup"><span data-stu-id="2a568-107">.</span></span> <span data-ttu-id="2a568-108">.</span><span class="sxs-lookup"><span data-stu-id="2a568-108">.</span></span> <span data-ttu-id="2a568-109">(ripetere per tutte le chiavi primarie necessarie)</span><span class="sxs-lookup"><span data-stu-id="2a568-109">(repeat for as many primary keys as needed)</span></span>

<span data-ttu-id="2a568-110">I primi tre campi della stringa sono necessari in ogni messaggio.</span><span class="sxs-lookup"><span data-stu-id="2a568-110">The first three fields of the string are required in every message.</span></span>

<span data-ttu-id="2a568-111">Il campo tipo di messaggio specifica se il ghiaccio segnala un errore, un errore, un avviso o un messaggio informativo.</span><span class="sxs-lookup"><span data-stu-id="2a568-111">The Message Type field specifies whether the ICE reports a Failure, Error, Warning, or Informational message.</span></span>



| <span data-ttu-id="2a568-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2a568-112">Value</span></span> | <span data-ttu-id="2a568-113">Tipo di messaggio</span><span class="sxs-lookup"><span data-stu-id="2a568-113">Message type</span></span>                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a568-114">0</span><span class="sxs-lookup"><span data-stu-id="2a568-114">0</span></span>     | <span data-ttu-id="2a568-115">Messaggio di errore che segnala l'errore dell'azione personalizzata ICE.</span><span class="sxs-lookup"><span data-stu-id="2a568-115">Failure message reporting the failure of the ICE custom action.</span></span>                                                                                                       |
| <span data-ttu-id="2a568-116">1</span><span class="sxs-lookup"><span data-stu-id="2a568-116">1</span></span>     | <span data-ttu-id="2a568-117">Segnalazione dei messaggi di errore creazione di un database che determina un comportamento non corretto.</span><span class="sxs-lookup"><span data-stu-id="2a568-117">Error message reporting database authoring that cause incorrect behavior.</span></span>                                                                                             |
| <span data-ttu-id="2a568-118">2</span><span class="sxs-lookup"><span data-stu-id="2a568-118">2</span></span>     | <span data-ttu-id="2a568-119">Avviso che segnala la creazione di un database che causa un comportamento errato in alcuni casi.</span><span class="sxs-lookup"><span data-stu-id="2a568-119">Warning message reporting database authoring that causes incorrect behavior in certain cases.</span></span> <span data-ttu-id="2a568-120">Gli avvisi possono anche segnalare effetti collaterali imprevisti della creazione di database.</span><span class="sxs-lookup"><span data-stu-id="2a568-120">Warnings can also report unexpected side-effects of database authoring.</span></span> |
| <span data-ttu-id="2a568-121">3</span><span class="sxs-lookup"><span data-stu-id="2a568-121">3</span></span>     | <span data-ttu-id="2a568-122">Messaggio informativo.</span><span class="sxs-lookup"><span data-stu-id="2a568-122">Informational message.</span></span>                                                                                                                                                |



 

<span data-ttu-id="2a568-123">Se la guida non è disponibile, il campo URL della guida può essere una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="2a568-123">If help is not available, the Help URL field may be the empty string.</span></span>

<span data-ttu-id="2a568-124">I messaggi di errore e di avviso devono fornire il nome della tabella, il nome della colonna e i campi di chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="2a568-124">Error and Warning messages should provide the Table Name, Column Name, and Primary Key fields.</span></span> <span data-ttu-id="2a568-125">Se uno di questi campi viene omesso, tutti i campi che seguono il primo campo vuoto devono essere esclusi dal messaggio.</span><span class="sxs-lookup"><span data-stu-id="2a568-125">If any of these fields are omitted, all of the fields following the first blank field must be left out of the message.</span></span> <span data-ttu-id="2a568-126">Ad esempio, viene fornito un nome di tabella senza un nome di colonna e chiavi primarie oppure un nome di tabella e viene fornito un nome di colonna senza chiavi primarie.</span><span class="sxs-lookup"><span data-stu-id="2a568-126">For example, a table name is provided without a column name and primary keys or a table name and a column name is provided with no primary keys.</span></span> <span data-ttu-id="2a568-127">Tuttavia, non è possibile utilizzare un nome di colonna e chiavi primarie senza un nome di tabella.</span><span class="sxs-lookup"><span data-stu-id="2a568-127">However a column name and primary keys cannot be used without a table name.</span></span> <span data-ttu-id="2a568-128">È possibile che vengano elencate più chiavi primarie fino a quando non sono state assegnate a tutte le chiavi primarie della tabella.</span><span class="sxs-lookup"><span data-stu-id="2a568-128">Multiple primary keys may be listed until all the primary keys in that table have been given values.</span></span>

## <a name="examples"></a><span data-ttu-id="2a568-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="2a568-129">Examples</span></span>

<span data-ttu-id="2a568-130">Il primo messaggio illustrato dal [ghiaccio di esempio in C++](sample-ice-in-c-.md):</span><span class="sxs-lookup"><span data-stu-id="2a568-130">The first message illustrated by the [Sample ICE in C++](sample-ice-in-c-.md):</span></span>

<span data-ttu-id="2a568-131">"ICE01 \\ T3 \\ tcreato 04/29/1998 <inserire il nome dell'autore qui>".</span><span class="sxs-lookup"><span data-stu-id="2a568-131">"ICE01\\t3\\tCreated 04/29/1998 by <insert author's name here>."</span></span>

<span data-ttu-id="2a568-132">Secondo messaggio inviato dal ghiaccio di esempio:</span><span class="sxs-lookup"><span data-stu-id="2a568-132">The second message posted by the sample ICE:</span></span>

<span data-ttu-id="2a568-133">"ICE01 \\ T3 \\ tLast modificato 05/06/1999 da <inserire il nome dell'autore qui>".</span><span class="sxs-lookup"><span data-stu-id="2a568-133">"ICE01\\t3\\tLast modified 05/06/1999 by <insert author's name here>."</span></span>

<span data-ttu-id="2a568-134">Terzo messaggio inviato dall'esempio ICE.</span><span class="sxs-lookup"><span data-stu-id="2a568-134">The third message posted by the sample ICE.</span></span>

<span data-ttu-id="2a568-135">"ICE01 \\ T3 \\ tSimple Ice per illustrare il concetto di ghiaccio".</span><span class="sxs-lookup"><span data-stu-id="2a568-135">"ICE01\\t3\\tSimple ICE to illustrating the ICE concept".</span></span>

 

 



