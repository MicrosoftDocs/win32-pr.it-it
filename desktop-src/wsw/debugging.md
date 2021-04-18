---
title: Debug (servizi Web Windows)
description: Un set di funzioni è disponibile solo nella build di DEBUG e è destinato a test e debug.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Debug di servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300812"
---
# <a name="debugging-windows-web-services"></a>Debug (servizi Web Windows)

Un set di funzioni è disponibile solo nella build di DEBUG e è destinato a test e debug.


Sono disponibili diverse funzioni e variabili di ambiente solo in modalità di DEBUG. Possono essere usati per semplificare il test e il debug.

-   Se si imposta WsTimeout = 0, tutti i timeout saranno infiniti. Questa operazione è utile quando si esegue il debug del debugger durante le operazioni sensibili al tempo.
-   L'impostazione di WsFailCount ha lo stesso effetto della chiamata di WsSetAutoFail.
-   WsFlags consente di impostare diversi flag che modificano il comportamento in fase di esecuzione. La sintassi è WsFlags = a, b, c. I flag supportati sono ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest e ModifySignatureValue.

Con il debug vengono usate le funzioni seguenti:

-   [**WsDumpMemory**](wsdumpmemory.md)
-   [**WsSetAutoFail**](wssetautofail.md)

 

 




