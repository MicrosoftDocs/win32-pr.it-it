---
description: Un processo utilizza la funzione CreateFile per aprire un handle per una risorsa di comunicazione.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Handle delle risorse di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401442"
---
# <a name="communications-resource-handles"></a><span data-ttu-id="0c38d-103">Handle delle risorse di comunicazione</span><span class="sxs-lookup"><span data-stu-id="0c38d-103">Communications Resource Handles</span></span>

<span data-ttu-id="0c38d-104">Un processo utilizza la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un handle per una risorsa di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="0c38d-104">A process uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a communications resource.</span></span> <span data-ttu-id="0c38d-105">Se, ad esempio, si specifica COM1, viene aperto un handle per una porta seriale e LPT1 apre un handle per una porta parallela.</span><span class="sxs-lookup"><span data-stu-id="0c38d-105">For example, specifying COM1 opens a handle to a serial port, and LPT1 opens a handle to a parallel port.</span></span> <span data-ttu-id="0c38d-106">Se la risorsa specificata è attualmente in uso da un altro processo, **CreateFile** ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0c38d-106">If the specified resource is currently being used by another process, **CreateFile** fails.</span></span> <span data-ttu-id="0c38d-107">Qualsiasi thread del processo può utilizzare l'handle restituito da **CreateFile** per identificare la risorsa in una qualsiasi delle funzioni che accedono alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c38d-107">Any thread of the process can use the handle returned by **CreateFile** to identify the resource in any of the functions that access the resource.</span></span>

<span data-ttu-id="0c38d-108">Quando il processo chiama [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire una risorsa di comunicazione, specifica gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c38d-108">When the process calls [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it specifies the following attributes:</span></span>

-   <span data-ttu-id="0c38d-109">Quale tipo di accesso in lettura/scrittura esiste per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="0c38d-109">What type of read/write access exists for the specified resource.</span></span>
-   <span data-ttu-id="0c38d-110">Indica se l'handle può essere ereditato dai processi figlio.</span><span class="sxs-lookup"><span data-stu-id="0c38d-110">Whether the handle can be inherited by child processes.</span></span>
-   <span data-ttu-id="0c38d-111">Indica se l'handle può essere utilizzato nelle operazioni di I/O sovrapposte (asincrone).</span><span class="sxs-lookup"><span data-stu-id="0c38d-111">Whether the handle can be used in overlapped (asynchronous) I/O operations.</span></span> <span data-ttu-id="0c38d-112">Per una descrizione delle operazioni sovrapposte, vedere [sincronizzazione](/windows/desktop/Sync/synchronization).</span><span class="sxs-lookup"><span data-stu-id="0c38d-112">(For a description of overlapped operations, see [Synchronization](/windows/desktop/Sync/synchronization).)</span></span>

<span data-ttu-id="0c38d-113">Quando il processo utilizza [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire una risorsa di comunicazione, è necessario specificare determinati valori per i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="0c38d-113">When the process uses [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it must specify certain values for the following parameters:</span></span>

-   <span data-ttu-id="0c38d-114">Il parametro *fdwShareMode* deve essere zero, aprendo la risorsa per l'accesso esclusivo.</span><span class="sxs-lookup"><span data-stu-id="0c38d-114">The *fdwShareMode* parameter must be zero, opening the resource for exclusive access.</span></span>
-   <span data-ttu-id="0c38d-115">Il parametro *fdwCreate* deve specificare il \_ flag aperto esistente.</span><span class="sxs-lookup"><span data-stu-id="0c38d-115">The *fdwCreate* parameter must specify the OPEN\_EXISTING flag.</span></span>
-   <span data-ttu-id="0c38d-116">Il parametro *hTemplateFile* deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="0c38d-116">The *hTemplateFile* parameter must be **NULL**.</span></span>

<span data-ttu-id="0c38d-117">Quando si usa [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) per aprire un handle direttamente in un dispositivo, un'applicazione deve usare i caratteri speciali " \\ \\ . \\ " per identificare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c38d-117">When using [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a handle directly to a device, an application must use the special characters " \\\\ .\\" to identify the device.</span></span> <span data-ttu-id="0c38d-118">Per aprire un handle per l'unità A, ad esempio, specificare \\ \\ . \\ r: per il parametro *lpszName* di **CreateFile**.</span><span class="sxs-lookup"><span data-stu-id="0c38d-118">For example, to open a handle to drive A, specify \\\\ .\\a: for the *lpszName* parameter of **CreateFile**.</span></span> <span data-ttu-id="0c38d-119">Il processo chiamante può usare l'handle nella funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) per inviare i codici di controllo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0c38d-119">The calling process can use the handle in the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function to send control codes to the device.</span></span>

 

 
