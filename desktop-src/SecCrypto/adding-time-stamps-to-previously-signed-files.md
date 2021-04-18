---
description: I timestamp vengono in genere inclusi quando un file viene firmato usando SignTool con l'opzione-t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Aggiunta di timestamp ai file firmati in precedenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322039"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a><span data-ttu-id="819e6-103">Aggiunta di timestamp ai file firmati in precedenza</span><span class="sxs-lookup"><span data-stu-id="819e6-103">Adding Time Stamps to Previously Signed Files</span></span>

<span data-ttu-id="819e6-104">I timestamp vengono in genere inclusi quando un file viene firmato usando SignTool con l'opzione **-t** .</span><span class="sxs-lookup"><span data-stu-id="819e6-104">Time stamps are normally included when a file is signed using SignTool with the **-t** option.</span></span> <span data-ttu-id="819e6-105">Inoltre, è possibile aggiungere timestamp ai file firmati senza un timestamp.</span><span class="sxs-lookup"><span data-stu-id="819e6-105">In addition, time stamps can be added to files that were signed without a time stamp.</span></span> <span data-ttu-id="819e6-106">Il seguente comando aggiunge un timestamp a un file firmato in precedenza:</span><span class="sxs-lookup"><span data-stu-id="819e6-106">The following command adds a time stamp to a previously signed file:</span></span>

<span data-ttu-id="819e6-107">**timestamp di SignTool-t https: \/ /timestamp.digicert.com *MyControl.exe***</span><span class="sxs-lookup"><span data-stu-id="819e6-107">**signtool timestamp -t https:\//timestamp.digicert.com *MyControl.exe***</span></span>

> [!Note]  
> <span data-ttu-id="819e6-108">Il file per il quale è stato contrassegnato il timestamp deve essere stato precedentemente firmato.</span><span class="sxs-lookup"><span data-stu-id="819e6-108">The file to be time stamped must have previously been signed.</span></span>

 

<span data-ttu-id="819e6-109">Per ulteriori informazioni su SignTool, vedere [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="819e6-109">For more information about SignTool, see [SignTool](signtool.md).</span></span>

 

 



