---
description: Specifica l'intero file sottostante l'oggetto. È anche un modo per fare riferimento a qualsiasi tipo di risorsa, inclusi quelli non inclusi in altri tipi di risorse dei dispositivi portatili Windows, ad esempio un tipo di oggetto personalizzato.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529892"
---
# <a name="wpd_resource_default"></a>\_impostazione predefinita della risorsa WPD \_

Specifica l'intero file sottostante l'oggetto. È anche un modo per fare riferimento a qualsiasi tipo di risorsa, inclusi quelli non inclusi in altri tipi di risorse dei dispositivi portatili Windows, ad esempio un tipo di oggetto personalizzato.

Verranno incluse tutte le risorse incorporate all'interno della risorsa specificata. Ad esempio, la risorsa predefinita di una cartella radice di contatti può includere tutti i contatti annidati. Tuttavia, le risorse figlio semplicemente *collegate* da metadati o riferimenti non sono incluse. Un esempio è costituito da una playlist, che può essere collegata solo a file audio tramite riferimenti ai metadati o riferimenti al percorso testuale nel file.

L'unico valore *PID* consentito per questo **PropertyKey** è zero.

Questo tipo di risorsa deve supportare gli attributi seguenti.



| Nome attributo                                                                                                            | Obbligatorio o facoltativo                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [\_ \_ dimensioni totali dell'attributo della risorsa WPD \_ \_](resource-attribute-properties.md)              | Obbligatorio.                                              |
| [l'attributo della risorsa WPD è in \_ \_ grado di \_ \_ leggere](attributes.md)                                     | Obbligatorio se i client possono leggere questa risorsa.            |
| [l' \_ attributo della risorsa WPD \_ \_ può \_ scrivere](attributes.md)                                   | Obbligatorio se i client possono scrivere in questa risorsa.        |
| [l' \_ attributo della risorsa WPD \_ può essere \_ \_ eliminato](attributes.md)                                 | Obbligatorio se i client possono eliminare questa risorsa.          |
| [\_dimensione del \_ \_ buffer di \_ lettura ottimale dell' \_ attributo \_ della risorsa WPD](attributes.md)   | Obbligatorio se i client hanno accesso in lettura alla risorsa.  |
| [\_dimensioni del \_ \_ buffer di scrittura ottimali dell'attributo \_ della \_ risorsa WPD \_](attributes.md) | Obbligatorio se i client hanno accesso in scrittura alla risorsa. |
| [\_formato dell' \_ attributo della risorsa WPD \_](resource-attribute-properties.md)                       | Obbligatorio.                                              |
| [\_chiave di \_ risorsa dell'attributo della risorsa WPD \_ \_](resource-attribute-properties.md)                                              | Consigliato.                                           |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Requisiti per le risorse**](requirements-for-resources.md)
</dt> </dl>

 

 



