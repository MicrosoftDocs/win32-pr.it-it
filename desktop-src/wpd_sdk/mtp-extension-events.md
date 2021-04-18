---
description: Eventi di estensione MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: Eventi di estensione MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319085"
---
# <a name="mtp-extension-events"></a>Eventi di estensione MTP

Gli eventi notificano a un'applicazione che si sono verificate modifiche in o con un dispositivo. Ad esempio, un'applicazione può registrarsi per ricevere notifica che un dispositivo è stato rimosso.

## <a name="vendor-extended-event-codes"></a>Fornitori-codici evento esteso

Quando un produttore di dispositivi supporta un evento esteso del fornitore, il driver combina il codice evento (UINT16) del fornitore con i 16 bit più alti del GUID degli **\_ \_ \_ \_ \_ eventi estesi del fornitore dell'evento MTP WPD** .

Se, ad esempio, il codice esteso del fornitore è 0xC001, il GUID risultante sarà come illustrato nell'esempio seguente:


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a>Fornitori-parametri eventi estesi

I parametri per un evento di fornitore esteso vengono segnalati dal **parametro di evento WPD \_ \_ \_ \_ ID** GUID e la **\_ Proprietà WPD \_ MTP \_ ext \_ Event \_ params**, che è una raccolta di **PROPVARIANTS**. Questi **PROPVARIANTS** corrispondono ai parametri dell'evento. Se non sono presenti parametri, questa raccolta è vuota.


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto delle estensioni MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



