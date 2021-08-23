---
title: Debug (Windows Web)
description: Un set di funzioni è disponibile solo nella build DEBUG e è destinato a test e debug.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Debug di servizi Web per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135f81ec45028df098679c91d750915005bfc64b3ff7d072b0494badc98159fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838681"
---
# <a name="debugging-windows-web-services"></a>Debug (Windows Web)

Un set di funzioni è disponibile solo nella build DEBUG e è destinato a test e debug.


Sono disponibili diverse funzioni e variabili di ambiente solo in modalità DEBUG. Possono essere usati per facilitare il test e il debug.

-   Se si imposta WsTimeout=0, tutti i timeout saranno INFINITE. Ciò è utile quando si esegue un'istruzione all'interno del debugger durante operazioni sensibili al tempo.
-   L'impostazione di WsFailCount ha lo stesso effetto della chiamata a WsSetAutoFail.
-   WsFlags consente di impostare vari flag che modificano il comportamento di runtime. La sintassi è WsFlags=a,b,c. I flag supportati sono ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest e ModifySignatureValue.

Con il debug vengono usate le funzioni seguenti:

-   [**WsDumpMemory**](wsdumpmemory.md)
-   [**WsSetAutoFail**](wssetautofail.md)

 

 




