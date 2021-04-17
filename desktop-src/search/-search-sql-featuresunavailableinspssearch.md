---
description: Il linguaggio di query di Microsoft Windows Search è basato su Structured Query Language (SQL); Tuttavia, non esegue la ricerca in un database relazionale con indici o tabelle definite dall'utente.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: Funzionalità SQL non disponibili in Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306131"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a><span data-ttu-id="20a84-103">Funzionalità SQL non disponibili in Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="20a84-103">SQL Features Unavailable in Microsoft Windows Search</span></span>

<span data-ttu-id="20a84-104">Il linguaggio di query di Microsoft Windows Search è basato su Structured Query Language (SQL); Tuttavia, non esegue la ricerca in un database relazionale con indici o tabelle definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="20a84-104">Microsoft Windows Search query language is based on Structured Query Language (SQL); however, it does not search in a relational database with user-defined tables or indexes.</span></span> <span data-ttu-id="20a84-105">Per questo motivo, molte istruzioni SQL standard e funzionalità di sintassi non si applicano.</span><span class="sxs-lookup"><span data-stu-id="20a84-105">Because of this, many standard SQL statements and syntax features do not apply.</span></span> <span data-ttu-id="20a84-106">Di seguito è riportato un elenco delle funzionalità SQL più significative che non sono supportate in Windows Search.</span><span class="sxs-lookup"><span data-stu-id="20a84-106">The following is a list of the more significant SQL features that are not supported in Windows Search.</span></span>


-   <span data-ttu-id="20a84-107">Istruzioni BATCH</span><span class="sxs-lookup"><span data-stu-id="20a84-107">BATCH statements</span></span>
-   <span data-ttu-id="20a84-108">Funzione COALESCE \_ Table</span><span class="sxs-lookup"><span data-stu-id="20a84-108">COALESCE\_TABLE function</span></span>
-   <span data-ttu-id="20a84-109">Funzione CONVERT (usare invece le funzioni CAST)</span><span class="sxs-lookup"><span data-stu-id="20a84-109">CONVERT function (use the CAST functions instead)</span></span>
-   <span data-ttu-id="20a84-110">CREATE VIEW - istruzione</span><span class="sxs-lookup"><span data-stu-id="20a84-110">CREATE VIEW statement</span></span>
-   <span data-ttu-id="20a84-111">Linguaggio di definizione dei dati</span><span class="sxs-lookup"><span data-stu-id="20a84-111">Data definition language</span></span>
-   <span data-ttu-id="20a84-112">DATASOURCE (istruzione)</span><span class="sxs-lookup"><span data-stu-id="20a84-112">DATASOURCE statement</span></span>
-   <span data-ttu-id="20a84-113">Formati di data e ora diversi dall'indicatore di data e ora ISO</span><span class="sxs-lookup"><span data-stu-id="20a84-113">Date and Time formats other than ISO date and time stamp</span></span>
-   <span data-ttu-id="20a84-114">Istruzione DELETE</span><span class="sxs-lookup"><span data-stu-id="20a84-114">DELETE statement</span></span>
-   <span data-ttu-id="20a84-115">GRANT - istruzione</span><span class="sxs-lookup"><span data-stu-id="20a84-115">GRANT statement</span></span>
-   <span data-ttu-id="20a84-116">Schema informazioni</span><span class="sxs-lookup"><span data-stu-id="20a84-116">Information schema</span></span>
-   <span data-ttu-id="20a84-117">Istruzione INSERT</span><span class="sxs-lookup"><span data-stu-id="20a84-117">INSERT statement</span></span>
-   <span data-ttu-id="20a84-118">Tipi di dati OLE DB</span><span class="sxs-lookup"><span data-stu-id="20a84-118">OLE DB data types</span></span>
-   <span data-ttu-id="20a84-119">Espressioni regolari SQL-standard (usare invece CONTAINs o LIKE)</span><span class="sxs-lookup"><span data-stu-id="20a84-119">SQL-standard regular expressions (use CONTAINS or LIKE instead)</span></span>
-   <span data-ttu-id="20a84-120">Parametri per le query SQL</span><span class="sxs-lookup"><span data-stu-id="20a84-120">Parameters to SQL queries</span></span>
-   <span data-ttu-id="20a84-121">Confronto tra colonne relazionali</span><span class="sxs-lookup"><span data-stu-id="20a84-121">Relational column comparison</span></span>
-   <span data-ttu-id="20a84-122">Intestazione ID Revisione</span><span class="sxs-lookup"><span data-stu-id="20a84-122">Revision ID header</span></span>
-   <span data-ttu-id="20a84-123">REVOKE - istruzione</span><span class="sxs-lookup"><span data-stu-id="20a84-123">REVOKE statement</span></span>
-   <span data-ttu-id="20a84-124">Alias di ambito o numeri di Revisione</span><span class="sxs-lookup"><span data-stu-id="20a84-124">SCOPE aliases or revision numbers</span></span>
-   <span data-ttu-id="20a84-125">Seleziona tutto (rimuove automaticamente i duplicati)</span><span class="sxs-lookup"><span data-stu-id="20a84-125">SELECT ALL (removes duplicates automatically)</span></span>
-   <span data-ttu-id="20a84-126">Stored procedure</span><span class="sxs-lookup"><span data-stu-id="20a84-126">Stored procedures</span></span>
-   <span data-ttu-id="20a84-127">Espansione di documenti strutturati</span><span class="sxs-lookup"><span data-stu-id="20a84-127">Structured document expansion</span></span>
-   <span data-ttu-id="20a84-128">UNION ALL</span><span class="sxs-lookup"><span data-stu-id="20a84-128">UNION ALL</span></span>
-   <span data-ttu-id="20a84-129">Parola chiave UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="20a84-129">UNKNOWN keyword</span></span>
-   <span data-ttu-id="20a84-130">Istruzione UPDATE</span><span class="sxs-lookup"><span data-stu-id="20a84-130">UPDATE statement</span></span>

<span data-ttu-id="20a84-131">Windows Search non supporta il thesaurus e le parole non significative.</span><span class="sxs-lookup"><span data-stu-id="20a84-131">Windows Search does not support Thesaurus and Noise Words.</span></span>

 

 



