---
description: Classificazioni bitmap
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Classificazioni bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226714"
---
# <a name="bitmap-classifications"></a><span data-ttu-id="8d23b-103">Classificazioni bitmap</span><span class="sxs-lookup"><span data-stu-id="8d23b-103">Bitmap Classifications</span></span>

<span data-ttu-id="8d23b-104">Esistono due classi di bitmap:</span><span class="sxs-lookup"><span data-stu-id="8d23b-104">There are two classes of bitmaps:</span></span>

-   <span data-ttu-id="8d23b-105">[Bitmap indipendenti dal dispositivo](device-independent-bitmaps.md) (DIB).</span><span class="sxs-lookup"><span data-stu-id="8d23b-105">[Device-independent bitmaps](device-independent-bitmaps.md) (DIB).</span></span> <span data-ttu-id="8d23b-106">Il formato del file DIB è stato progettato per garantire che le immagini bitmap create usando un'applicazione possano essere caricate e visualizzate in un'altra applicazione, mantenendo lo stesso aspetto dell'originale.</span><span class="sxs-lookup"><span data-stu-id="8d23b-106">The DIB file format was designed to ensure that bitmapped graphics created using one application can be loaded and displayed in another application, retaining the same appearance as the original.</span></span>

-   <span data-ttu-id="8d23b-107">Le [bitmap dipendenti dal dispositivo](device-dependent-bitmaps.md) (DDB), note anche come bitmap GDI, erano le uniche bitmap disponibili nelle prime versioni di Microsoft Windows a 16 bit (prima della versione 3,0).</span><span class="sxs-lookup"><span data-stu-id="8d23b-107">[Device-dependent bitmaps](device-dependent-bitmaps.md) (DDB), also known as GDI bitmaps, were the only bitmaps available in early versions of 16-bit Microsoft Windows (prior to version 3.0).</span></span> <span data-ttu-id="8d23b-108">Tuttavia, con il miglioramento della tecnologia di visualizzazione e con l'aumentare della varietà di dispositivi di visualizzazione disponibili, si verificano alcuni problemi intrinseci che possono essere risolti solo con la funzionalità DIB.</span><span class="sxs-lookup"><span data-stu-id="8d23b-108">However, as display technology improved and as the variety of available display devices increased, certain inherent problems surfaced which could only be solved using DIBs.</span></span> <span data-ttu-id="8d23b-109">Ad esempio, non esisteva alcun metodo di archiviazione (o recupero) della risoluzione del tipo di visualizzazione in cui è stata creata una bitmap, pertanto un'applicazione di disegno non è stata in grado di determinare rapidamente se una bitmap fosse adatta per il tipo di dispositivo di visualizzazione video in cui l'applicazione era in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8d23b-109">For example, there was no method of storing (or retrieving) the resolution of the display type on which a bitmap was created, so a drawing application could not quickly determine whether a bitmap was suitable for the type of video display device on which the application was running.</span></span>

    <span data-ttu-id="8d23b-110">Nonostante questi problemi, DDB (noti anche come bitmap compatibili) sono ancora utili per migliorare le prestazioni GDI e per altre situazioni.</span><span class="sxs-lookup"><span data-stu-id="8d23b-110">Despite these problems, DDBs (also known as compatible bitmaps) are still useful for better GDI performance and for other situations.</span></span>

 

 



