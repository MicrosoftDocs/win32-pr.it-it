---
description: Un'applicazione può eseguire ricerche nella directory corrente per tutti i nomi di file che corrispondono a un modello specificato usando le funzioni FindFirstFile, FindFirstFileEx, FindNextFile e FindClose.
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: Ricerca di uno o più file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308215"
---
# <a name="searching-for-one-or-more-files"></a><span data-ttu-id="41791-103">Ricerca di uno o più file</span><span class="sxs-lookup"><span data-stu-id="41791-103">Searching for One or More Files</span></span>

<span data-ttu-id="41791-104">Un'applicazione può eseguire ricerche nella directory corrente per tutti i nomi di file che corrispondono a un modello specificato usando le funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="41791-104">An application can search the current directory for all file names that match a given pattern by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span> <span data-ttu-id="41791-105">Il criterio deve essere un nome di file valido e può includere caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="41791-105">The pattern must be a valid file name and can include wildcard characters.</span></span>

<span data-ttu-id="41791-106">Le funzioni [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) creano handle che **FindFirstFileEx** USA per cercare altri file con lo stesso modello.</span><span class="sxs-lookup"><span data-stu-id="41791-106">The [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) functions create handles that **FindFirstFileEx** uses to search for other files with the same pattern.</span></span> <span data-ttu-id="41791-107">Tutte le funzioni restituiscono informazioni sul file trovato.</span><span class="sxs-lookup"><span data-stu-id="41791-107">All functions return information about the file that was found.</span></span> <span data-ttu-id="41791-108">Queste informazioni includono il nome del file, la dimensione, gli attributi e l'ora.</span><span class="sxs-lookup"><span data-stu-id="41791-108">This information includes the file name, size, attributes, and time.</span></span>

<span data-ttu-id="41791-109">La funzione [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) consente anche a un'applicazione di cercare i file in base a criteri di ricerca aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="41791-109">The [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) function also allows an application to search for files based on additional search criteria.</span></span> <span data-ttu-id="41791-110">La funzione può limitare le ricerche ai nomi dei dispositivi o dei nomi di directory.</span><span class="sxs-lookup"><span data-stu-id="41791-110">The function can limit searches to device names or directory names.</span></span>

<span data-ttu-id="41791-111">La funzione [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) Elimina gli handle creati da [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) e [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span><span class="sxs-lookup"><span data-stu-id="41791-111">The [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function destroys handles created by [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span></span>

<span data-ttu-id="41791-112">Un'applicazione può cercare un singolo file in un percorso specifico usando la funzione [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) .</span><span class="sxs-lookup"><span data-stu-id="41791-112">An application can search for a single file on a specific path by using the [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) function.</span></span>

 

 
