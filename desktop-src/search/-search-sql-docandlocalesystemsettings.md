---
description: Quando il sistema operativo, o anche un'applicazione, è impostato per l'utilizzo di una lingua e delle impostazioni locali specifiche, sono interessate molte impostazioni.
ms.assetid: cec164d1-125f-483c-9d74-0e24b8215157
title: Impostazioni locali documento e sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9408093a8583a4b17566b5fcd118b30439c0ebda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306132"
---
# <a name="document-and-system-locale-settings"></a><span data-ttu-id="6458d-103">Impostazioni locali documento e sistema</span><span class="sxs-lookup"><span data-stu-id="6458d-103">Document and System Locale Settings</span></span>

<span data-ttu-id="6458d-104">Quando il sistema operativo, o anche un'applicazione, è impostato per l'utilizzo di una lingua e delle impostazioni locali specifiche, sono interessate molte impostazioni.</span><span class="sxs-lookup"><span data-stu-id="6458d-104">When the operating system, or even an application, is set to use a particular language and locale, many settings are affected.</span></span> <span data-ttu-id="6458d-105">Queste impostazioni includono formato numerico, formato data, formato valuta, mapping maiuscolo e minuscolo, ordinamento dizionario, token e altro.</span><span class="sxs-lookup"><span data-stu-id="6458d-105">These settings include numeric format, date format, currency format, uppercase and lowercase mapping, dictionary sort ordering, tokenization, and others.</span></span> <span data-ttu-id="6458d-106">Anche se queste impostazioni consentono a Windows Search di fornire un supporto localizzato eccellente, possono verificarsi risultati imprevisti quando viene eseguita una ricerca nei documenti di un'impostazione locale usando un sistema impostato su altre impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="6458d-106">Although these settings help Windows Search provide excellent localized support, unexpected results can occur when documents from one locale are searched by using a system that is set to another locale.</span></span>

<span data-ttu-id="6458d-107">Quando l'oggetto [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) elabora le proprietà e il contenuto di testo di un documento, segnala la lingua del documento all'indicizzatore di contenuto.</span><span class="sxs-lookup"><span data-stu-id="6458d-107">When the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) object processes a document's text properties and content, it reports the language of that document to the content indexer.</span></span> <span data-ttu-id="6458d-108">Utilizzando queste informazioni, Windows Search può applicare il Word breaker appropriato.</span><span class="sxs-lookup"><span data-stu-id="6458d-108">Using this information, Windows Search can apply the appropriate word breaker.</span></span>

 

 
