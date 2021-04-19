---
description: Uso delle API dei controlli padre
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Uso delle API dei controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311579"
---
# <a name="using-parental-controls-apis"></a><span data-ttu-id="0621e-103">Uso delle API dei controlli padre</span><span class="sxs-lookup"><span data-stu-id="0621e-103">Using Parental Controls APIs</span></span>

## <a name="api-selection"></a><span data-ttu-id="0621e-104">Selezione API</span><span class="sxs-lookup"><span data-stu-id="0621e-104">API Selection</span></span>

<span data-ttu-id="0621e-105">Come indicato nella sezione Panoramica, lo sviluppo prevede l'uso di un massimo di tre API:</span><span class="sxs-lookup"><span data-stu-id="0621e-105">As noted in the overview section, development involves use of up to three APIs:</span></span>

-   <span data-ttu-id="0621e-106">Accesso alle impostazioni di base: l'API COM per la conformità minima dei controlli padre (API di conformità) definita in Wpcapi. h per un accesso semplice a un subset chiave dello stato dei controlli padre.</span><span class="sxs-lookup"><span data-stu-id="0621e-106">Basic settings access: the Parental Controls minimum compliance COM API (Compliance API) defined in Wpcapi.h for simple access to a key subset of Parental Controls state.</span></span>
-   <span data-ttu-id="0621e-107">Accesso in lettura/scrittura completo delle impostazioni: l'uso di un piccolo subset dell'API COM WMI per l'accesso completo è necessario solo se l'ISV deve modificare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="0621e-107">Full settings write/read access: use of a small subset of the WMI COM API for full access is only required if the ISV needs to modify settings.</span></span> <span data-ttu-id="0621e-108">L'aggiunta di un collegamento di estendibilità dell'interfaccia utente, la sostituzione del filtro contenuto Web o le aggiunte all'applicazione HTTP a livello di computer o agli elenchi di esenzione del filtro URL sono i motivi principali per usare l'API.</span><span class="sxs-lookup"><span data-stu-id="0621e-108">Addition of a UI extensibility link, replacement of the Web Content Filter, or additions to the computer-wide HTTP application or URL filtering exemption lists are the primarily reasons to use the API.</span></span> <span data-ttu-id="0621e-109">Poiché l'utilizzo dello spazio dei nomi dei controlli padre WMI fornisce accesso non elaborato all'archivio delle impostazioni sottostante, gli ISV devono procedere con cautela nell'interpretazione dello stato dalle singole impostazioni che possono in realtà avere dipendenze di controllo da altre impostazioni.</span><span class="sxs-lookup"><span data-stu-id="0621e-109">As the WMI Parental Controls namespace usage provides raw access to the underlying settings store, ISVs should proceed with caution in interpreting state from individual settings that may in fact have gating dependencies on other settings.</span></span> <span data-ttu-id="0621e-110">È quindi consigliabile usare l'API di conformità per leggere lo stato di tutti i valori esposti da tale API.</span><span class="sxs-lookup"><span data-stu-id="0621e-110">It is therefore recommended to use the Compliance API for reading state for all values exposed by that API.</span></span>
-   <span data-ttu-id="0621e-111">Registrazione: l'API di traccia eventi di Windows Vista e il sistema di creazione di report (noto anche come ETW) per la pubblicazione di eventi di attività nei log dei controlli padre, in combinazione con descrittori di evento ed enumerazioni di matrici definite in WpcEvent. h.</span><span class="sxs-lookup"><span data-stu-id="0621e-111">Logging: the Windows Vista Event Tracing and Reporting system API (also referred to as ETW) for publishing activity events into the Parental Controls logs, in conjunction with event descriptors and array enumerations defined in WpcEvent.h.</span></span>

<span data-ttu-id="0621e-112">Tutte le API possono essere richiamate come utente standard.</span><span class="sxs-lookup"><span data-stu-id="0621e-112">All of the APIs are callable as a standard user.</span></span> <span data-ttu-id="0621e-113">Per la registrazione, qualsiasi utente può eseguire eventi di log di origine.</span><span class="sxs-lookup"><span data-stu-id="0621e-113">For logging, any user may source log events.</span></span> <span data-ttu-id="0621e-114">La chiamata a per recuperare o modificare le impostazioni per un altro utente avrà esito negativo se il chiamante non dispone dei privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="0621e-114">Calling to retrieve or change settings for another user will fail if the caller does not have administrator privileges.</span></span> <span data-ttu-id="0621e-115">In altre parole, un utente standard può accedere solo alle proprie impostazioni e solo per la lettura.</span><span class="sxs-lookup"><span data-stu-id="0621e-115">In other words, a standard user can access his or her own settings only, and only for reading.</span></span>

<span data-ttu-id="0621e-116">Le impostazioni e l'utilizzo dell'API di registrazione sono descritte in dettaglio nelle sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0621e-116">Settings and logging API usage are discussed further in these sections:</span></span>

-   [<span data-ttu-id="0621e-117">Uso delle API delle impostazioni dei controlli padre</span><span class="sxs-lookup"><span data-stu-id="0621e-117">Using Parental Controls Settings APIs</span></span>](using-parental-controls-settings-apis.md)
-   [<span data-ttu-id="0621e-118">Uso delle API di registrazione per i controlli padre</span><span class="sxs-lookup"><span data-stu-id="0621e-118">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a><span data-ttu-id="0621e-119">Ambiente di sviluppo</span><span class="sxs-lookup"><span data-stu-id="0621e-119">Development Environment</span></span>

<span data-ttu-id="0621e-120">Per lo sviluppo di controlli padre è necessario l'accesso a tre file di intestazione: WPC. h, WpcApi. h e WpcEvent. h.</span><span class="sxs-lookup"><span data-stu-id="0621e-120">Developing for Parental Controls requires access to three header files: Wpc.h, WpcApi.h, and WpcEvent.h.</span></span> <span data-ttu-id="0621e-121">WPC. h è un agente di raccolta che include le impostazioni API di conformità pubbliche e intestazioni di evento, quindi è sufficiente includere WPC. h nel codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0621e-121">Wpc.h is a collector that includes the settings public compliance API and event headers, so it is sufficient to include Wpc.h in application code.</span></span>

<span data-ttu-id="0621e-122">Le autorizzazioni di lettura/scrittura per l'API WMI sono specificate dal file Wpcsprov. mof.</span><span class="sxs-lookup"><span data-stu-id="0621e-122">Read/write permissions to the WMI API is specified by the Wpcsprov.mof file.</span></span> <span data-ttu-id="0621e-123">Questo file viene installato nella sottodirectory WBEM sotto la directory system32 di Windows.</span><span class="sxs-lookup"><span data-stu-id="0621e-123">This file is installed to the WBEM subdirectory under the Windows System32 directory.</span></span>

<span data-ttu-id="0621e-124">Il Software Development Kit (SDK) di Microsoft Windows contiene codice di esempio per rafforzare il codice di esempio illustrato di seguito e fornire semplici strumenti basati su riga di comando per l'esplorazione API o il test di integrazione.</span><span class="sxs-lookup"><span data-stu-id="0621e-124">The Microsoft Windows Software Development Kit (SDK) contains sample code to reinforce example code shown here and provide simple command-line driven tools for API exploration or integration testing.</span></span>

 

 



