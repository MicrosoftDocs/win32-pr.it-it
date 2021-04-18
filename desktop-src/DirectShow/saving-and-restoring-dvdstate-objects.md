---
description: Salvataggio e ripristino di oggetti DvdState
ms.assetid: 65180fe2-0faf-47c0-bccd-728e01056c46
title: Salvataggio e ripristino di oggetti DvdState
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9640b20bc8d763054c15331017da343ef45f3c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303909"
---
# <a name="saving-and-restoring-dvdstate-objects"></a><span data-ttu-id="5b892-103">Salvataggio e ripristino di oggetti DvdState</span><span class="sxs-lookup"><span data-stu-id="5b892-103">Saving and Restoring DvdState Objects</span></span>

<span data-ttu-id="5b892-104">Gli oggetti [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) consentono alle applicazioni di salvare uno snapshot della sessione utente, incluse informazioni quali il percorso corrente sul disco, il livello padre della persona che sta visualizzando, i flussi audio e di sottoimmagine selezionati e così via.</span><span class="sxs-lookup"><span data-stu-id="5b892-104">[**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) objects enable applications to save a snapshot of the user session, including information such as the current location on the disc, the parental level of the person who is viewing, the selected audio and subpicture streams, and so on.</span></span> <span data-ttu-id="5b892-105">Questo significa che gli utenti possono salvare il proprio posto su un disco DVD-Video e guardarlo in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="5b892-105">This means that users can save their place on a DVD-Video disc and watch it at a later time.</span></span>

<span data-ttu-id="5b892-106">Le applicazioni non possono creare oggetti DvdState.</span><span class="sxs-lookup"><span data-stu-id="5b892-106">Applications cannot create DvdState objects.</span></span> <span data-ttu-id="5b892-107">Questi oggetti vengono creati internamente dal navigatore DVD quando un'applicazione chiama [**IDvdInfo2:: GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span><span class="sxs-lookup"><span data-stu-id="5b892-107">These objects are created internally by the DVD Navigator when an application calls [**IDvdInfo2::GetState**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getstate).</span></span> <span data-ttu-id="5b892-108">Gli oggetti DvdState espongono l'interfaccia [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) per consentire alle applicazioni di eseguire query per determinate informazioni.</span><span class="sxs-lookup"><span data-stu-id="5b892-108">DvdState objects expose the [**IDvdState**](/windows/desktop/api/Strmif/nn-strmif-idvdstate) interface to allow applications to query for certain information.</span></span>

<span data-ttu-id="5b892-109">Nell'applicazione di esempio DVD le funzioni **CDvdCore:: RestoreBookmark** e **CDvdCore:: SaveBookmark** mostrano come salvare e recuperare gli oggetti DvdState.</span><span class="sxs-lookup"><span data-stu-id="5b892-109">In the DVD sample application, the **CDvdCore::RestoreBookmark** and **CDvdCore::SaveBookmark** functions show how to save and retrieve DvdState objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b892-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b892-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b892-111">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="5b892-111">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



