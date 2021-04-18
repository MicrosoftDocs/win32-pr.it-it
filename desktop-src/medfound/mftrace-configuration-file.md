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
# <a name="mftrace-configuration-file"></a>File di configurazione MFTrace

Lo strumento [MFTrace](mftrace.md) è in grado di leggere un file di configurazione XML che specifica uno o più provider di traccia.

L'elemento [**providers**](providers.md) è l'elemento radice nel file di configurazione.

## <a name="in-this-section"></a>Contenuto della sezione

-   [**parola chiave**](keyword.md)
-   [**mfdetours**](mfdetours.md)
-   [**provider**](provider.md)
-   [**provider**](providers.md)

## <a name="example"></a>Esempio

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

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MFTrace](mftrace.md)
</dt> </dl>

 

 



