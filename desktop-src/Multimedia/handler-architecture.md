---
title: Architettura del gestore
description: Architettura del gestore
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044816"
---
# <a name="handler-architecture"></a><span data-ttu-id="80259-103">Architettura del gestore</span><span class="sxs-lookup"><span data-stu-id="80259-103">Handler Architecture</span></span>

<span data-ttu-id="80259-104">La funzione interna di un gestore di file o di flussi viene definita dal gestore stesso.</span><span class="sxs-lookup"><span data-stu-id="80259-104">The internal function of a file or stream handler is defined by the handler itself.</span></span> <span data-ttu-id="80259-105">Per un'applicazione, un gestore di file viene in genere visualizzato come modulo per la lettura e la scrittura di file AVI.</span><span class="sxs-lookup"><span data-stu-id="80259-105">To an application, a file handler typically appears as a module to read and write AVI files.</span></span> <span data-ttu-id="80259-106">Analogamente, un gestore di flusso viene visualizzato come modulo per la lettura e la scrittura di un tipo specifico di flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="80259-106">Similarly, a stream handler appears as a module to read and write a specific type of data stream.</span></span> <span data-ttu-id="80259-107">L'interfaccia di flusso coerente rende l'origine e la destinazione del flusso non importanti per l'applicazione che utilizza il gestore.</span><span class="sxs-lookup"><span data-stu-id="80259-107">The consistent stream interface makes the source and destination of the stream unimportant to the application that uses the handler.</span></span>

<span data-ttu-id="80259-108">Un gestore di file consente di accedere a un'origine dati costituita da uno o più flussi di dati.</span><span class="sxs-lookup"><span data-stu-id="80259-108">A file handler provides access to a data source consisting of one or more data streams.</span></span> <span data-ttu-id="80259-109">I gestori di file consentono in genere l'accesso a file su disco contenenti uno o più flussi di dati e le funzioni interne del gestore file leggono e scrivono i dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="80259-109">File handlers typically provide access to disk files containing one or more data streams, and the internal functions of the file handler read and write the multimedia data.</span></span> <span data-ttu-id="80259-110">Tuttavia, i gestori di file possono funzionare con qualsiasi origine dati, ad esempio un canale di trasmissione digitale che contiene diversi flussi di dati intermisti.</span><span class="sxs-lookup"><span data-stu-id="80259-110">However, file handlers can work with any data source, such as a digital transmission channel containing several intermingled data streams.</span></span>

<span data-ttu-id="80259-111">Un gestore di flusso elabora invece un tipo di dati e viene visualizzato come flusso di dati in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80259-111">In contrast, a stream handler processes one type of data and appears as a data stream to an application.</span></span> <span data-ttu-id="80259-112">Un gestore di flusso può fornire dati che produce oppure può recuperare dati da un file o da un'origine esterna.</span><span class="sxs-lookup"><span data-stu-id="80259-112">A stream handler can provide data that it manufactures, or it can retrieve data from a file or an external source.</span></span> <span data-ttu-id="80259-113">Fornisce i dati in un formato che può essere usato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80259-113">It supplies its data in a format that your application can use.</span></span>

 

 




