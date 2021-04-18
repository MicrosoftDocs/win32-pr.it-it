---
description: Managed Object Format (MOF) è il linguaggio utilizzato per descrivere le classi Common Information Model (CIM).
ms.assetid: 26494142-2078-4d46-a794-e43973255c2d
ms.tgt_platform: multiple
title: MOF (Managed Object Format)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16f95c6868943a2f41c4326c341207ff26a03af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316564"
---
# <a name="managed-object-format-mof"></a><span data-ttu-id="159fc-103">MOF (Managed Object Format)</span><span class="sxs-lookup"><span data-stu-id="159fc-103">Managed Object Format (MOF)</span></span>

<span data-ttu-id="159fc-104">Managed Object Format (MOF) è il linguaggio utilizzato per descrivere le classi [*Common Information Model (CIM)*](gloss-c.md) .</span><span class="sxs-lookup"><span data-stu-id="159fc-104">Managed Object Format (MOF) is the language used to describe [*Common Information Model (CIM)*](gloss-c.md) classes.</span></span>

<span data-ttu-id="159fc-105">Il modo consigliato per i provider WMI di implementare nuove classi WMI è nei file MOF compilati utilizzando [**Mofcomp.exe**](mofcomp.md) nel [*repository WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="159fc-105">The recommended way for WMI providers to implement new WMI classes is in MOF files which are compiled using [**Mofcomp.exe**](mofcomp.md) into the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="159fc-106">È anche possibile creare e modificare le classi e le istanze CIM usando l' [API com per WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="159fc-106">It is also possible to create and manipulate CIM classes and instances using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="159fc-107">Un provider WMI è in genere costituito da un file MOF, che definisce i dati e le classi di evento per i quali il provider restituisce i dati e un file DLL contenente il codice che fornisce i dati.</span><span class="sxs-lookup"><span data-stu-id="159fc-107">A WMI provider normally consists of a MOF file, which defines the data and event classes for which the provider returns data, and a DLL file which contains the code that supplies data.</span></span> <span data-ttu-id="159fc-108">Per ulteriori informazioni, vedere la pagina relativa [alla fornitura di dati a WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="159fc-108">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="159fc-109">Le applicazioni e gli script client WMI possono eseguire una query per le istanze delle classi MOF del provider o sottoscrivere la ricezione di notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="159fc-109">WMI client scripts and applications can query for instances of provider MOF classes or subscribe to receive event notifications.</span></span>

<span data-ttu-id="159fc-110">Con MOF è possibile eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="159fc-110">You can perform the following tasks with MOF:</span></span>

-   [<span data-ttu-id="159fc-111">Compilazione di file MOF</span><span class="sxs-lookup"><span data-stu-id="159fc-111">Compiling MOF Files</span></span>](compiling-mof-files.md)
-   [<span data-ttu-id="159fc-112">Creazione di una classe</span><span class="sxs-lookup"><span data-stu-id="159fc-112">Creating a Class</span></span>](creating-a-class.md)
-   [<span data-ttu-id="159fc-113">Creazione di un'istanza</span><span class="sxs-lookup"><span data-stu-id="159fc-113">Creating an Instance</span></span>](creating-an-instance.md)
-   [<span data-ttu-id="159fc-114">Creazione di un metodo</span><span class="sxs-lookup"><span data-stu-id="159fc-114">Creating a Method</span></span>](creating-a-method.md)
-   [<span data-ttu-id="159fc-115">Aggiunta di un qualificatore</span><span class="sxs-lookup"><span data-stu-id="159fc-115">Adding a Qualifier</span></span>](adding-a-qualifier.md)
-   [<span data-ttu-id="159fc-116">Creazione di un commento</span><span class="sxs-lookup"><span data-stu-id="159fc-116">Creating a Comment</span></span>](creating-a-comment.md)

## <a name="related-topics"></a><span data-ttu-id="159fc-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="159fc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="159fc-118">Informazioni su WMI</span><span class="sxs-lookup"><span data-stu-id="159fc-118">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 



