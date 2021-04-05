---
title: Implementazione del set di proprietà informazioni di riepilogo
description: Quando si implementa un set di proprietà di informazioni di riepilogo per l'archiviazione strutturata, sono disponibili linee guida da seguire.
ms.assetid: e1204de5-b712-4bd5-bffb-6a12ec8d7052
keywords:
- Implementazione del set di proprietà informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69e5ae6208aa5cb7a325d1cccf77f17e969c5b75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707300"
---
# <a name="implementing-the-summary-information-property-set"></a><span data-ttu-id="22311-104">Implementazione del set di proprietà informazioni di riepilogo</span><span class="sxs-lookup"><span data-stu-id="22311-104">Implementing the Summary Information Property Set</span></span>

<span data-ttu-id="22311-105">Quando si implementa un set di proprietà di informazioni di riepilogo per l'archiviazione strutturata, sono disponibili linee guida da seguire.</span><span class="sxs-lookup"><span data-stu-id="22311-105">There are guidelines to follow when implementing a summary information property set for Structured Storage.</span></span>

<span data-ttu-id="22311-106">Di seguito sono riportate le linee guida per l'implementazione [del set di proprietà informazioni di riepilogo](the-summary-information-property-set.md):</span><span class="sxs-lookup"><span data-stu-id="22311-106">The following are the guidelines for implementing [The Summary Information Property Set](the-summary-information-property-set.md):</span></span>

-   <span data-ttu-id="22311-107">**PID \_ Il modello** fa riferimento a un documento esterno contenente informazioni sul formato e sullo stile.</span><span class="sxs-lookup"><span data-stu-id="22311-107">**PID\_TEMPLATE** refers to an external document containing format and style information.</span></span> <span data-ttu-id="22311-108">Il processo con cui si trova il modello è definito dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="22311-108">The process by which the template is located is implementation-defined.</span></span>
-   <span data-ttu-id="22311-109">**PID \_ LASTAUTHOR** è il nome archiviato nelle informazioni utente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="22311-109">**PID\_LASTAUTHOR** is the name stored in User Information by the application.</span></span> <span data-ttu-id="22311-110">Ad esempio, Mary crea un documento nel computer e lo assegna a John, che lo modifica e lo salva.</span><span class="sxs-lookup"><span data-stu-id="22311-110">For example, Mary creates a document on her computer and gives it to John, who then modifies and saves it.</span></span> <span data-ttu-id="22311-111">Mary è l'autore, Giorgio è l'ultimo salvataggio per valore.</span><span class="sxs-lookup"><span data-stu-id="22311-111">Mary is the author, John is the last saved by value.</span></span>
-   <span data-ttu-id="22311-112">**PID \_ REVNUMBER** è il numero di volte in cui il comando file/Salva è stato chiamato in questo documento.</span><span class="sxs-lookup"><span data-stu-id="22311-112">**PID\_REVNUMBER** is the number of times the File/Save command has been called on this document.</span></span>
-   <span data-ttu-id="22311-113">Ognuno dei valori di data/ora deve essere archiviato in formato UTC (Universal Coordinated Time).</span><span class="sxs-lookup"><span data-stu-id="22311-113">Each of the date/time values must be stored in Universal Coordinated Time (UTC).</span></span>
-   <span data-ttu-id="22311-114">**PID \_ CREATE \_ DTM** è una proprietà di sola lettura. Questa proprietà deve essere impostata quando viene creato un documento, ma non deve essere modificata successivamente.</span><span class="sxs-lookup"><span data-stu-id="22311-114">**PID\_CREATE\_DTM** is a read-only property; this property should be set when a document is created, but should not be subsequently changed.</span></span>
-   <span data-ttu-id="22311-115">Per **l' \_ Anteprima PID**, le applicazioni devono archiviare i dati nel formato **CF \_ DIB** o **CF \_ METAFILEPICT** .</span><span class="sxs-lookup"><span data-stu-id="22311-115">For **PID\_THUMBNAIL**, applications should store data in **CF\_DIB** or **CF\_METAFILEPICT** format.</span></span> <span data-ttu-id="22311-116">**CF \_** È consigliabile usare METAFILEPICT.</span><span class="sxs-lookup"><span data-stu-id="22311-116">**CF\_METAFILEPICT** is recommended.</span></span>
-   <span data-ttu-id="22311-117">**PID \_ La sicurezza** è il livello di sicurezza suggerito per il documento.</span><span class="sxs-lookup"><span data-stu-id="22311-117">**PID\_SECURITY** is the suggested security level for the document.</span></span> <span data-ttu-id="22311-118">Annotando il livello di sicurezza del documento, un'applicazione diversa dal creatore del documento può modificare l'interfaccia utente per le proprietà.</span><span class="sxs-lookup"><span data-stu-id="22311-118">By noting the security level on the document, an application other than the originator of the document can adjust its user interface to the properties.</span></span> <span data-ttu-id="22311-119">Un'applicazione non deve visualizzare informazioni su un documento protetto da password o abilitare le modifiche apportate Read-Only o documenti bloccati per le annotazioni.</span><span class="sxs-lookup"><span data-stu-id="22311-119">An application should not display any information about a password-protected document or enable modifications to enforced Read-Only or Locked-for-Annotations documents.</span></span> <span data-ttu-id="22311-120">Se l'utente tenta di modificare le proprietà, l'applicazione deve avvisare l'utente sulla Read-Only stato consigliato.</span><span class="sxs-lookup"><span data-stu-id="22311-120">If the user attempts to modify properties, the application should warn the user about the Read-Only Recommended status.</span></span>



| <span data-ttu-id="22311-121">Livello di sicurezza</span><span class="sxs-lookup"><span data-stu-id="22311-121">Security level</span></span>         | <span data-ttu-id="22311-122">Valore</span><span class="sxs-lookup"><span data-stu-id="22311-122">Value</span></span> |
|------------------------|-------|
| <span data-ttu-id="22311-123">nessuno</span><span class="sxs-lookup"><span data-stu-id="22311-123">None</span></span>                   | <span data-ttu-id="22311-124">0</span><span class="sxs-lookup"><span data-stu-id="22311-124">0</span></span>     |
| <span data-ttu-id="22311-125">Protetto da password</span><span class="sxs-lookup"><span data-stu-id="22311-125">Password protected</span></span>     | <span data-ttu-id="22311-126">1</span><span class="sxs-lookup"><span data-stu-id="22311-126">1</span></span>     |
| <span data-ttu-id="22311-127">Di sola lettura consigliata</span><span class="sxs-lookup"><span data-stu-id="22311-127">Read-only recommended</span></span>  | <span data-ttu-id="22311-128">2</span><span class="sxs-lookup"><span data-stu-id="22311-128">2</span></span>     |
| <span data-ttu-id="22311-129">Applicazione di sola lettura</span><span class="sxs-lookup"><span data-stu-id="22311-129">Read-only enforced</span></span>     | <span data-ttu-id="22311-130">4</span><span class="sxs-lookup"><span data-stu-id="22311-130">4</span></span>     |
| <span data-ttu-id="22311-131">Bloccato per le annotazioni</span><span class="sxs-lookup"><span data-stu-id="22311-131">Locked for annotations</span></span> | <span data-ttu-id="22311-132">8</span><span class="sxs-lookup"><span data-stu-id="22311-132">8</span></span>     |



 

 

 




