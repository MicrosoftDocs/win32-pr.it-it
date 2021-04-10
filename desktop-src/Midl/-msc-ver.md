---
title: /msc_ver opzione
description: L' \_ opzione/MSC ver viene utilizzata per consentire a MIDL di generare codice che include ottimizzazioni per versioni diverse dei compilatori Microsoft C/C++.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver switch MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857545"
---
# <a name="msc_ver-switch"></a>\_opzione ver/MSC

L'opzione **/MSC \_ ver** viene utilizzata per consentire a MIDL di generare codice che include ottimizzazioni per versioni diverse dei compilatori Microsoft C/C++.

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*numero di versione \_* 
</dt> <dd>

Specifica un numero di versione Integer del compilatore Microsoft Visual C++ che verrà usato per compilare gli stub client e server dell'applicazione distribuita. Il numero di versione predefinito è 1100, che corrisponde a Visual C++ versione 5,0. Il numero di versione 1200 corrisponde a Visual C++ versione 6,0 e così via.

</dd> </dl>

## <a name="remarks"></a>Commenti

In particolare, i valori di versione 1100 o superiore fanno sì che il compilatore MIDL generi codice usando la direttiva **\_ \_ declspec (UUID)** . Attiva inoltre le macro che usano le direttive **\_ \_ declspec (selectany)** e **\_ \_ declspec (novtable)** .

 

 




