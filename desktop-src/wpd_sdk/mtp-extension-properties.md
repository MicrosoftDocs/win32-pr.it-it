---
description: Proprietà estensione MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Proprietà estensione MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313899"
---
# <a name="mtp-extension-properties"></a>Proprietà estensione MTP

Le proprietà descrivono oggetti, proprietà, risorse e dispositivi.

## <a name="vendor-extended-object-properties"></a>Proprietà degli oggetti estesi del fornitore

Quando un produttore di dispositivi crea una proprietà estesa dal fornitore per un oggetto dispositivo, combina le **\_ Proprietà WPD proprietà \_ MTP \_ fornitore \_ esteso \_ oggetto \_ Props** GUID con il codice di proprietà dell'oggetto per costruire una struttura **PropertyKey** .

Se, ad esempio, il codice della proprietà dell'oggetto è 0xD801, il **PropertyKey** risultante sarà come illustrato nell'esempio seguente:


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a>Proprietà del dispositivo esteso del fornitore

Quando un produttore di dispositivi crea una proprietà estesa dal fornitore per un dispositivo, combina le **\_ Proprietà WPD \_ MTP \_ Vendor \_ Extended \_ Device \_ Props** GUID con il codice di proprietà dell'oggetto per costruire una struttura **PropertyKey** .

Se, ad esempio, il codice della proprietà dell'oggetto è 0xD001, il **PropertyKey** risultante sarà come illustrato nell'esempio seguente:


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto delle estensioni MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



