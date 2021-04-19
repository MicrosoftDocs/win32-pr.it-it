---
description: È possibile specificare che il driver Ritaglia i frame.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Ritaglio di un frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311631"
---
# <a name="clipping-a-frame"></a><span data-ttu-id="79424-103">Ritaglio di un frame</span><span class="sxs-lookup"><span data-stu-id="79424-103">Clipping a Frame</span></span>

<span data-ttu-id="79424-104">È possibile specificare che il driver Ritaglia i frame.</span><span class="sxs-lookup"><span data-stu-id="79424-104">You can specify that the driver clip the frames.</span></span> <span data-ttu-id="79424-105">Se le altre sezioni del filtro di acquisizione vengono omesse, può trattarsi dell'unica funzione del filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="79424-105">(If the other capture filter sections are omitted, this may be the only function of your capture filter).</span></span> <span data-ttu-id="79424-106">Se il campo **nFrameBytesToCopy** è diverso da zero (0), il relativo valore specifica il numero di byte di ogni frame ricevuti da mantenere.</span><span class="sxs-lookup"><span data-stu-id="79424-106">If the **nFrameBytesToCopy** field is not zero (0), its value specifies how many bytes of each frame received to retain.</span></span> <span data-ttu-id="79424-107">Se il campo è zero, viene mantenuto il frame intero.</span><span class="sxs-lookup"><span data-stu-id="79424-107">If the field is zero, then the whole frame is retained.</span></span>

> [!Note]  
> <span data-ttu-id="79424-108">È possibile ritagliare tutti i frame che passano le altre parti del filtro di acquisizione impostando **nFrameBytesToCopy**.</span><span class="sxs-lookup"><span data-stu-id="79424-108">You may clip any frame that passes the other portions of your capture filter by setting **nFrameBytesToCopy**.</span></span>

 

 

 



