---
description: ICE39 convalida il flusso di informazioni di riepilogo del database.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314217"
---
# <a name="ice39"></a><span data-ttu-id="13bc9-103">ICE39</span><span class="sxs-lookup"><span data-stu-id="13bc9-103">ICE39</span></span>

<span data-ttu-id="13bc9-104">ICE39 convalida il [flusso di informazioni di riepilogo](summary-information-stream.md) del database.</span><span class="sxs-lookup"><span data-stu-id="13bc9-104">ICE39 validates the [Summary Information Stream](summary-information-stream.md) of the database.</span></span>

<span data-ttu-id="13bc9-105">ICE39 controlla il formato delle proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="13bc9-105">ICE39 checks the format of the following properties:</span></span>

-   [<span data-ttu-id="13bc9-106">**Riepilogo Conteggio parole**</span><span class="sxs-lookup"><span data-stu-id="13bc9-106">**Word Count Summary**</span></span>](word-count-summary.md)
-   [<span data-ttu-id="13bc9-107">**Riepilogo conteggio pagine**</span><span class="sxs-lookup"><span data-stu-id="13bc9-107">**Page Count Summary**</span></span>](page-count-summary.md)
-   [<span data-ttu-id="13bc9-108">**Riepilogo modelli**</span><span class="sxs-lookup"><span data-stu-id="13bc9-108">**Template Summary**</span></span>](template-summary.md)
-   [<span data-ttu-id="13bc9-109">**Riepilogo numero revisione**</span><span class="sxs-lookup"><span data-stu-id="13bc9-109">**Revision Number Summary**</span></span>](revision-number-summary.md)
-   [<span data-ttu-id="13bc9-110">**Crea riepilogo Data/ora**</span><span class="sxs-lookup"><span data-stu-id="13bc9-110">**Create Time/Date Summary**</span></span>](create-time-date-summary.md)
-   [<span data-ttu-id="13bc9-111">**Ultimo riepilogo Data/ora di salvataggio**</span><span class="sxs-lookup"><span data-stu-id="13bc9-111">**Last Saved Time/Date Summary**</span></span>](last-saved-time-date-summary.md)
-   [<span data-ttu-id="13bc9-112">**Ultimo riepilogo stampato**</span><span class="sxs-lookup"><span data-stu-id="13bc9-112">**Last Printed Summary**</span></span>](last-printed-summary.md)

<span data-ttu-id="13bc9-113">Se la proprietà di [**Riepilogo di Word Count**](word-count-summary.md) specifica che l'origine è compressa, ICE39 pubblica un avviso se eventuali file sono contrassegnati come compressi nella colonna attributi della [tabella file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="13bc9-113">If the [**Word Count Summary**](word-count-summary.md) Property specifies that the source is compressed, ICE39 posts a warning if any files are also marked as compressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="13bc9-114">Vedere [uso di cabinet e origini compresse](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="13bc9-114">See [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="13bc9-115">ICE39 pubblica un avviso se la proprietà di [**Riepilogo di Word Count**](word-count-summary.md) specifica che il pacchetto è conforme a UAC e la [tabella MsiPackageCertificate](msipackagecertificate-table.md) non è vuota.</span><span class="sxs-lookup"><span data-stu-id="13bc9-115">ICE39 posts a warning if the [**Word Count Summary**](word-count-summary.md) Property specifies that the package is UAC compliant and the [MsiPackageCertificate Table](msipackagecertificate-table.md) is not empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13bc9-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13bc9-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13bc9-117">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="13bc9-117">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



