---
description: Lo strumento MFTrace è in grado di leggere un file di configurazione XML che specifica uno o più provider di traccia.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: File di configurazione MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6598bcfdde16291fb744783b2f12be414ae997b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310206"
---
# <a name="mftrace-configuration-file"></a><span data-ttu-id="bb5ef-103">File di configurazione MFTrace</span><span class="sxs-lookup"><span data-stu-id="bb5ef-103">MFTrace Configuration File</span></span>

<span data-ttu-id="bb5ef-104">Lo strumento [MFTrace](mftrace.md) è in grado di leggere un file di configurazione XML che specifica uno o più provider di traccia.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-104">The [MFTrace](mftrace.md) tool can read an XML configuration file that specifies one or more trace providers.</span></span>

<span data-ttu-id="bb5ef-105">L'elemento [**providers**](providers.md) è l'elemento radice nel file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="bb5ef-105">The [**providers**](providers.md) element is the root element in the configuration file.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bb5ef-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="bb5ef-106">In this section</span></span>

-   [<span data-ttu-id="bb5ef-107">**parola chiave**</span><span class="sxs-lookup"><span data-stu-id="bb5ef-107">**keyword**</span></span>](keyword.md)
-   [<span data-ttu-id="bb5ef-108">**mfdetours**</span><span class="sxs-lookup"><span data-stu-id="bb5ef-108">**mfdetours**</span></span>](mfdetours.md)
-   [<span data-ttu-id="bb5ef-109">**provider**</span><span class="sxs-lookup"><span data-stu-id="bb5ef-109">**provider**</span></span>](provider.md)
-   [<span data-ttu-id="bb5ef-110">**provider**</span><span class="sxs-lookup"><span data-stu-id="bb5ef-110">**providers**</span></span>](providers.md)

## <a name="example"></a><span data-ttu-id="bb5ef-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="bb5ef-111">Example</span></span>

``` syntax
<?xml version='1.0' encoding='utf-8'?>
<providers>
  <mfdetours level="info"> 
    <keyword ID="MFPlatExport" />
  </mfdetours>
  
  <!-- Manifest-based traces -->

  <provider level="verbose" ID="Microsoft-Windows-MediaFoundation-MFReadWrite">
    <keyword ID="0x0000000000000000" />
  </provider>

</providers>
```

## <a name="related-topics"></a><span data-ttu-id="bb5ef-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bb5ef-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb5ef-113">MFTrace</span><span class="sxs-lookup"><span data-stu-id="bb5ef-113">MFTrace</span></span>](mftrace.md)
</dt> </dl>

 

 



