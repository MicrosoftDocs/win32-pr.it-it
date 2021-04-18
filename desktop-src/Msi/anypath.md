---
description: Il tipo di dati AnyPath è una stringa di testo contenente un percorso completo o relativo.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311059"
---
# <a name="anypath"></a><span data-ttu-id="34688-103">AnyPath</span><span class="sxs-lookup"><span data-stu-id="34688-103">AnyPath</span></span>

<span data-ttu-id="34688-104">Il tipo di dati AnyPath è una stringa di testo contenente un percorso completo o relativo.</span><span class="sxs-lookup"><span data-stu-id="34688-104">The AnyPath data type is a text string containing either a full path or a relative path.</span></span> <span data-ttu-id="34688-105">Quando si specifica un percorso relativo, è possibile includere un nome di file lungo con il nome di file breve separando i nomi brevi e lunghi con una barra verticale ( \| ).</span><span class="sxs-lookup"><span data-stu-id="34688-105">When specifying a relative path, you can include a long file name with the short file name by separating the short and long names with a vertical bar (\|).</span></span> <span data-ttu-id="34688-106">Si noti che in questo modo non è possibile specificare più livelli di una directory o percorsi completi.</span><span class="sxs-lookup"><span data-stu-id="34688-106">Note that you cannot specify multiple levels of a directory or fully qualified paths in this way.</span></span> <span data-ttu-id="34688-107">Il percorso può contenere proprietà racchiuse tra parentesi quadre ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="34688-107">The path may contain properties enclosed within square brackets (\[ \]).</span></span>

<span data-ttu-id="34688-108">Esempi di dati AnyPath validi:</span><span class="sxs-lookup"><span data-stu-id="34688-108">Examples of valid AnyPath data:</span></span>

-   <span data-ttu-id="34688-109">\\\\\\temporanea condivisione \\ Server</span><span class="sxs-lookup"><span data-stu-id="34688-109">\\\\server\\share\\temp</span></span>
-   <span data-ttu-id="34688-110">c: \\ Temp</span><span class="sxs-lookup"><span data-stu-id="34688-110">c:\\temp</span></span>
-   <span data-ttu-id="34688-111">\\Temp</span><span class="sxs-lookup"><span data-stu-id="34688-111">\\temp</span></span>
-   <span data-ttu-id="34688-112">Stato progetto Project ~ 1 \|</span><span class="sxs-lookup"><span data-stu-id="34688-112">projec~1\|Project Status</span></span>

<span data-ttu-id="34688-113">Esempi di dati AnyPath non validi:</span><span class="sxs-lookup"><span data-stu-id="34688-113">Examples of invalid AnyPath data:</span></span>

-   <span data-ttu-id="34688-114">c: \\ temp \\ Project ~ 1 \| c: \\ stato del \\ progetto Temp One</span><span class="sxs-lookup"><span data-stu-id="34688-114">c:\\temp\\projec~1\|c:\\temp one\\Project Status</span></span>
-   <span data-ttu-id="34688-115">\\\\ \| \\ stato di un \\ progetto Temp Project ~ 1</span><span class="sxs-lookup"><span data-stu-id="34688-115">\\temp\\projec~1\|\\temp one\\Project Status</span></span>

 

 



