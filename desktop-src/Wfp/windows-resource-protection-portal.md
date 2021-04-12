---
description: La protezione delle risorse impedisce la sostituzione di file di sistema e cartelle e chiavi del registro di sistema essenziali per il sistema operativo. La modifica delle risorse protette può causare un errore di sistema o dell'applicazione.
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Protezione risorse di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347216"
---
# <a name="windows-resource-protection"></a><span data-ttu-id="1629b-104">Protezione risorse di Windows</span><span class="sxs-lookup"><span data-stu-id="1629b-104">Windows Resource Protection</span></span>

## <a name="purpose"></a><span data-ttu-id="1629b-105">Scopo</span><span class="sxs-lookup"><span data-stu-id="1629b-105">Purpose</span></span>

<span data-ttu-id="1629b-106">Protezione risorse di Windows (WRP) impedisce la sostituzione dei file di sistema essenziali, delle cartelle e delle chiavi del registro di sistema installate come parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1629b-106">Windows Resource Protection (WRP) prevents the replacement of essential system files, folders, and registry keys that are installed as part of the operating system.</span></span> <span data-ttu-id="1629b-107">È diventato disponibile a partire da Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1629b-107">It became available starting with Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="1629b-108">Le applicazioni non devono sovrascrivere queste risorse perché vengono usate dal sistema e da altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1629b-108">Applications should not overwrite these resources because they are used by the system and other applications.</span></span> <span data-ttu-id="1629b-109">La protezione di queste risorse impedisce gli errori dell'applicazione e del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1629b-109">Protecting these resources prevents application and operating system failures.</span></span> <span data-ttu-id="1629b-110">WRP è il nuovo nome per la protezione dei file di Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="1629b-110">WRP is the new name for Windows File Protection (WFP).</span></span> <span data-ttu-id="1629b-111">WRP protegge le chiavi del registro di sistema e le cartelle, nonché i file di sistema essenziali.</span><span class="sxs-lookup"><span data-stu-id="1629b-111">WRP protects registry keys and folders as well as essential system files.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="1629b-112">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="1629b-112">Where applicable</span></span>

<span data-ttu-id="1629b-113">Tutte le applicazioni basate su Windows e i relativi programmi di installazione eseguiti in Windows Server 2008 o Windows Vista e nei sistemi operativi successivi devono essere a conoscenza di WRP.</span><span class="sxs-lookup"><span data-stu-id="1629b-113">All Windows-based applications and their installation programs that run on Windows Server 2008 or Windows Vista, and later operating systems, should be aware of WRP.</span></span> <span data-ttu-id="1629b-114">Tutte le applicazioni basate su Windows in esecuzione su Microsoft Windows Server 2003 o Windows XP e i relativi programmi di installazione devono essere a conoscenza di Pam.</span><span class="sxs-lookup"><span data-stu-id="1629b-114">All Windows-based applications that run on Microsoft Windows Server 2003 or Windows XP and their installation programs should be aware of WFP.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1629b-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="1629b-115">Developer audience</span></span>

<span data-ttu-id="1629b-116">L'API WRP è progettata per l'uso da parte dei programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="1629b-116">The WRP API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="1629b-117">L'API WRP ha due funzioni: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) e [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span><span class="sxs-lookup"><span data-stu-id="1629b-117">The WRP API has two functions: [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) and [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1629b-118">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="1629b-118">Run-time requirements</span></span>

<span data-ttu-id="1629b-119">Le applicazioni che usano solo la funzione [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) richiedono windows Server 2008, Windows Vista, windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1629b-119">Applications that use only the [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) function require Windows Server 2008, Windows Vista, Windows Server 2003, or Windows XP.</span></span> <span data-ttu-id="1629b-120">Le applicazioni che usano la funzione [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) richiedono windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1629b-120">Applications that use the [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) function require Windows Server 2008 or Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1629b-121">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="1629b-121">In this section</span></span>



| <span data-ttu-id="1629b-122">Argomento</span><span class="sxs-lookup"><span data-stu-id="1629b-122">Topic</span></span>                                                                                     | <span data-ttu-id="1629b-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1629b-123">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="1629b-124">Informazioni su Protezione risorse di Windows</span><span class="sxs-lookup"><span data-stu-id="1629b-124">About Windows Resource Protection</span></span>](about-windows-file-protection.md)<br/>         | <span data-ttu-id="1629b-125">Informazioni generali su WRP.</span><span class="sxs-lookup"><span data-stu-id="1629b-125">General information about WRP.</span></span><br/>   |
| [<span data-ttu-id="1629b-126">Riferimento Protezione risorse di Windows</span><span class="sxs-lookup"><span data-stu-id="1629b-126">Windows Resource Protection Reference</span></span>](windows-file-protection-reference.md)<br/> | <span data-ttu-id="1629b-127">Documentazione di riferimento per WRP.</span><span class="sxs-lookup"><span data-stu-id="1629b-127">Reference documentation for WRP.</span></span><br/> |



 

 

 




