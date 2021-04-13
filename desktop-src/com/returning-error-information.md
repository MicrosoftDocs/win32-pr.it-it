---
title: Restituzione di informazioni sull'errore
description: Restituzione di informazioni sull'errore
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303db82dc220d09d4db7f52bf4c04ad1e5ca691f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399750"
---
# <a name="returning-error-information"></a><span data-ttu-id="856f1-103">Restituzione di informazioni sull'errore</span><span class="sxs-lookup"><span data-stu-id="856f1-103">Returning Error Information</span></span>

<span data-ttu-id="856f1-104">Utilizzando le interfacce e le funzioni di gestione degli errori COM, è possibile restituire informazioni sugli errori eseguendo i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="856f1-104">Using the COM error-handling interfaces and functions, you can return error information by performing the following the steps:</span></span>

1.  <span data-ttu-id="856f1-105">Implementare l'interfaccia [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="856f1-105">Implement the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span>
2.  <span data-ttu-id="856f1-106">Per creare un'istanza dell'oggetto errore generico, chiamare la funzione [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="856f1-106">To create an instance of the generic error object, call the [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) function.</span></span>
3.  <span data-ttu-id="856f1-107">Per impostarne il contenuto, usare i metodi [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="856f1-107">To set its contents, use the [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) methods.</span></span>
4.  <span data-ttu-id="856f1-108">Per associare l'oggetto Error al thread logico corrente, chiamare la funzione [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="856f1-108">To associate the error object with the current logical thread, call the [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) function.</span></span>

<span data-ttu-id="856f1-109">Le interfacce di gestione degli errori creano e gestiscono un oggetto Error, che fornisce informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="856f1-109">The error handling interfaces create and manage an error object, which provides information about the error.</span></span> <span data-ttu-id="856f1-110">L'oggetto Error non è uguale all'oggetto che ha rilevato l'errore.</span><span class="sxs-lookup"><span data-stu-id="856f1-110">The error object is not the same as the object that encountered the error.</span></span> <span data-ttu-id="856f1-111">Si tratta di un oggetto separato associato al thread di esecuzione corrente.</span><span class="sxs-lookup"><span data-stu-id="856f1-111">It is a separate object associated with the current thread of execution.</span></span>

 

 