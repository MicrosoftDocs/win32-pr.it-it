---
title: Codici in FACILITY_ITF
description: Codici in funzionalità \_ ITF
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955305"
---
# <a name="codes-in-facility_itf"></a><span data-ttu-id="74293-103">Codici in funzionalità \_ ITF</span><span class="sxs-lookup"><span data-stu-id="74293-103">Codes in FACILITY\_ITF</span></span>

<span data-ttu-id="74293-104">**HRESULT** s con funzionalità come la funzione \_ null e \_ la RPC della funzione hanno un significato universale perché sono definiti in una singola origine: Microsoft.</span><span class="sxs-lookup"><span data-stu-id="74293-104">**HRESULT** s with facilities such as FACILITY\_NULL and FACILITY\_RPC have universal meaning because they are defined at a single source: Microsoft.</span></span> <span data-ttu-id="74293-105">Tuttavia, i valori di **HRESULT** nella funzionalità \_ ITF sono determinati dalla funzione o dal metodo di interfaccia da cui vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="74293-105">However, **HRESULT** s in FACILITY\_ITF are determined by the function or interface method from which they are returned.</span></span> <span data-ttu-id="74293-106">Ciò significa che lo stesso valore a 32 bit nella funzionalità \_ ITF restituita da due diversi metodi di interfaccia potrebbe avere significati diversi.</span><span class="sxs-lookup"><span data-stu-id="74293-106">This means that the same 32-bit value in FACILITY\_ITF returned from two different interface methods might have different meanings.</span></span>

<span data-ttu-id="74293-107">Il motivo per cui **HRESULT** s nella funzionalità \_ ITF può avere significati diversi in interfacce diverse è che **HRESULT** s viene mantenuto in una dimensione del tipo di dati efficiente di 32 bit.</span><span class="sxs-lookup"><span data-stu-id="74293-107">The reason **HRESULT** s in FACILITY\_ITF can have different meanings in different interfaces is that **HRESULT** s are kept to an efficient data type size of 32 bits.</span></span> <span data-ttu-id="74293-108">Sfortunatamente, 32 bit non è sufficiente per lo sviluppo di un sistema di allocazione di codice di errore che evita codici in conflitto allocati da programmatori diversi in momenti diversi in posizioni diverse (a differenza della gestione degli identificatori di interfaccia e dei CLSID).</span><span class="sxs-lookup"><span data-stu-id="74293-108">Unfortunately, 32 bits is not large enough for the development of an error code allocation system that avoids conflicting codes allocated by different programmers at different times in different places (unlike the handling of interface identifiers and CLSIDs).</span></span> <span data-ttu-id="74293-109">Di conseguenza, l' **HRESULT** a 32 bit è strutturato in modo tale che Microsoft possa definire diversi codici di errore universali, consentendo ad altri programmatori di definire nuovi codici di errore senza temere conflitti.</span><span class="sxs-lookup"><span data-stu-id="74293-109">As a result, the 32-bit **HRESULT** is structured such that Microsoft can define several universal error codes, while allowing other programmers to define new error codes without fear of conflict.</span></span> <span data-ttu-id="74293-110">La convenzione relativa al codice di stato è la seguente:</span><span class="sxs-lookup"><span data-stu-id="74293-110">The status code convention is as follows:</span></span>

-   <span data-ttu-id="74293-111">I codici di stato in strutture diverse \_ dalla funzionalità ITF possono essere definiti solo da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="74293-111">Status codes in facilities other than FACILITY\_ITF can be defined only by Microsoft.</span></span>
-   <span data-ttu-id="74293-112">I codici di stato in funzionalità \_ ITF sono definiti esclusivamente dallo sviluppatore dell'interfaccia o funzione che restituisce il codice di stato.</span><span class="sxs-lookup"><span data-stu-id="74293-112">Status codes in facility FACILITY\_ITF are defined solely by the developer of the interface or function that returns the status code.</span></span> <span data-ttu-id="74293-113">Per evitare conflitti tra i codici di errore, chi definisce l'interfaccia è responsabile del coordinamento e della pubblicazione dei \_ codici di stato ITF della struttura associati a tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="74293-113">To avoid conflicting error codes, whoever defines the interface is responsible for coordinating and publishing the FACILITY\_ITF status codes associated with that interface.</span></span>

<span data-ttu-id="74293-114">Tutti i codici ITF della funzionalità definita da COM \_ hanno un valore di codice compreso nell'intervallo di 0x0000-0x01ff.</span><span class="sxs-lookup"><span data-stu-id="74293-114">All the COM-defined FACILITY\_ITF codes have a code value in the range of 0x0000-0x01FF.</span></span> <span data-ttu-id="74293-115">Sebbene sia possibile usare qualsiasi codice nella funzionalità \_ ITF, è consigliabile usare solo i valori del codice nell'intervallo di 0x0200-0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="74293-115">While it is legal to use any codes in FACILITY\_ITF, it is recommended that only code values in the range of 0x0200-0xFFFF be used.</span></span> <span data-ttu-id="74293-116">Questa raccomandazione viene effettuata come mezzo per ridurre la confusione con eventuali errori definiti da COM.</span><span class="sxs-lookup"><span data-stu-id="74293-116">This recommendation is made as a means of reducing confusion with any COM-defined errors.</span></span>

<span data-ttu-id="74293-117">È inoltre consigliabile che gli sviluppatori definiscano nuove funzioni e interfacce per restituire i codici di errore definiti da COM e in strutture diverse dalla funzionalità \_ ITF.</span><span class="sxs-lookup"><span data-stu-id="74293-117">It is also recommended that developers define new functions and interfaces to return error codes as defined by COM and in facilities other than FACILITY\_ITF.</span></span> <span data-ttu-id="74293-118">In particolare, le interfacce che hanno la possibilità di essere riutilizzate in remoto con RPC in futuro dovrebbero definire i \_ codici RPC della struttura come validi.</span><span class="sxs-lookup"><span data-stu-id="74293-118">In particular, interfaces that have any chance of being remoted using RPC in the future should define the FACILITY\_RPC codes as legal.</span></span> <span data-ttu-id="74293-119">E \_ imprevisto è un codice di errore specifico che la maggior parte degli sviluppatori desidera rendere legale universalmente.</span><span class="sxs-lookup"><span data-stu-id="74293-119">E\_UNEXPECTED is a specific error code that most developers will want to make universally legal.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74293-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74293-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74293-121">Gestione degli errori in COM</span><span class="sxs-lookup"><span data-stu-id="74293-121">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




