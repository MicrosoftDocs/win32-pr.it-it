---
title: Errore
description: Errore
ms.assetid: d3a087e4-7b57-4070-aa82-3673bc18a54f
keywords:
- Funzioni di callback AVICap, messaggi di notifica degli errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f418f16ae2af15902e96927990d79a4ecac08b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045133"
---
# <a name="error"></a><span data-ttu-id="b9baa-104">Errore</span><span class="sxs-lookup"><span data-stu-id="b9baa-104">Error</span></span>

<span data-ttu-id="b9baa-105">Una finestra di acquisizione usa i messaggi di notifica degli errori per notificare l'applicazione degli errori AVICap, ad esempio l'esaurimento dello spazio su disco, il tentativo di scrittura in un file di sola lettura, l'errore di accesso all'hardware o l'eliminazione di un numero eccessivo di frame.</span><span class="sxs-lookup"><span data-stu-id="b9baa-105">A capture window uses error notification messages to notify your application of AVICap errors, such as running out of disk space, attempting to write to a read-only file, failing to access hardware, or dropping too many frames.</span></span> <span data-ttu-id="b9baa-106">Il contenuto di una notifica di errore include un identificatore di messaggio e una stringa di testo formattata pronta per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b9baa-106">The content of an error notification includes a message identifier and a formatted text string ready for display.</span></span> <span data-ttu-id="b9baa-107">L'applicazione può utilizzare l'identificatore del messaggio per filtrare le notifiche e limitare i messaggi da presentare all'utente.</span><span class="sxs-lookup"><span data-stu-id="b9baa-107">Your application can use the message identifier to filter the notifications and limit the messages to present to the user.</span></span> <span data-ttu-id="b9baa-108">Un identificatore di messaggio zero indica che è in corso l'avvio di una nuova operazione e che la funzione di callback deve cancellare qualsiasi messaggio di errore visualizzato.</span><span class="sxs-lookup"><span data-stu-id="b9baa-108">A message identifier of zero indicates a new operation is starting and the callback function should clear any displayed error message.</span></span>

 

 




