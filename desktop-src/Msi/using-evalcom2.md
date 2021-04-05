---
description: Evalcom2.dll può essere usato per implementare le operazioni di convalida per i pacchetti di installazione e unire i moduli usando gli analizzatori di coerenza interni-CIEM.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Uso di Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49a165115b505d5c78ebe5b5e714b8a3c359d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751695"
---
# <a name="using-evalcom2"></a><span data-ttu-id="68278-103">Uso di Evalcom2</span><span class="sxs-lookup"><span data-stu-id="68278-103">Using Evalcom2</span></span>

<span data-ttu-id="68278-104">Evalcom2.dll può essere usato per implementare le operazioni di convalida per i pacchetti di installazione e unire i moduli usando gli [analizzatori di coerenza interni-CIEM](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="68278-104">Evalcom2.dll can be used to implement validation operations for installation packages and merge modules using [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="68278-105">L'oggetto Main implementa le interfacce per i programmi C/C++.</span><span class="sxs-lookup"><span data-stu-id="68278-105">The main object implements interfaces for C/C++ programs.</span></span>

<span data-ttu-id="68278-106">L'oggetto Main implementa anche le [interfacce Evalcom2](evalcom2-interfaces.md) per i programmi C/C++.</span><span class="sxs-lookup"><span data-stu-id="68278-106">The main object also implements [Evalcom2 interfaces](evalcom2-interfaces.md) for C/C++ programs.</span></span> <span data-ttu-id="68278-107">Il CLSID necessario per ottenere l'interfaccia da [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) è {6E5E1910-8053-4660-B795-6B612E29BC58}.</span><span class="sxs-lookup"><span data-stu-id="68278-107">The CLSID required to obtain the interface from [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is {6E5E1910-8053-4660-B795-6B612E29BC58}.</span></span> <span data-ttu-id="68278-108">REFIID è {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.</span><span class="sxs-lookup"><span data-stu-id="68278-108">The REFIID is {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.</span></span>

<span data-ttu-id="68278-109">Per implementare le operazioni di convalida, è possibile utilizzare la procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="68278-109">You can use the following procedure to implement validation operations.</span></span>

<span data-ttu-id="68278-110">**Per implementare le operazioni di convalida**</span><span class="sxs-lookup"><span data-stu-id="68278-110">**To implement validation operations**</span></span>

1.  <span data-ttu-id="68278-111">Inizializzare COM sul thread chiamante usando [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).</span><span class="sxs-lookup"><span data-stu-id="68278-111">Initialize COM on the calling thread using [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).</span></span>
2.  <span data-ttu-id="68278-112">Ottenere il puntatore all'interfaccia [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) utilizzando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="68278-112">Obtain the pointer to the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>
3.  <span data-ttu-id="68278-113">Aprire il pacchetto di installazione o il modulo merge usando il metodo [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) .</span><span class="sxs-lookup"><span data-stu-id="68278-113">Open the installation package or merge module using the [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) method.</span></span>
4.  <span data-ttu-id="68278-114">Aprire il file di valutazione usando il metodo [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) .</span><span class="sxs-lookup"><span data-stu-id="68278-114">Open the evaluation file using the [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) method.</span></span>
5.  <span data-ttu-id="68278-115">Impostare la funzione di callback di visualizzazione utilizzando il metodo di [**visualizzazione**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) .</span><span class="sxs-lookup"><span data-stu-id="68278-115">Set the display callback function using the [**SetDisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) method.</span></span>
6.  <span data-ttu-id="68278-116">Impostare la funzione di callback dello stato usando il metodo [**sestatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) .</span><span class="sxs-lookup"><span data-stu-id="68278-116">Set the status callback function using the [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) method.</span></span>
7.  <span data-ttu-id="68278-117">Eseguire la convalida usando il metodo [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) .</span><span class="sxs-lookup"><span data-stu-id="68278-117">Perform the validation using the [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) method.</span></span>
8.  <span data-ttu-id="68278-118">Chiudere il file con estensione cub usando il metodo [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) .</span><span class="sxs-lookup"><span data-stu-id="68278-118">Close the .cub file using the [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) method.</span></span>
9.  <span data-ttu-id="68278-119">Chiudere il database utilizzando il metodo [**ChiudiDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) .</span><span class="sxs-lookup"><span data-stu-id="68278-119">Close the database using the [**CloseDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) method.</span></span>
10. <span data-ttu-id="68278-120">Rilasciare l'interfaccia [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) .</span><span class="sxs-lookup"><span data-stu-id="68278-120">Release the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface.</span></span>
11. <span data-ttu-id="68278-121">Annullare l'inizializzazione di COM con [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span><span class="sxs-lookup"><span data-stu-id="68278-121">Uninitialize COM using [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

## <a name="related-topics"></a><span data-ttu-id="68278-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68278-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68278-123">Interfacce Evalcom2</span><span class="sxs-lookup"><span data-stu-id="68278-123">Evalcom2 Interfaces</span></span>](evalcom2-interfaces.md)
</dt> <dt>

[<span data-ttu-id="68278-124">Automazione della convalida</span><span class="sxs-lookup"><span data-stu-id="68278-124">Validation Automation</span></span>](validation-automation.md)
</dt> <dt>

[<span data-ttu-id="68278-125">Funzioni di callback di convalida</span><span class="sxs-lookup"><span data-stu-id="68278-125">Validation Callback Functions</span></span>](validation-callback-functions.md)
</dt> </dl>

 

 
