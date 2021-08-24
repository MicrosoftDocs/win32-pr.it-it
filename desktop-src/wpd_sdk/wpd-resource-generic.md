---
description: Specifica un tipo di risorsa non definito diversamente da Windows dispositivi portatili.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c418299474373d8b960d15c429ea98d887cc404be49c8d38c7d2bb83611c4ca1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805871"
---
# <a name="wpd_resource_generic"></a>RISORSA WPD \_ \_ GENERICA

Specifica un tipo di risorsa non definito diversamente da Windows dispositivi portatili. È possibile definire risorse personalizzate che supportano qualsiasi attributo personalizzato o Windows attributi definiti da Dispositivi portatili. Tuttavia, qualsiasi risorsa creata deve supportare gli attributi seguenti.



| Nome attributo                                                                                                            | Obbligatorio o facoltativo                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [DIMENSIONI TOTALI \_ DELL'ATTRIBUTO DELLA RISORSA \_ \_ \_ WPD](resource-attribute-properties.md)              | Obbligatorio.                                              |
| [ATTRIBUTO RISORSA WPD \_ \_ \_ \_ LEGGIBILE](attributes.md)                                     | Obbligatorio se i client possono leggere questa risorsa.            |
| [L'ATTRIBUTO \_ DELLA RISORSA WPD PUÒ \_ \_ \_ SCRIVERE](attributes.md)                                   | Obbligatorio se i client possono scrivere in questa risorsa.        |
| [L'ATTRIBUTO \_ DELLA RISORSA WPD PUÒ ESSERE \_ \_ \_ ELIMINATO](attributes.md)                                 | Obbligatorio se i client possono eliminare questa risorsa.          |
| [DIMENSIONI OTTIMALI DEL \_ BUFFER DI \_ LETTURA \_ DELL'ATTRIBUTO DELLA \_ \_ RISORSA \_ WPD](attributes.md)   | Obbligatorio se i client hanno accesso in lettura alla risorsa.  |
| [DIMENSIONI OTTIMALI DEL \_ BUFFER DI \_ SCRITTURA \_ DELL'ATTRIBUTO \_ \_ RISORSA \_ WPD](attributes.md) | Obbligatorio se i client hanno accesso in scrittura alla risorsa. |
| [FORMATO DELL'ATTRIBUTO DELLA RISORSA WPD \_ \_ \_](resource-attribute-properties.md)                       | Obbligatorio.                                              |
| [CHIAVE DI RISORSA \_ \_ DELL'ATTRIBUTO \_ DELLA RISORSA \_ WPD](resource-attribute-properties.md)                                              | Consigliato.                                           |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Requisiti per le risorse**](requirements-for-resources.md)
</dt> </dl>

 

 



