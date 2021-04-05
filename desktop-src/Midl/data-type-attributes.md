---
title: Attributi del tipo di dati
description: È possibile applicare questi attributi ai tipi di dati in un'istruzione typedef per definire ulteriormente l'utilizzo o l'effetto del tipo di dati.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- MIDL di IDL, attributi, tipo di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714368"
---
# <a name="data-type-attributes"></a>Attributi del tipo di dati

È possibile applicare questi attributi ai tipi di dati in un'istruzione [**typedef**](typedef.md) per definire ulteriormente l'utilizzo o l'effetto del tipo di dati.



| Attributo                                 | Utilizzo                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**handle di contesto \_**](context-handle.md) | Identifica un handle di associazione che mantiene le informazioni sullo stato (contesto) su un particolare server tra le chiamate di procedure remote da un particolare client. Non valido per le funzioni dell'interfaccia dell' [**oggetto**](object.md) .                                                                                                         |
| [**gestire**](handle.md)                  | Specifica un tipo di handle personalizzato specifico per l'applicazione.                                                                                                                                                                                                                                                                |
| [**MS \_ Union**](-ms-union.md)            | Controlla l'allineamento del rapporto di recapito delle unioni non incapsulate. Usare su [**typedef**](typedef.md)per la compatibilità con le interfacce compilate con MIDL 1,0 o 2,0.                                                                                                                                                            |
| [**inviare tramite pipe**](pipe.md)                      | Consente la trasmissione di un flusso aperto di dati tipizzati in una chiamata di procedura remota. Un parametro [**in**](in.md) pipe consente al server di eseguire il pull del flusso di dati dal client durante una chiamata di procedura remota. Un parametro [**out**](-out.md) pipe consente al server di eseguire il push del flusso di dati al client. |
| [**Trasmetti \_ come**](transmit-as.md)       | Specifica il modo in cui un tipo di dati verrà trasmesso in una rete, usato per il marshalling personalizzato.                                                                                                                                                                                                                                  |
| [**\_enum V1**](v1-enum.md)               | Indica che il tipo enumerato specificato deve essere trasmesso come entità a 32 bit, anziché come valore predefinito a 16 bit.                                                                                                                                                                                                              |
| [**\_marshalling di rete**](wire-marshal.md)     | Simile a [**trasmettere \_ come**](transmit-as.md) , ma si implementano le routine per ridimensionare, effettuare il marshalling, annullare il marshalling e liberare i dati.                                                                                                                                                                                              |



 

 

 




