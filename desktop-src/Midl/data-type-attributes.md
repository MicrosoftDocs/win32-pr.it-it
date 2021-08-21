---
title: Attributi del tipo di dati
description: È possibile applicare questi attributi ai tipi di dati in un'istruzione typedef per definire ulteriormente l'utilizzo o l'effetto del tipo di dati.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- IDL MIDL, attributi, tipo di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85142c13d9b478c449bf07955b85dd586b6312d891e17699861afb5bc2cc658b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067371"
---
# <a name="data-type-attributes"></a>Attributi del tipo di dati

È possibile applicare questi attributi ai tipi di dati in [**un'istruzione typedef**](typedef.md) per definire ulteriormente l'utilizzo o l'effetto del tipo di dati.



| Attributo                                 | Utilizzo                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**handle di \_ contesto**](context-handle.md) | Identifica un handle di associazione che gestisce le informazioni sullo stato (contesto) in un determinato server tra chiamate di procedura remota da un client specifico. Non valido per le [**funzioni dell'interfaccia**](object.md) a oggetti.                                                                                                         |
| [**Gestire**](handle.md)                  | Specifica un tipo di handle personalizzato specifico per l'applicazione.                                                                                                                                                                                                                                                                |
| [**ms \_ union**](-ms-union.md)            | Controlla l'allineamento del rapporto di mancato recapito delle unioni non incapsulate. Usare in [**typedef**](typedef.md)s per la compatibilità con le versioni precedenti con le interfacce compilate con MIDL 1.0 o 2.0.                                                                                                                                                            |
| [**inviare tramite pipe**](pipe.md)                      | Consente la trasmissione di un flusso aperto di dati tipiati in una chiamata di procedura remota. Un [**parametro della**](in.md) pipe in consente al server di eseguire il pull del flusso di dati dal client durante una chiamata di procedura remota. Un [**parametro out**](-out.md) pipe consente al server di eseguire il push del flusso di dati al client. |
| [**trasmettere \_ come**](transmit-as.md)       | Specifica la modalità di trasmissione di un tipo di dati in una rete, utilizzata per il marshalling personalizzato.                                                                                                                                                                                                                                  |
| [**Enumerazione \_ v1**](v1-enum.md)               | Indica che il tipo enumerato specificato viene trasmesso come entità a 32 bit, anziché come valore predefinito a 16 bit.                                                                                                                                                                                                              |
| [**wire \_ marshal**](wire-marshal.md)     | Analogamente alla [**\_ trasmissione come**](transmit-as.md) , ma si implementano le routine per ridimensionare, effettuare il marshalling, annullare il marshalling e liberare i dati.                                                                                                                                                                                              |



 

 

 




