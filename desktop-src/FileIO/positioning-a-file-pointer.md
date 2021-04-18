---
description: Windows utilizza un puntatore di file per tenere traccia dei byte letti o scritti.
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: Posizionamento di un puntatore di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6588a3d65e71c2180c4e9753e65cd94ed070d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312353"
---
# <a name="positioning-a-file-pointer"></a><span data-ttu-id="b4824-103">Posizionamento di un puntatore di file</span><span class="sxs-lookup"><span data-stu-id="b4824-103">Positioning a File Pointer</span></span>

<span data-ttu-id="b4824-104">Quando un'applicazione chiama [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire un file per la prima volta, Windows posiziona il [puntatore del file](file-pointers.md) all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="b4824-104">When an application calls [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to open a file for the first time, Windows places the [file pointer](file-pointers.md) at the beginning of the file.</span></span> <span data-ttu-id="b4824-105">Poiché i byte vengono letti o scritti nel file, Windows sposta il puntatore del file in base al numero di byte letti o scritti.</span><span class="sxs-lookup"><span data-stu-id="b4824-105">As bytes are read from or written to the file, Windows advances the file pointer the number of bytes read or written.</span></span>

<span data-ttu-id="b4824-106">Un'applicazione può posizionare il puntatore del file in un offset specificato chiamando [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).</span><span class="sxs-lookup"><span data-stu-id="b4824-106">An application can position the file pointer to a specified offset by calling [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).</span></span>

<span data-ttu-id="b4824-107">La funzione [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) può essere utilizzata anche per eseguire una query sulla posizione corrente del puntatore del file specificando un metodo Move di **file \_ corrente** e una distanza pari a zero.</span><span class="sxs-lookup"><span data-stu-id="b4824-107">The [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function can also be used to query the current file pointer position by specifying a move method of **FILE\_CURRENT** and a distance of zero.</span></span>

 

 



