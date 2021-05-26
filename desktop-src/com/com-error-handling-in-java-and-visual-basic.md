---
title: Gestione degli errori COM in Java e Visual Basic
description: Gestione degli errori COM in Java e Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c55c1c2414c69ff9398845858baadebd58cbf9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424011"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="6e8e5-103">Gestione degli errori COM in Java e Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6e8e5-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="6e8e5-104">Esistono tre interfacce e tre funzioni che possono essere usate in COM per fornire la gestione degli errori durante la programmazione in Java o Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="6e8e5-105">In Java e Visual Basic, la chiamata al metodo non restituisce **un HRESULT** come valore restituito.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="6e8e5-106">Questi linguaggi usano invece le interfacce e le funzioni COM per ottenere **valori HRESULT** e per gestire errori o eccezioni.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="6e8e5-107">Le eccezioni sono eventi oltre il controllo del programma, ad esempio problemi di file o parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="6e8e5-108">Le tre interfacce che forniscono supporto per **HRESULT** sono elencate e descritte brevemente nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|  <span data-ttu-id="6e8e5-109">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="6e8e5-109">Interface</span></span>                                                                        |  <span data-ttu-id="6e8e5-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8e5-110">Description</span></span>                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e8e5-111">**ICreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6e8e5-111">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="6e8e5-112">Imposta le informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-112">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="6e8e5-113">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6e8e5-113">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="6e8e5-114">Restituisce informazioni da un oggetto errore.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-114">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="6e8e5-115">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6e8e5-115">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="6e8e5-116">Identifica l'oggetto come supporto [**dell'interfaccia IErrorInfo.**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)</span><span class="sxs-lookup"><span data-stu-id="6e8e5-116">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="6e8e5-117">Le tre funzioni che forniscono supporto per **HRESULT** sono elencate e descritte brevemente nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-117">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|    <span data-ttu-id="6e8e5-118">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="6e8e5-118">Interface</span></span>       |       <span data-ttu-id="6e8e5-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e8e5-119">Description</span></span>       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e8e5-120">**CreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6e8e5-120">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="6e8e5-121">Crea un'istanza di un oggetto errore generico.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-121">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="6e8e5-122">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="6e8e5-122">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="6e8e5-123">Ottiene il puntatore alle informazioni sull'errore impostato dalla chiamata precedente [**a SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) nel thread logico corrente.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-123">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="6e8e5-124">**Seterrorinfo**</span><span class="sxs-lookup"><span data-stu-id="6e8e5-124">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="6e8e5-125">Imposta l'oggetto informazioni sull'errore per il thread di esecuzione corrente.</span><span class="sxs-lookup"><span data-stu-id="6e8e5-125">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="6e8e5-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6e8e5-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e8e5-127">Gestione degli errori in COM</span><span class="sxs-lookup"><span data-stu-id="6e8e5-127">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

