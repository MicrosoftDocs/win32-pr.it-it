---
description: Questa sezione descrive come eseguire attività di programmazione di base con l'API di firma digitale XPS.
ms.assetid: a25a8d33-000a-4774-8beb-56d3bb39d5ae
title: Attività comuni di programmazione della firma digitale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 346b29c7768f4c4e972284afa697f97bb1da5f69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485804"
---
# <a name="common-digital-signature-programming-tasks"></a><span data-ttu-id="29ed1-103">Attività comuni di programmazione della firma digitale</span><span class="sxs-lookup"><span data-stu-id="29ed1-103">Common Digital Signature Programming Tasks</span></span>

<span data-ttu-id="29ed1-104">Questa sezione descrive come eseguire attività di programmazione di base con l'API di firma digitale XPS.</span><span class="sxs-lookup"><span data-stu-id="29ed1-104">This section describes how to perform basic programming tasks with the XPS Digital Signature API.</span></span>

<span data-ttu-id="29ed1-105">Attività</span><span class="sxs-lookup"><span data-stu-id="29ed1-105">Tasks</span></span>

-   [<span data-ttu-id="29ed1-106">Inizializzazione di gestione firme</span><span class="sxs-lookup"><span data-stu-id="29ed1-106">Initialize the Signature Manager</span></span>](initialize-the-signature-manager.md)
-   [<span data-ttu-id="29ed1-107">Firmare un documento</span><span class="sxs-lookup"><span data-stu-id="29ed1-107">Sign a Document</span></span>](sign-a-document.md)
-   [<span data-ttu-id="29ed1-108">Aggiungere una richiesta di firma a un documento XPS</span><span class="sxs-lookup"><span data-stu-id="29ed1-108">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
-   [<span data-ttu-id="29ed1-109">Verificare le firme del documento</span><span class="sxs-lookup"><span data-stu-id="29ed1-109">Verify Document Signatures</span></span>](verify-document-signatures.md)

## <a name="disclaimer"></a><span data-ttu-id="29ed1-110">Dichiarazione di non responsabilità</span><span class="sxs-lookup"><span data-stu-id="29ed1-110">Disclaimer</span></span>

<span data-ttu-id="29ed1-111">Gli esempi di codice non sono destinati a essere programmi completi e funzionanti.</span><span class="sxs-lookup"><span data-stu-id="29ed1-111">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="29ed1-112">Gli esempi di codice a cui si fa riferimento in questa pagina, ad esempio, non eseguono il controllo dei parametri, il controllo degli errori, la memoria completa o la gestione delle risorse o la gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="29ed1-112">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, complete memory or resource management, or error handling.</span></span> <span data-ttu-id="29ed1-113">Usare questi esempi come punto di partenza, quindi aggiungere il codice necessario per creare un'applicazione affidabile.</span><span class="sxs-lookup"><span data-stu-id="29ed1-113">Use these examples as a starting point, then add the necessary code to create a robust application.</span></span> <span data-ttu-id="29ed1-114">Per ulteriori informazioni sui valori restituiti **HRESULT** e sulle strategie di gestione degli errori, vedere [gestione degli errori in com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="29ed1-114">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="29ed1-115">Per maggiore chiarezza, questi esempi di codice usano scenari di firma e documento XPS molto semplici, che potrebbero non essere sufficientemente complessi da soddisfare le proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="29ed1-115">For clarity, these code examples use very simple XPS document and signature scenarios, which might not be sufficiently complex to meet your needs.</span></span>

 

 
