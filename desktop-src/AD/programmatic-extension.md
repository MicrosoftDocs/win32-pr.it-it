---
title: Estensione a livello di codice
description: Le estensioni programmatiche presentano diversi meriti, tuttavia un'applicazione è opaca; l'amministratore deve considerare attendibile la documentazione inclusa nell'applicazione di installazione.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Estensione a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707582"
---
# <a name="programmatic-extension"></a><span data-ttu-id="7cf51-104">Estensione a livello di codice</span><span class="sxs-lookup"><span data-stu-id="7cf51-104">Programmatic Extension</span></span>

<span data-ttu-id="7cf51-105">Il vantaggio di un file LDIF è che l'amministratore può esaminarne la funzione.</span><span class="sxs-lookup"><span data-stu-id="7cf51-105">The benefit of an LDIF file is that the administrator can examine its function.</span></span> <span data-ttu-id="7cf51-106">Tuttavia, lo schema può anche essere esteso a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="7cf51-106">However, the schema can also be extended programmatically.</span></span> <span data-ttu-id="7cf51-107">Le estensioni a livello di codice hanno diversi meriti, ma un'applicazione è opaca; l'amministratore deve considerare attendibile la documentazione inclusa nell'applicazione di installazione.</span><span class="sxs-lookup"><span data-stu-id="7cf51-107">Programmatic extensions have several merits, but an application is opaque; the administrator must trust the documentation included with the setup application.</span></span> <span data-ttu-id="7cf51-108">L'utilizzo delle estensioni dello schema programmatico può essere una barriera alla distribuzione per le applicazioni che le utilizzano.</span><span class="sxs-lookup"><span data-stu-id="7cf51-108">Use of programmatic schema extensions may be a barrier to deployment for applications that use them.</span></span> <span data-ttu-id="7cf51-109">Un'estensione a livello di codice è invariante. si tratta di un eseguibile di Windows NT.</span><span class="sxs-lookup"><span data-stu-id="7cf51-109">A programmatic extension is invariant; it is a Windows NT executable.</span></span> <span data-ttu-id="7cf51-110">Il file binario non può essere alterato, a differenza di un file LDIF o CSV, che può essere modificato inavvertitamente o intenzionalmente.</span><span class="sxs-lookup"><span data-stu-id="7cf51-110">The binary cannot be tampered with, unlike an LDIF or .csv file, which can be edited inadvertently or maliciously.</span></span>

<span data-ttu-id="7cf51-111">I vantaggi di un file LDIF includono:</span><span class="sxs-lookup"><span data-stu-id="7cf51-111">Benefits of an LDIF file include:</span></span>

-   <span data-ttu-id="7cf51-112">Le applicazioni possono rilevare e correggere gli errori e fornire commenti e suggerimenti degli utenti.</span><span class="sxs-lookup"><span data-stu-id="7cf51-112">Applications can detect and recover from errors and provide user feedback.</span></span>
-   <span data-ttu-id="7cf51-113">Le applicazioni possono gestire Unicode senza ricorrere alla codifica Base64.</span><span class="sxs-lookup"><span data-stu-id="7cf51-113">Applications can handle Unicode without resorting to Base64 encoding.</span></span>
-   <span data-ttu-id="7cf51-114">Le applicazioni possono utilizzare le API di installazione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7cf51-114">Applications can leverage Windows Installer setup APIs.</span></span>
-   <span data-ttu-id="7cf51-115">Le applicazioni possono essere firmate per stabilire l'autenticità.</span><span class="sxs-lookup"><span data-stu-id="7cf51-115">Applications can be signed to establish authenticity.</span></span>

 

 




