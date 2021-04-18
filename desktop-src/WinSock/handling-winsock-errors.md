---
description: Gestione degli errori in Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Gestione degli errori Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbad01ad7add7995cf978e101535104f6dc0da6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306955"
---
# <a name="handling-winsock-errors"></a><span data-ttu-id="e4207-103">Gestione degli errori Winsock</span><span class="sxs-lookup"><span data-stu-id="e4207-103">Handling Winsock Errors</span></span>

<span data-ttu-id="e4207-104">La maggior parte delle funzioni di Windows Sockets 2 non restituisce la determinata origine di un errore quando la funzione restituisce.</span><span class="sxs-lookup"><span data-stu-id="e4207-104">Most Windows Sockets 2 functions do not return the specific cause of an error when the function returns.</span></span> <span data-ttu-id="e4207-105">Alcune funzioni Winsock restituiscono un valore pari a zero in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e4207-105">Some Winsock functions return a value of zero if successful.</span></span> <span data-ttu-id="e4207-106">In caso contrario, \_ viene restituito l'errore di socket del valore (-1) ed è possibile recuperare un numero di errore specifico chiamando la funzione [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) .</span><span class="sxs-lookup"><span data-stu-id="e4207-106">Otherwise, the value SOCKET\_ERROR (-1) is returned and a specific error number can be retrieved by calling the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function.</span></span> <span data-ttu-id="e4207-107">Per le funzioni Winsock che restituiscono un handle, un valore restituito di socket non valido \_ (0xFFFF) indica un errore e un numero di errore specifico può essere recuperato chiamando **WSAGetLastError**.</span><span class="sxs-lookup"><span data-stu-id="e4207-107">For Winsock functions that return a handle, a return value of INVALID\_SOCKET (0xffff) indicates an error and a specific error number can be retrieved by calling **WSAGetLastError**.</span></span> <span data-ttu-id="e4207-108">Per le funzioni Winsock che restituiscono un puntatore, un valore restituito **null** indica un errore e un numero di errore specifico può essere recuperato chiamando la funzione **WSAGetLastError** .</span><span class="sxs-lookup"><span data-stu-id="e4207-108">For Winsock functions that return a pointer, a return value of **NULL** indicates an error and a specific error number can be retrieved by calling the **WSAGetLastError** function.</span></span>

<span data-ttu-id="e4207-109">Un codice di errore Winsock può essere convertito in un valore HRESULT da utilizzare in una chiamata di procedura remota (RPC) utilizzando HRESULT \_ da \_ Win32.</span><span class="sxs-lookup"><span data-stu-id="e4207-109">A Winsock error code can be converted to an HRESULT for use in a remote procedure call (RPC) using HRESULT\_FROM\_WIN32.</span></span> <span data-ttu-id="e4207-110">Nelle versioni precedenti di Platform Software Development Kit (SDK), HRESULT \_ da \_ Win32 è stato definito come una macro nel file di intestazione *Winerror. h* .</span><span class="sxs-lookup"><span data-stu-id="e4207-110">In earlier versions of the Platform Software Development Kit (SDK), HRESULT\_FROM\_WIN32 was defined as a macro in the *Winerror.h* header file.</span></span> <span data-ttu-id="e4207-111">Nel Software Development Kit (SDK) di Microsoft Windows, HRESULT \_ da \_ Win32 viene definito come funzione inline nel file di intestazione *Winerror. h* .</span><span class="sxs-lookup"><span data-stu-id="e4207-111">In the Microsoft Windows Software Development Kit (SDK), HRESULT\_FROM\_WIN32 is defined as an inline function in the *Winerror.h* header file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4207-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4207-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4207-113">Codici di errore di Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="e4207-113">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



