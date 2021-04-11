---
description: Specifica un tipo di risorsa non definito diversamente dai dispositivi portatili Windows.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128947"
---
# <a name="wpd_resource_generic"></a>\_risorsa WPD \_ generica

Specifica un tipo di risorsa non definito diversamente dai dispositivi portatili Windows. È possibile definire risorse personalizzate che supportano qualsiasi attributo definito da dispositivi portatili o di Windows. Tutte le risorse create devono tuttavia supportare i seguenti attributi.



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

 

 



