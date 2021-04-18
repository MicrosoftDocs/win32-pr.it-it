---
description: Dopo aver creato una DLL, è possibile usare le funzioni definite in un'applicazione. Di seguito è riportata una semplice applicazione console che usa la funzione put esportata da Myputs.dll (vedere Creazione di una libreria di Dynamic-Link semplice).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Uso di Load-Time collegamento dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e5d14ba2190528c44d892b957d22b273fd4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310041"
---
# <a name="using-load-time-dynamic-linking"></a><span data-ttu-id="a3880-104">Uso di Load-Time collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="a3880-104">Using Load-Time Dynamic Linking</span></span>

<span data-ttu-id="a3880-105">Dopo aver creato una DLL, è possibile usare le funzioni definite in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a3880-105">After you have created a DLL, you can use the functions it defines in an application.</span></span> <span data-ttu-id="a3880-106">Di seguito è riportata una semplice applicazione console che usa la funzione put esportata da Myputs.dll (vedere [creazione di una libreria di Dynamic-Link semplice](creating-a-simple-dynamic-link-library.md)).</span><span class="sxs-lookup"><span data-stu-id="a3880-106">The following is a simple console application that uses the myPuts function exported from Myputs.dll (see [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).</span></span>

<span data-ttu-id="a3880-107">Poiché in questo esempio la funzione DLL viene chiamata in modo esplicito, il modulo per l'applicazione deve essere collegato con la libreria di importazione My put. lib.</span><span class="sxs-lookup"><span data-stu-id="a3880-107">Because this example calls the DLL function explicitly, the module for the application must be linked with the import library Myputs.lib.</span></span> <span data-ttu-id="a3880-108">Per ulteriori informazioni sulla creazione di dll, vedere la documentazione inclusa con gli strumenti di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="a3880-108">For more information about building DLLs, see the documentation included with your development tools.</span></span>


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a><span data-ttu-id="a3880-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3880-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3880-110">Collegamento dinamico in fase di caricamento</span><span class="sxs-lookup"><span data-stu-id="a3880-110">Load-Time Dynamic Linking</span></span>](load-time-dynamic-linking.md)
</dt> </dl>

 

 



