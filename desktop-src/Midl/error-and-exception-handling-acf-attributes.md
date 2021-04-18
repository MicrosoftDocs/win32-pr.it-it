---
title: Attributi ACF di gestione degli errori e delle eccezioni
description: Usare gli attributi seguenti per la gestione degli errori.
ms.assetid: fb00df67-4645-4ef0-9216-618d0af1d9d4
keywords:
- MIDL, attributi, errori e gestione delle eccezioni di ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7187ab887fa1d09b18385b86065775ca0e656f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299790"
---
# <a name="error-and-exception-handling-acf-attributes"></a><span data-ttu-id="48603-104">Attributi ACF di gestione degli errori e delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="48603-104">Error and Exception Handling ACF Attributes</span></span>

<span data-ttu-id="48603-105">Usare gli attributi seguenti per la gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="48603-105">Use the following attributes for error handling.</span></span>



| <span data-ttu-id="48603-106">Attributo</span><span class="sxs-lookup"><span data-stu-id="48603-106">Attribute</span></span>                                                                | <span data-ttu-id="48603-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="48603-107">Usage</span></span>                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48603-108">stato di errore [**\_ dello stato di comunicazione**](comm-status.md)[**\_**](fault-status.md)</span><span class="sxs-lookup"><span data-stu-id="48603-108">[**comm\_status**](comm-status.md)[**fault\_status**](fault-status.md)</span></span> | <span data-ttu-id="48603-109">Consentire all'applicazione client di gestire le eccezioni normalmente causando la restituzione delle comunicazioni e degli errori del server al client come valori dei parametri.</span><span class="sxs-lookup"><span data-stu-id="48603-109">Let your client application handle exceptions gracefully by causing communication and server errors to be returned to the client as parameter values.</span></span> <span data-ttu-id="48603-110">L'applicazione client può quindi chiamare la funzione della fase di esecuzione RPC [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) per inoltrare un messaggio di errore all'utente.</span><span class="sxs-lookup"><span data-stu-id="48603-110">The client application can then call the RPC run-time function [**DceErrorInqText**](/windows/desktop/api/rpcdce/nf-rpcdce-dceerrorinqtext) to relay an error message to the user.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="48603-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48603-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48603-112">Importazione di file e librerie dei tipi</span><span class="sxs-lookup"><span data-stu-id="48603-112">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> </dl>

 

 