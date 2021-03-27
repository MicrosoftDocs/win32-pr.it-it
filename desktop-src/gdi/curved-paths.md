---
description: Percorsi curvi
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Percorsi curvi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880318"
---
# <a name="curved-paths"></a><span data-ttu-id="854a1-103">Percorsi curvi</span><span class="sxs-lookup"><span data-stu-id="854a1-103">Curved Paths</span></span>

<span data-ttu-id="854a1-104">Un'applicazione può appiattire le curve in un percorso chiamando la funzione [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) .</span><span class="sxs-lookup"><span data-stu-id="854a1-104">An application can flatten the curves in a path by calling the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function.</span></span> <span data-ttu-id="854a1-105">Questa funzione è particolarmente utile per le applicazioni che soddisfano il testo nel contorno di un tracciato che contiene curve.</span><span class="sxs-lookup"><span data-stu-id="854a1-105">This function is especially useful for applications that fit text onto the contour of a path which contains curves.</span></span> <span data-ttu-id="854a1-106">Per adattarsi al testo, l'applicazione deve eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="854a1-106">To fit the text, the application must perform the following steps:</span></span>

1.  <span data-ttu-id="854a1-107">Creare il percorso in cui viene visualizzato il testo.</span><span class="sxs-lookup"><span data-stu-id="854a1-107">Create the path where the text appears.</span></span>
2.  <span data-ttu-id="854a1-108">Chiamare la funzione [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) per convertire le curve in un percorso in segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="854a1-108">Call the [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) function to convert the curves in a path into line segments.</span></span>
3.  <span data-ttu-id="854a1-109">Chiamare la funzione [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) per recuperare i segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="854a1-109">Call the [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) function to retrieve those line segments.</span></span>
4.  <span data-ttu-id="854a1-110">Calcolare la lunghezza di ogni riga e la larghezza di ogni carattere nella stringa.</span><span class="sxs-lookup"><span data-stu-id="854a1-110">Calculate the length of each line and the width of each character in the string.</span></span>
5.  <span data-ttu-id="854a1-111">Usare i dati di larghezza riga e carattere per posizionare ogni carattere lungo la curva.</span><span class="sxs-lookup"><span data-stu-id="854a1-111">Use line-width and character-width data to position each character along the curve.</span></span>

 

 



