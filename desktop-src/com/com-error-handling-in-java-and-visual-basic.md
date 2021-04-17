---
title: Gestione degli errori COM in Java e Visual Basic
description: Gestione degli errori COM in Java e Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea12dc040218e14098ce2394fbb5cd2ebeff1704
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399774"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="44573-103">Gestione degli errori COM in Java e Visual Basic</span><span class="sxs-lookup"><span data-stu-id="44573-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="44573-104">Sono disponibili tre interfacce e tre funzioni che possono essere utilizzate in COM per fornire la gestione degli errori durante la programmazione in Java o Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="44573-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="44573-105">In Java e Visual Basic la chiamata al metodo non restituisce **HRESULT** come valore restituito.</span><span class="sxs-lookup"><span data-stu-id="44573-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="44573-106">Al contrario, questi linguaggi utilizzano le interfacce COM e le funzioni per ottenere i valori **HRESULT** e per gestire gli errori o le eccezioni.</span><span class="sxs-lookup"><span data-stu-id="44573-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="44573-107">(Le eccezioni sono eventi oltre il controllo del programma, ad esempio problemi di file o parametri non validi).</span><span class="sxs-lookup"><span data-stu-id="44573-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="44573-108">Le tre interfacce che forniscono supporto per **HRESULT** s sono elencate e descritte brevemente nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="44573-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                          |                                                                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44573-109">**ICreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="44573-109">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="44573-110">Imposta le informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="44573-110">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="44573-111">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="44573-111">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="44573-112">Restituisce informazioni da un oggetto Error.</span><span class="sxs-lookup"><span data-stu-id="44573-112">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="44573-113">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="44573-113">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="44573-114">Identifica l'oggetto come supporto dell'interfaccia [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="44573-114">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="44573-115">Le tre funzioni che forniscono supporto per **HRESULT** s sono elencate e descritte brevemente nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="44573-115">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                        |                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="44573-116">**CreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="44573-116">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="44573-117">Crea un'istanza di un oggetto errore generico.</span><span class="sxs-lookup"><span data-stu-id="44573-117">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="44573-118">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="44573-118">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="44573-119">Ottiene il puntatore alle informazioni sull'errore impostato dalla chiamata precedente a [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) nel thread logico corrente.</span><span class="sxs-lookup"><span data-stu-id="44573-119">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="44573-120">**SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="44573-120">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="44573-121">Imposta l'oggetto informazioni sull'errore per il thread di esecuzione corrente.</span><span class="sxs-lookup"><span data-stu-id="44573-121">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="44573-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="44573-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44573-123">Gestione degli errori in COM</span><span class="sxs-lookup"><span data-stu-id="44573-123">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

