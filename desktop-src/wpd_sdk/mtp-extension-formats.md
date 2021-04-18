---
description: Formati di estensione MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Formati di estensione MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313900"
---
# <a name="mtp-extension-formats"></a>Formati di estensione MTP

Il formato di un file in un dispositivo può essere descritto da un valore GUID. Questo valore viene specificato dalla proprietà del \_ formato dell'oggetto WPD \_ .

## <a name="vendor-extended-formats"></a>Formati estesi fornitore

Quando un produttore di dispositivi supporta un formato esteso dal fornitore, il driver combina il codice del formato del fornitore (UINT16) con i 16 bit più alti del GUID del **formato dell'oggetto WPD non \_ \_ \_ specificato** .

Se, ad esempio, il codice esteso del fornitore è 0xB001, il GUID risultante sarà come illustrato nell'esempio seguente:


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto delle estensioni MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



