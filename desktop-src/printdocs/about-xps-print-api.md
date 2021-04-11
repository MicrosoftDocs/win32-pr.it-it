---
description: XPS&\# 160; Stampa&\# 160; API fornisce un'interfaccia allo spooler di stampa che le applicazioni possono utilizzare per stampare processi che inviano documenti XPS a una stampante.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: Informazioni sull'API di stampa XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1467458a737a6faaddb5ed45c81623207ccdb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131603"
---
# <a name="about-the-xps-print-api"></a><span data-ttu-id="2195c-103">Informazioni sull'API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="2195c-103">About the XPS Print API</span></span>

<span data-ttu-id="2195c-104">L' [API di stampa XPS](xps-printing.md) fornisce un'interfaccia allo spooler di stampa che le applicazioni possono utilizzare per stampare processi che inviano documenti XPS a una stampante.</span><span class="sxs-lookup"><span data-stu-id="2195c-104">The [XPS Print API](xps-printing.md) provides an interface to the print spooler that applications can use to print jobs that send XPS documents to a printer.</span></span>

<span data-ttu-id="2195c-105">Se la stampante di destinazione utilizza un driver della stampante XPSDrv, l'API di stampa XPS consente al driver della stampante XPSDrv di ricevere eventi di documento durante l'elaborazione di un processo di stampa da parte dello spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="2195c-105">If the destination printer uses an XPSDrv printer driver, the XPS Print API makes it possible for the XPSDrv printer driver to receive document events as the print spooler processes a print job.</span></span> <span data-ttu-id="2195c-106">Per una descrizione degli eventi di documento inviati al driver della stampante XPSDrv, vedere [eventi del documento del driver XPS](/windows-hardware/drivers/print/xps-driver-document-events).</span><span class="sxs-lookup"><span data-stu-id="2195c-106">For a description of the document events that are sent to the XPSDrv printer driver see [XPS Driver Document Events](/windows-hardware/drivers/print/xps-driver-document-events).</span></span>

<span data-ttu-id="2195c-107">Se la stampante di destinazione utilizza un driver della stampante GDI, l' [API di stampa XPS](xps-printing.md) consente al sistema di gestire la necessaria conversione dei dati del processo di stampa dal formato XPS al formato Enhanced Metafile (EMF) utilizzato dal driver della stampante GDI.</span><span class="sxs-lookup"><span data-stu-id="2195c-107">If the destination printer uses a GDI printer driver, the [XPS Print API](xps-printing.md) lets the system handle the necessary conversion of the print job data from XPS format to the Enhanced Metafile (EMF) format that the GDI printer driver uses.</span></span> <span data-ttu-id="2195c-108">Per una descrizione degli eventi del documento del driver della stampante GDI, vedere [funzione DocumentEvent](documentevent.md).</span><span class="sxs-lookup"><span data-stu-id="2195c-108">For a description of the GDI printer driver document events see [DocumentEvent Function](documentevent.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2195c-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2195c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2195c-110">Uso dell'API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="2195c-110">Using the XPS Print API</span></span>](using-the-xps-print-api.md)
</dt> <dt>

[<span data-ttu-id="2195c-111">Informazioni di riferimento sulle API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="2195c-111">XPS Print API Reference</span></span>](xpsprint-api.md)
</dt> </dl>

 

 
