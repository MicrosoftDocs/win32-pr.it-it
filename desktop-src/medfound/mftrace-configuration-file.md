---
description: Lo strumento MFTrace può leggere un file di configurazione XML che specifica uno o più provider di traccia.
ms.assetid: 70d11a55-041e-4eb5-96a9-238e7ecdd906
title: File di configurazione di MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60969d52405b5aeeb768710d35751d9ea2cab40ca60a7d85a4da1bc1b0c65468
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117871938"
---
# <a name="mftrace-configuration-file"></a>File di configurazione di MFTrace

Lo [strumento MFTrace](mftrace.md) può leggere un file di configurazione XML che specifica uno o più provider di traccia.

[**L'elemento providers**](providers.md) è l'elemento radice nel file di configurazione.

## <a name="in-this-section"></a>Contenuto della sezione

-   [**Parola chiave**](keyword.md)
-   [**mfdetours**](mfdetours.md)
-   [**Provider**](provider.md)
-   [**Provider**](providers.md)

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

 

 



