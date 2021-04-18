---
description: Le API Windows Image Acquisition (WIA) restituiscono lo stato di completamento in un valore restituito HRESULT.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: Informazioni sull'errore WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31bcbba9e42d8b7a95b892eb8bba14a56ad758e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307315"
---
# <a name="wia-error-information"></a><span data-ttu-id="f590b-103">Informazioni sull'errore WIA</span><span class="sxs-lookup"><span data-stu-id="f590b-103">WIA Error Information</span></span>

<span data-ttu-id="f590b-104">Le API Windows Image Acquisition (WIA) restituiscono lo stato di completamento in un valore restituito HRESULT.</span><span class="sxs-lookup"><span data-stu-id="f590b-104">The Windows Image Acquisition (WIA)APIs return their completion status in an HRESULT return value.</span></span> <span data-ttu-id="f590b-105">Le applicazioni controllano questi valori restituiti rispetto alla \_ costante WIA della struttura per determinare se l'errore richiede l'intervento dell'utente da cancellare, ad esempio un percorso di carta inceppata, e segnalarli all'utente.</span><span class="sxs-lookup"><span data-stu-id="f590b-105">Applications check these return values against the FACILITY\_WIA constant to determine whether the error requires user intervention to clear, such as a jammed paper path, and report them to the user.</span></span> <span data-ttu-id="f590b-106">Inoltre, tutti gli errori a livello di driver vengono registrati in dettaglio nel registro eventi, usando le stringhe di errore fornite dal dispositivo minidriver.</span><span class="sxs-lookup"><span data-stu-id="f590b-106">In addition, all driver-level errors are logged in detail to the event log, using error strings provided by the device minidriver.</span></span> <span data-ttu-id="f590b-107">Per un elenco di codici di errore specifici di WIA, vedere [codici di errore](-wia-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f590b-107">For a listing of WIA-specific error codes, see [Error Codes](-wia-error-codes.md).</span></span>

 

 



