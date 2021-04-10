---
description: Il flusso di informazioni di riepilogo contiene informazioni sul pacchetto che possono essere visualizzate tramite Esplora risorse di Microsoft Windows.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Informazioni sul flusso di informazioni di riepilogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131510"
---
# <a name="about-the-summary-information-stream"></a><span data-ttu-id="c9928-103">Informazioni sul flusso di informazioni di riepilogo</span><span class="sxs-lookup"><span data-stu-id="c9928-103">About the Summary Information Stream</span></span>

<span data-ttu-id="c9928-104">Il flusso di informazioni di riepilogo contiene informazioni sul pacchetto che possono essere visualizzate tramite Esplora risorse di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c9928-104">The summary information stream contains information about the package that can be viewed through Microsoft Windows Explorer.</span></span> <span data-ttu-id="c9928-105">Queste informazioni sono accessibili tramite l'interfaccia **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c9928-105">This information is accessible through the **IStream** interface.</span></span> <span data-ttu-id="c9928-106">Spetta all'autore specificare i valori per ognuna di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c9928-106">It is up to the author to provide the values for each of these properties.</span></span>

<span data-ttu-id="c9928-107">Il flusso di informazioni di riepilogo USA COM per fornire l'archiviazione strutturata dei database.</span><span class="sxs-lookup"><span data-stu-id="c9928-107">The summary information stream uses COM to provide structured storage of databases.</span></span> <span data-ttu-id="c9928-108">COM supporta il concetto di archiviazione strutturata accessibile tramite l'interfaccia **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c9928-108">COM supports the concept of structured storage accessible through the **IStream** interface.</span></span> <span data-ttu-id="c9928-109">L'archiviazione strutturata, a sua volta, supporta il concetto di set di proprietà come metodo flessibile per la serializzazione di quasi tutte le informazioni.</span><span class="sxs-lookup"><span data-stu-id="c9928-109">Structured storage, in turn, supports the concept of property sets as a flexible method for serializing almost any information.</span></span> <span data-ttu-id="c9928-110">La specifica COM definisce un singolo set di proprietà standard, informazioni di riepilogo, utilizzato per popolare le finestre delle proprietà visualizzabili da Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="c9928-110">The COM specification defines a single standard property set, summary information, which is used to populate property sheets viewable from Windows Explorer.</span></span> <span data-ttu-id="c9928-111">Quindi, le informazioni archiviate nel flusso di informazioni di riepilogo possono essere visualizzate dagli utenti facendo clic con il pulsante destro del mouse su un database del programma di installazione o una trasformazione e selezionando [Proprietà](about-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c9928-111">So, information stored in the summary information stream can be viewed by users when they right-click an installer database or transform and select [Properties](about-properties.md).</span></span>

<span data-ttu-id="c9928-112">Per un elenco del set di proprietà di riepilogo, vedere [set di proprietà del flusso di informazioni di riepilogo](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="c9928-112">For a list of the summary property set see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="c9928-113">Per brevi descrizioni delle proprietà delle informazioni di riepilogo usate con i database, le trasformazioni e le patch, vedere [descrizioni delle proprietà di riepilogo](summary-property-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="c9928-113">For brief descriptions of the Summary Information properties used with databases, transforms, and patches, see [Summary Property Descriptions](summary-property-descriptions.md).</span></span>

 

 



