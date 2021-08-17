---
description: Proprietà dell'estensione MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Proprietà dell'estensione MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0468d249b469c4e768962ab6a920935e7a64b51d8e035af111e8274f7f0b9af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193947"
---
# <a name="mtp-extension-properties"></a>Proprietà dell'estensione MTP

Le proprietà descrivono oggetti, proprietà, risorse e dispositivi.

## <a name="vendor-extended-object-properties"></a>Proprietà degli oggetti estesi dal fornitore

Quando un produttore di dispositivi crea una proprietà estesa del fornitore per un oggetto dispositivo, combina il GUID **WPD \_ PROPERTIES \_ MTP \_ VENDOR EXTENDED \_ \_ OBJECT \_ PROPS** con il codice della proprietà dell'oggetto per costruire una **struttura PROPERTYKEY.**

Ad esempio, se il codice della proprietà dell'oggetto è 0xD801, l'oggetto **PROPERTYKEY** risultante sarà come illustrato nell'esempio seguente:


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a>Proprietà del dispositivo estese al fornitore

Quando un produttore di dispositivi crea una proprietà estesa del fornitore per un dispositivo, combina il GUID DELLE PROPRIETÀ **\_ \_ MTP \_ DEL \_ \_ \_** DISPOSITIVO ESTESO DEL FORNITORE WPD con il codice della proprietà dell'oggetto per costruire una **struttura PROPERTYKEY.**

Ad esempio, se il codice della proprietà dell'oggetto è 0xD001, l'oggetto **PROPERTYKEY** risultante sarà come illustrato nell'esempio seguente:


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto delle estensioni MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



