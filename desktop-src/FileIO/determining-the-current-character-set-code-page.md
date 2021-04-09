---
description: La funzione AreFileApisANSI determina se le funzioni di I/O dei file utilizzano la tabella codici del set di caratteri ANSI o OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Determinazione della tabella codici del set di caratteri corrente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882189"
---
# <a name="determining-the-current-character-set-code-page"></a><span data-ttu-id="f4186-103">Determinazione della tabella codici del set di caratteri corrente</span><span class="sxs-lookup"><span data-stu-id="f4186-103">Determining the Current Character Set Code Page</span></span>

<span data-ttu-id="f4186-104">La funzione [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina se le funzioni di i/O dei file utilizzano la tabella codici del set di caratteri ANSI o OEM.</span><span class="sxs-lookup"><span data-stu-id="f4186-104">The [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) function determines whether the file I/O functions are using the ANSI or OEM character set code page.</span></span> <span data-ttu-id="f4186-105">La funzione [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) fa sì che le funzioni usino la tabella codici ANSI.</span><span class="sxs-lookup"><span data-stu-id="f4186-105">The [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) function causes the functions to use the ANSI code page.</span></span> <span data-ttu-id="f4186-106">La funzione [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) fa sì che le funzioni usino la tabella codici OEM.</span><span class="sxs-lookup"><span data-stu-id="f4186-106">The [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) function causes the functions to use the OEM code page.</span></span>

<span data-ttu-id="f4186-107">Per impostazione predefinita, le funzioni di I/O dei file usano i nomi file ANSI.</span><span class="sxs-lookup"><span data-stu-id="f4186-107">By default, file I/O functions use ANSI file names.</span></span> <span data-ttu-id="f4186-108">Le funzioni esportate da Kernel32.dll che accettano o restituiscono nomi di file sono interessate dall'impostazione della tabella codici del file.</span><span class="sxs-lookup"><span data-stu-id="f4186-108">Functions exported by Kernel32.dll that accept or return file names are affected by the file code page setting.</span></span>

<span data-ttu-id="f4186-109">Sia [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) che [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) impostano la tabella codici per processo, anziché per thread o per computer.</span><span class="sxs-lookup"><span data-stu-id="f4186-109">Both [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) and [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) set the code page per process, rather than per thread or per computer.</span></span>

 

 



