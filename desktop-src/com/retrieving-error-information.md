---
title: Recupero delle informazioni sugli errori
description: Recupero delle informazioni sugli errori
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5918ee7338d1b8428079da20ecb43c7b4b4ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047391"
---
# <a name="retrieving-error-information"></a><span data-ttu-id="88bc3-103">Recupero delle informazioni sugli errori</span><span class="sxs-lookup"><span data-stu-id="88bc3-103">Retrieving Error Information</span></span>

<span data-ttu-id="88bc3-104">Utilizzando le interfacce e le funzioni di gestione degli errori COM, è possibile recuperare le informazioni sugli errori nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="88bc3-104">Using the COM error-handling interfaces and functions, you can retrieve error information as follows:</span></span>

1.  <span data-ttu-id="88bc3-105">Controllare se il valore restituito rappresenta un errore che l'oggetto è pronto a gestire.</span><span class="sxs-lookup"><span data-stu-id="88bc3-105">Check whether the returned value represents an error that the object is prepared to handle.</span></span>
2.  <span data-ttu-id="88bc3-106">Chiamare [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un puntatore all'interfaccia [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="88bc3-106">Call [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span> <span data-ttu-id="88bc3-107">Chiamare quindi [**ISupportErrorInfo:: InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) per verificare che l'errore sia stato generato dall'oggetto che lo ha restituito e che l'oggetto Error sia relativo all'errore corrente e non a una chiamata precedente.</span><span class="sxs-lookup"><span data-stu-id="88bc3-107">Then call [**ISupportErrorInfo::InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) to verify that the error was raised by the object that returned it and that the error object pertains to the current error and not to a previous call.</span></span>
3.  <span data-ttu-id="88bc3-108">Per ottenere un puntatore all'oggetto Error, chiamare la funzione [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="88bc3-108">To get a pointer to the error object, call the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function.</span></span>
4.  <span data-ttu-id="88bc3-109">Per recuperare informazioni dall'oggetto Error, usare i metodi [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="88bc3-109">To retrieve information from the error object, use the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) methods.</span></span>

<span data-ttu-id="88bc3-110">Se l'oggetto non è pronto per gestire l'errore, ma è necessario propagare le informazioni sugli errori ulteriormente nella catena di chiamate, è sufficiente passare il valore restituito al chiamante.</span><span class="sxs-lookup"><span data-stu-id="88bc3-110">If the object is not prepared to handle the error but needs to propagate the error information further down the call chain, it should simply pass the return value to its caller.</span></span> <span data-ttu-id="88bc3-111">Poiché la funzione [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) Cancella le informazioni sull'errore e passa la proprietà dell'oggetto Error al chiamante, la funzione deve essere chiamata solo dall'oggetto che gestisce l'errore.</span><span class="sxs-lookup"><span data-stu-id="88bc3-111">Because the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function clears the error information and passes ownership of the error object to the caller, the function should be called only by the object that handles the error.</span></span>

 

 