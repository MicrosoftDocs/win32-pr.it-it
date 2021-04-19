---
description: Esempi di controlli padre
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Esempi di controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316432"
---
# <a name="parental-controls-samples"></a><span data-ttu-id="77044-103">Esempi di controlli padre</span><span class="sxs-lookup"><span data-stu-id="77044-103">Parental Controls Samples</span></span>

<span data-ttu-id="77044-104">Il codice di esempio per i controlli padre è disponibile in percorso <installation directory> \\ Windows \\ <version number> \\ Samples \\ Security \\ parentalcontrols.</span><span class="sxs-lookup"><span data-stu-id="77044-104">Sample code for Parental Controls is available under path <installation directory>\\Windows\\<version number>\\Samples\\Security\\ParentalControls.</span></span> <span data-ttu-id="77044-105">Gli esempi sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="77044-105">The samples are as follows:</span></span>

## <a name="utilities"></a><span data-ttu-id="77044-106">Utilità</span><span class="sxs-lookup"><span data-stu-id="77044-106">Utilities</span></span>

<span data-ttu-id="77044-107">Funzionalità di supporto per la gestione COM di base, le operazioni sulle stringhe SID e la funzionalità di lettura e scrittura WMI.</span><span class="sxs-lookup"><span data-stu-id="77044-107">Helper functionality for basic COM management, SID string operations, and WMI read and write functionality.</span></span> <span data-ttu-id="77044-108">Tutti gli altri esempi dipendono da questo progetto se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="77044-108">All of the other samples depend on this project unless otherwise specified.</span></span>

## <a name="complianceapi"></a><span data-ttu-id="77044-109">ComplianceAPI</span><span class="sxs-lookup"><span data-stu-id="77044-109">ComplianceAPI</span></span>

<span data-ttu-id="77044-110">Applicazione console guidata dalla riga di comando che illustra come usare l'API di conformità per recuperare un sottoinsieme di impostazioni chiave per un utente.</span><span class="sxs-lookup"><span data-stu-id="77044-110">Command-line driven console application demonstrating how to use the Compliance API to retrieve a key subset of settings for a user.</span></span>

## <a name="complianceapp"></a><span data-ttu-id="77044-111">ComplianceApp</span><span class="sxs-lookup"><span data-stu-id="77044-111">ComplianceApp</span></span>

<span data-ttu-id="77044-112">Semplice applicazione console che illustra l'uso dell'API di conformità per verificare la registrazione richiesta e restrizioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="77044-112">Simple console application demonstrating use of the Compliance API to check for logging required and specific restrictions.</span></span> <span data-ttu-id="77044-113">Se sono abilitate le restrizioni temporali, l'applicazione attende anche gli eventi di disconnessione imminenti.</span><span class="sxs-lookup"><span data-stu-id="77044-113">If time restrictions are enabled, the application also waits for the impending logout events.</span></span>

## <a name="uiextensibility"></a><span data-ttu-id="77044-114">UIExtensibility</span><span class="sxs-lookup"><span data-stu-id="77044-114">UIExtensibility</span></span>

<span data-ttu-id="77044-115">Applicazione console guidata dalla riga di comando che illustra l'uso delle API WMI e dello schema WPC per elencare, eseguire query, aggiungere, modificare ed eliminare voci di collegamento di estensibilità dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="77044-115">Command-line driven console application demonstrating use of the WMI APIs and WPC schema to list, query, add, modify, and delete UI Extensibility link entries.</span></span>

<span data-ttu-id="77044-116">Esempio di riga di comando per esempio:</span><span class="sxs-lookup"><span data-stu-id="77044-116">Example command line for sample:</span></span>

<span data-ttu-id="77044-117">"D: \\ WPC \\ Samples \\ Security \\ parentalcontrols \\ UIExtensibility \\ debug \\ UIExtensibility" Add/g: {FD59BB7F-54AB-11dB-9666-00E08161165F}/c: 0/N: D:/WPC/Samples/Security/parentalcontrols/UiExtRC/debug/UiExtRC.dll-101/S: d:/WPC/Samples/Security/parentalcontrols/UiExtRC/debug/UiExtRC.dll,-103/I: d:/WPC/Samples/Security/parentalcontrols/UiExtRC/debug/UiExtRC.dll,-104/D: D:/WPC/Samples/Security/parentalcontrols/UiExtRC/debug/UiExtRC.dll,-106/e: c: \\ Windows \\Notepad.exe</span><span class="sxs-lookup"><span data-stu-id="77044-117">"D:\\WPC\\Samples\\Security\\ParentalControls\\UIExtensibility\\debug\\UIExtensibility" add /g:{FD59BB7F-54AB-11DB-9666-00E08161165F} /c:0 /n:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-101 /s:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-103 /i:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-104 /d:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-106 /e:c:\\windows\\Notepad.exe</span></span>

<span data-ttu-id="77044-118">dove UiExtRC è una DLL di risorse semplice con risorse di stringa per l'ID 101 e 103 e 24x24 pixel 32 bit con bitmap Alpha per le risorse 104 e 106.</span><span class="sxs-lookup"><span data-stu-id="77044-118">where UiExtRC is a simple resource DLL with string resources for ID's 101 and 103, and 24x24 pixel 32-bit with alpha bitmaps for resources 104 and 106.</span></span>

## <a name="webextensibility"></a><span data-ttu-id="77044-119">Estendibilità</span><span class="sxs-lookup"><span data-stu-id="77044-119">WebExtensibility</span></span>

<span data-ttu-id="77044-120">Applicazione console guidata dalla riga di comando che illustra come usare le API WMI e lo schema WPC per elencare, aggiungere ed eliminare le voci di esenzione URL o applicazione HTTP e per impostare e reimpostare l'override di un filtro contenuto Web con le proprietà FilterID e FilterName.</span><span class="sxs-lookup"><span data-stu-id="77044-120">Command-line driven console application demonstrating how to use the WMI APIs and WPC schema to list, add, and delete HTTP application or URL exemption entries, and to set and reset a Web Content Filter override with the FilterID and FilterName properties.</span></span>

<span data-ttu-id="77044-121">L'accesso all'applicazione HTTP di sola lettura e agli elenchi di esenzione URL non viene visualizzato, ma il codice per leggere gli elenchi è identico a quello per il caso di lettura/scrittura, fatta eccezione per la modifica del parametro WMI.</span><span class="sxs-lookup"><span data-stu-id="77044-121">Access to the read-only HTTP application and URL exemption lists is not shown, but the code to read the lists would be the same as for the read/write case except for modification of the WMI parameter.</span></span>

 

 



