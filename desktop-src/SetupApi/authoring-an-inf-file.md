---
description: Quando si crea un file INF per un'applicazione di installazione, è necessario fare riferimento anche al formato di file INF descritto in linee guida generali per i file INF e le sezioni e le direttive del file inf del Microsoft Windows 2000 Driver Development Kit.
ms.assetid: f9df95bb-345d-4a70-a27e-0b1bc2a27ada
title: Creazione di un file INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73807f919a016f414a248f47e53f27d5b079bb33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306514"
---
# <a name="authoring-an-inf-file"></a><span data-ttu-id="a66ce-103">Creazione di un file INF</span><span class="sxs-lookup"><span data-stu-id="a66ce-103">Authoring an INF file</span></span>

<span data-ttu-id="a66ce-104">Quando si crea un file INF per un'applicazione di installazione, è necessario fare riferimento anche al formato di file INF descritto in *linee guida generali per i file inf* e le *sezioni e le direttive del file* inf del Microsoft Windows 2000 Driver Development Kit.</span><span class="sxs-lookup"><span data-stu-id="a66ce-104">When authoring an INF file for a Setup application you should also refer to the INF file format documented in *General Guidelines for INF Files* and *INF File Sections and Directives* of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="a66ce-105">Quando si creano file INF per un'applicazione di installazione, attenersi alle regole seguenti.</span><span class="sxs-lookup"><span data-stu-id="a66ce-105">When authoring INF files for a setup application adhere to the following rules.</span></span>

-   <span data-ttu-id="a66ce-106">Una sezione **Version** è obbligatoria in ogni file inf.</span><span class="sxs-lookup"><span data-stu-id="a66ce-106">A **Version** section is required in every INF file.</span></span>
-   <span data-ttu-id="a66ce-107">Le sezioni devono iniziare con il nome della sezione racchiuso tra parentesi quadre ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="a66ce-107">Sections must begin with the section name enclosed by square brackets (\[\]).</span></span>
-   <span data-ttu-id="a66ce-108">I nomi delle sezioni **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings** e **Version** devono essere identici a quelli del tipo di sezione.</span><span class="sxs-lookup"><span data-stu-id="a66ce-108">Names of **DestinationDirs**, **SourceDisksFiles**, **SourceDisksNames**, **Strings**, and **Version** sections must be identical to the section type.</span></span> <span data-ttu-id="a66ce-109">Ad esempio \[ , usare DestinationDirs \] .</span><span class="sxs-lookup"><span data-stu-id="a66ce-109">For example use \[DestinationDirs\].</span></span> <span data-ttu-id="a66ce-110">Gli autori possono specificare i nomi di altri tipi di sezioni.</span><span class="sxs-lookup"><span data-stu-id="a66ce-110">Authors may specify the names of other types of sections.</span></span>
-   <span data-ttu-id="a66ce-111">I nomi delle sezioni **SourceDisksNames** e **SourceDisksFiles** possono essere aggiunti con un suffisso specifico della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="a66ce-111">Names of **SourceDisksNames** and **SourceDisksFiles** sections may be appended with a platform-specific suffix.</span></span> <span data-ttu-id="a66ce-112">Per visualizzare, ad esempio, una sezione **SourceDisksNames** specifica di Intel, utilizzare \[ SourceDisksNames. x86 \] .</span><span class="sxs-lookup"><span data-stu-id="a66ce-112">For example, to show an Intel-specific **SourceDisksNames** section use \[SourceDisksNames.x86\].</span></span> <span data-ttu-id="a66ce-113">Se le funzioni di installazione trovano sezioni specifiche della piattaforma **SourceDisksNames** e **SourceDisksFiles** che corrispondono alla piattaforma dell'utente, le funzioni usano le sezioni specifiche della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="a66ce-113">If the setup functions find platform-specific **SourceDisksNames** and **SourceDisksFiles** sections matching the user's platform, the functions use the platform-specific sections.</span></span> <span data-ttu-id="a66ce-114">In caso contrario, le funzioni di installazione utilizzano le sezioni **SourceDisksNames** e **SourceDisksFiles** senza suffisso.</span><span class="sxs-lookup"><span data-stu-id="a66ce-114">Otherwise the setup functions use the non-suffixed **SourceDisksNames** and **SourceDisksFiles** sections.</span></span> <span data-ttu-id="a66ce-115">Le funzioni di installazione possono determinare a livello di codice il sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a66ce-115">The setup functions can programmatically determine the user's system.</span></span> <span data-ttu-id="a66ce-116">Vedere l' [esempio di sezioni inf SourceDisksNames e SourceDisksFiles](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span><span class="sxs-lookup"><span data-stu-id="a66ce-116">See the [INF SourceDisksNames and SourceDisksFiles Sections Example](inf-sourcedisksnames-and-sourcedisksfiles-sections-example.md).</span></span>
-   <span data-ttu-id="a66ce-117">I valori possono essere espressi come stringhe sostituibili utilizzando il formato%*strKey*%.</span><span class="sxs-lookup"><span data-stu-id="a66ce-117">Values may be expressed as replaceable strings using the form %*strkey*%.</span></span> <span data-ttu-id="a66ce-118">Per usare un carattere% nella stringa, usare%%.</span><span class="sxs-lookup"><span data-stu-id="a66ce-118">To use a % character in the string, use %%.</span></span> <span data-ttu-id="a66ce-119">StrKey deve essere definito in una sezione **Strings** del file inf.</span><span class="sxs-lookup"><span data-stu-id="a66ce-119">The strkey must be defined in a **Strings** section of the INF file.</span></span>

 

 



