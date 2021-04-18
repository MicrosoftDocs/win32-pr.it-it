---
description: impostazioni locali \_ INvariabili
ms.assetid: d37df17d-8cd5-4481-bee2-062cf9d78e9b
title: LOCALE_INVARIANT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca1e526b91ba372ed7efaad62e9e1597b0d5130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306610"
---
# <a name="locale_invariant"></a><span data-ttu-id="e93e7-103">impostazioni locali \_ INvariabili</span><span class="sxs-lookup"><span data-stu-id="e93e7-103">LOCALE\_INVARIANT</span></span>

<span data-ttu-id="e93e7-104">**Windows XP:** Impostazioni locali utilizzate per le funzioni a livello di sistema che richiedono risultati coerenti e indipendenti dalle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="e93e7-104">**Windows XP:** The locale used for operating system-level functions that require consistent and locale-independent results.</span></span> <span data-ttu-id="e93e7-105">Ad esempio, le impostazioni locali invariabili vengono utilizzate quando un'applicazione confronta le stringhe di caratteri utilizzando la funzione [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) e prevede un risultato coerente indipendentemente dalle impostazioni locali dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e93e7-105">For example, the invariant locale is used when an application compares character strings using the [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) function and expects a consistent result regardless of the user locale.</span></span> <span data-ttu-id="e93e7-106">Le impostazioni locali invariabili sono simili a quelle per la lingua inglese (Stati Uniti) ma non devono essere utilizzate per visualizzare dati formattati.</span><span class="sxs-lookup"><span data-stu-id="e93e7-106">The settings of the invariant locale are similar to those for English (United States) but should not be used to display formatted data.</span></span> <span data-ttu-id="e93e7-107">In genere, un'applicazione non usa l' \_ INvariante delle impostazioni locali perché prevede che i risultati di un'azione dipendano dalle regole che regolano ogni singola impostazione locale.</span><span class="sxs-lookup"><span data-stu-id="e93e7-107">Typically, an application does not use LOCALE\_INVARIANT because it expects the results of an action to depend on the rules governing each individual locale.</span></span> <span data-ttu-id="e93e7-108">Il valore di impostazioni locali \_ INvariante è 0x007f.</span><span class="sxs-lookup"><span data-stu-id="e93e7-108">The value of LOCALE\_INVARIANT IS 0x007f.</span></span>

 

 
