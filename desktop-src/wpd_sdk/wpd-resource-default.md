---
description: Specifica l'intero file dietro l'oggetto . È anche un modo per fare riferimento a qualsiasi tipo di risorsa, inclusi quelli non coperti da altri tipi di risorse dispositivi portatili Windows, ad esempio un tipo di oggetto personalizzato.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d939cf58033baded231363b39410c2e527fe303075c94255a00ba96831a609b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805881"
---
# <a name="wpd_resource_default"></a>IMPOSTAZIONE PREDEFINITA \_ DELLA RISORSA WPD \_

Specifica l'intero file dietro l'oggetto . È anche un modo per fare riferimento a qualsiasi tipo di risorsa, inclusi quelli non coperti da altri tipi di risorse dispositivi portatili Windows, ad esempio un tipo di oggetto personalizzato.

Verranno incluse tutte le risorse incorporate nella risorsa specificata. Ad esempio, la risorsa predefinita di una cartella radice di contatti può includere tutti i contatti annidati. Tuttavia, tutte le risorse figlio collegate solo *da* metadati o riferimenti non sono incluse. Un esempio è una playlist, che potrebbe collegarsi solo a file audio tramite riferimenti ai metadati o riferimenti di percorso testuali nel file.

L'unico *valore pid consentito* per **PROPERTYKEY** è zero.

Questo tipo di risorsa deve supportare gli attributi seguenti.



| Nome attributo                                                                                                            | Obbligatorio o facoltativo                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [DIMENSIONI TOTALI \_ DELL'ATTRIBUTO DELLA RISORSA \_ \_ \_ WPD](resource-attribute-properties.md)              | Obbligatorio.                                              |
| [L'ATTRIBUTO DELLA RISORSA WPD \_ \_ PUÒ \_ \_ LEGGERE](attributes.md)                                     | Obbligatorio se i client possono leggere questa risorsa.            |
| [L'ATTRIBUTO DELLA RISORSA WPD \_ \_ PUÒ \_ \_ SCRIVERE](attributes.md)                                   | Obbligatorio se i client possono scrivere in questa risorsa.        |
| [L'ATTRIBUTO DELLA RISORSA WPD \_ \_ PUÒ ESSERE \_ \_ ELIMINATO](attributes.md)                                 | Obbligatorio se i client possono eliminare questa risorsa.          |
| [DIMENSIONI OTTIMALI DEL \_ BUFFER DI \_ LETTURA \_ DELL'ATTRIBUTO DELLA \_ RISORSA \_ \_ WPD](attributes.md)   | Obbligatorio se i client hanno accesso in lettura alla risorsa.  |
| [DIMENSIONI OTTIMALI DEL \_ BUFFER DI \_ SCRITTURA \_ DELL'ATTRIBUTO DELLA \_ RISORSA \_ \_ WPD](attributes.md) | Obbligatorio se i client hanno accesso in scrittura alla risorsa. |
| [FORMATO DELL'ATTRIBUTO DELLA RISORSA WPD \_ \_ \_](resource-attribute-properties.md)                       | Obbligatorio.                                              |
| [CHIAVE DI \_ RISORSA \_ DELL'ATTRIBUTO DELLA RISORSA \_ WPD \_](resource-attribute-properties.md)                                              | Consigliato.                                           |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Requisiti per le risorse**](requirements-for-resources.md)
</dt> </dl>

 

 



