---
title: Opzione /msc_ver
description: L'opzione /msc ver viene usata per consentire a MIDL di generare codice che include ottimizzazioni per versioni diverse dei compilatori \_ Microsoft C/C++.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- Opzione /msc_ver MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f010224e5339ef89e05d1d96630dbedc0cb453eb8dafb4dd5e9c6edb3c24cc00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811371"
---
# <a name="msc_ver-switch"></a>/msc \_ ver - opzione

**L'opzione /msc \_ ver** viene usata per consentire a MIDL di generare codice che include ottimizzazioni per versioni diverse dei compilatori Microsoft C/C++.

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a>Opzioni switch

<dl> <dt>

*numero di \_ versione* 
</dt> <dd>

Specifica un numero di versione intero del Microsoft Visual C++ che verrà usato per compilare gli stub client e server dell'applicazione distribuita. Il numero di versione predefinito è 1100, che corrisponde Visual C++ versione 5.0. Il numero di versione 1200 corrisponde Visual C++ versione 6.0 e così via.

</dd> </dl>

## <a name="remarks"></a>Commenti

In particolare, i valori di versione 1100 o superiori causano la generazione di codice da parte del compilatore MIDL utilizzando la direttiva **\_ \_ declspec(uuid()).** Attiva anche le macro che usano le direttive **\_ \_ declspec(selectany)** e **\_ \_ declspec(novtable).**

 

 




