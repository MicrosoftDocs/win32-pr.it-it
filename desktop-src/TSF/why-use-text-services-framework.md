---
title: Perché usare il Framework di servizi di testo
description: Perché usare il Framework di servizi di testo
ms.assetid: 64b3b0a1-7740-49fa-b0a6-f80040147280
keywords:
- Framework servizi di testo (TSF), informazioni
- TSF (Text Services Framework), informazioni
- Servizi di testo, informazioni
- Applicazioni abilitate per TSF, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6647981b890bd1fcdf488b18bffad587f49ed9b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297841"
---
# <a name="why-use-text-services-framework"></a><span data-ttu-id="515f6-107">Perché usare Text Services Framework?</span><span class="sxs-lookup"><span data-stu-id="515f6-107">Why Use Text Services Framework?</span></span>

<span data-ttu-id="515f6-108">Il Framework di servizi di testo (TSF) consente a un'applicazione abilitata per TSF di ricevere input di testo da un numero qualsiasi di dispositivi o origini.</span><span class="sxs-lookup"><span data-stu-id="515f6-108">Text Services Framework (TSF) enables a TSF-enabled application to receive text input from any number of devices or sources.</span></span> <span data-ttu-id="515f6-109">Poiché TSF è estensibile, l'applicazione può ricevere input di testo da origini di testo aggiuntive con modifiche minime o nulle.</span><span class="sxs-lookup"><span data-stu-id="515f6-109">Because TSF is extensible, the application can receive text input from additional text sources with little or no modification.</span></span>

<span data-ttu-id="515f6-110">Un servizio di testo ottiene il testo da e fornisce il testo a qualsiasi applicazione abilitata per TSF senza richiedere alcuna conoscenza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="515f6-110">A text service obtains text from, and provides text to, any TSF-enabled application without requiring any knowledge about the application.</span></span> <span data-ttu-id="515f6-111">Questa struttura consente al servizio di testo di essere disponibile per qualsiasi applicazione abilitata per TSF.</span><span class="sxs-lookup"><span data-stu-id="515f6-111">This structure enables the text service to be available to any TSF-enabled application.</span></span> <span data-ttu-id="515f6-112">Il servizio di testo può essere installato o aggiornato come modulo separato ed è indipendente da qualsiasi applicazione specifica.</span><span class="sxs-lookup"><span data-stu-id="515f6-112">The text service can be installed or updated as a separate module and is independent of any specific application.</span></span> <span data-ttu-id="515f6-113">TSF consente inoltre a un servizio di testo di archiviare metadati con un documento, una parte di testo o un oggetto all'interno del documento.</span><span class="sxs-lookup"><span data-stu-id="515f6-113">TSF also enables a text service to store metadata with a document, a piece of text, or an object within the document.</span></span> <span data-ttu-id="515f6-114">Ad esempio, un servizio di testo di input vocale può archiviare le informazioni audio associate a un blocco di testo.</span><span class="sxs-lookup"><span data-stu-id="515f6-114">For example, a speech input text service can store sound information associated with a block of text.</span></span>

<span data-ttu-id="515f6-115">TSF consente ai servizi di testo di fornire una conversione di testo accurata e completa, con accesso continuo al buffer del documento.</span><span class="sxs-lookup"><span data-stu-id="515f6-115">TSF enables text services to provide accurate and complete text conversion, with continuous access to the document buffer.</span></span> <span data-ttu-id="515f6-116">I servizi di testo che usano TSF possono evitare la separazione delle funzionalità in modalità per l'input e le modalità di modifica.</span><span class="sxs-lookup"><span data-stu-id="515f6-116">Text services using TSF can avoid separating their functionality into modes for input and modes for editing.</span></span> <span data-ttu-id="515f6-117">Questa architettura di input consente la modifica dinamica del flusso di testo memorizzato nel buffer e dell'accumulo, consentendo in tal modo un input di tastiera e una modifica del testo più efficienti.</span><span class="sxs-lookup"><span data-stu-id="515f6-117">This input architecture enables the buffered and accumulating text stream to change dynamically, thereby enabling more efficient keyboard input and text editing.</span></span>

<span data-ttu-id="515f6-118">TSF è indipendente dal dispositivo e Abilita i servizi di testo per più dispositivi di input, tra cui tastiera, penna e microfono.</span><span class="sxs-lookup"><span data-stu-id="515f6-118">TSF is device-independent and enables text services for multiple input devices including keyboard, pen, and microphone.</span></span>

 

 




