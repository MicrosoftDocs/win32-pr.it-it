---
description: Formati di estensione MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Formati di estensione MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a490c29c98b454b7d563e8af46131b040f123b9de2ef689ea5ede1a2ac100ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193957"
---
# <a name="mtp-extension-formats"></a>Formati di estensione MTP

Il formato di un file in un dispositivo può essere descritto da un valore GUID. Questo valore viene specificato dalla proprietà WPD \_ OBJECT \_ FORMAT.

## <a name="vendor-extended-formats"></a>Formati estesi del fornitore

Quando un produttore di dispositivi supporta un formato esteso del fornitore, il driver combina il codice di formato del fornitore (UINT16) con i 16 bit più alti del GUID NON SPECIFICATO **WPD \_ OBJECT \_ FORMAT. \_**

Ad esempio, se il codice esteso del fornitore è 0xB001, il GUID risultante sarà come illustrato nell'esempio seguente:


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto delle estensioni MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



