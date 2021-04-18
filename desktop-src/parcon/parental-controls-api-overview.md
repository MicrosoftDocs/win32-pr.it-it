---
description: Cenni preliminari sull'API dei controlli padre
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Cenni preliminari sull'API dei controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0aa88592f2262b89f98cfd5baaac5ad2f35f959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318402"
---
# <a name="parental-controls-api-overview"></a><span data-ttu-id="bcb8e-103">Cenni preliminari sull'API dei controlli padre</span><span class="sxs-lookup"><span data-stu-id="bcb8e-103">Parental Controls API Overview</span></span>

<span data-ttu-id="bcb8e-104">Le API usate per i controlli padre espongono i criteri e le impostazioni di restrizione predefinite e la funzionalità di registrazione.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-104">APIs used for Parental Controls expose the policy and in-box restrictions settings, and logging functionality.</span></span>

## <a name="settings"></a><span data-ttu-id="bcb8e-105">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="bcb8e-105">Settings</span></span>

<span data-ttu-id="bcb8e-106">Sono disponibili due API pubbliche:</span><span class="sxs-lookup"><span data-stu-id="bcb8e-106">Two public APIs are provided:</span></span>

-   <span data-ttu-id="bcb8e-107">Un'API di conformità minima basata su COM (denominata API di conformità) principalmente per le applicazioni per determinare se la registrazione deve essere attivata.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-107">A lightweight COM-based minimum compliance API (called the Compliance API) primarily for applications to determine whether logging should be turned on.</span></span> <span data-ttu-id="bcb8e-108">Vengono inoltre forniti metodi semplici per:</span><span class="sxs-lookup"><span data-stu-id="bcb8e-108">In addition, simple methods are provided for:</span></span>
    -   <span data-ttu-id="bcb8e-109">Recupero dello stato delle restrizioni per le restrizioni Web, i limiti di tempo, le restrizioni dei giochi e le restrizioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-109">Retrieving the restrictions state for web restrictions, time limits, games restrictions, and application restrictions.</span></span>
    -   <span data-ttu-id="bcb8e-110">Recupero dell'ID del filtro contenuto Web attivo.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-110">Retrieving the ID of the active Web content filter.</span></span>
    -   <span data-ttu-id="bcb8e-111">Determinare se gli elementi dell'interfaccia utente del fornitore devono essere visualizzati, in modo coerente con il nascondiglio in box quando vengono aggiunti a un dominio.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-111">Determining whether vendor user interface elements should be shown, in a manner consistent with the in-box hiding when joined to a domain.</span></span>
    -   <span data-ttu-id="bcb8e-112">Recupero dell'Ultima modifica di un'impostazione per un utente.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-112">Retrieving the last time a setting has been changed for a user.</span></span>
    -   <span data-ttu-id="bcb8e-113">Il recupero del download dei file basati sul browser o di tipo browser deve essere bloccato per un utente e la possibilità di richiedere un URL da consentire in modo specifico al filtro contenuto Web per tale utente.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-113">Retrieving whether browser-based or browser-like file downloads need to be blocked for a user, and the ability to request a URL to be specifically allowed by the Web Content Filter for that user.</span></span>
    -   <span data-ttu-id="bcb8e-114">Determinare se un determinato gioco è bloccato per un utente.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-114">Determining whether a given game is blocked for a user.</span></span>
-   <span data-ttu-id="bcb8e-115">Accesso all'API Strumentazione gestione Windows (WMI) a uno spazio dei nomi dei controlli padre per l'accesso in lettura e scrittura completo a tutte le impostazioni esposte.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-115">Windows Management Instrumentation (WMI) API access to a Parental Controls namespace for full write and read access to all exposed settings.</span></span> <span data-ttu-id="bcb8e-116">I controlli padre distribuiscono un provider WMI per gestire le autorizzazioni di lettura/scrittura per l'archivio delle impostazioni sottostanti con l'imposizione corretta dei privilegi per gli amministratori e gli utenti controllati.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-116">Parental Controls deploys a WMI Provider to manage read/write permissions to the underlying settings store with proper enforcement of privileges for administrators and controlled users.</span></span>

<span data-ttu-id="bcb8e-117">Agli ISV viene richiesto di utilizzare l'API di conformità e l'API WMI, se necessario, per controllare le restrizioni appropriate per la sicurezza figlio in base alle funzionalità dell'applicazione o della soluzione.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-117">ISVs are requested to use the Compliance API, and the WMI API as necessary, to control restrictions as appropriate for child safety based on the functionality of the application or solution.</span></span>

## <a name="logging"></a><span data-ttu-id="bcb8e-118">Registrazione</span><span class="sxs-lookup"><span data-stu-id="bcb8e-118">Logging</span></span>

-   <span data-ttu-id="bcb8e-119">Le API di pubblicazione e utilizzo di eventi standard di Windows vengono utilizzate per il monitoraggio delle attività dei controlli padre.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-119">Windows standard event publishing and consuming APIs are used for Parental Controls activity monitoring.</span></span> <span data-ttu-id="bcb8e-120">Il sistema di segnalazione degli eventi e di traccia di Windows Vista ha migliorato le prestazioni rispetto alla funzionalità ETW (Previous Event Tracing for Windows).</span><span class="sxs-lookup"><span data-stu-id="bcb8e-120">The Windows Vista Event Reporting and Tracing system has improved performance over previous Event Tracing for Windows (ETW) functionality.</span></span> <span data-ttu-id="bcb8e-121">I controlli padre definiscono un canale univoco per i dati in ETW.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-121">Parental Controls defines a unique channel for its data in ETW.</span></span>
-   <span data-ttu-id="bcb8e-122">Agli ISV viene richiesto di utilizzare l'API di pubblicazione degli eventi per registrare l'attività utente come specificato nella sezione Utilizzo delle API dei controlli padre.</span><span class="sxs-lookup"><span data-stu-id="bcb8e-122">ISVs are requested to use the event publishing API to log user activity as specified in the Using Parental Controls APIs section.</span></span>

 

 



