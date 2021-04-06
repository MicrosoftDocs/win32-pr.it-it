---
title: Attributi di aliasing e marshalling
description: Le applicazioni distribuite passano quasi sempre i dati tra i programmi client e server quando chiamano procedure di interfaccia.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- IDL MIDL, attributi MIDL, aliasing e marshalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045295"
---
# <a name="aliasing-and-marshaling-attributes"></a>Attributi di aliasing e marshalling

Le applicazioni distribuite passano quasi sempre i dati tra i programmi client e server quando chiamano procedure di interfaccia. Gli sviluppatori utilizzano MIDL per descrivere i dati che i programmi client e server passano in modo standard. Il compilatore MIDL crea Stub applicazione, o proxy, programmi per il client e il server che convertono i dati in un formato standardizzato che può essere inviato in rete. Questo formato, il formato di rappresentazione dei dati di rete (NDR), viene spesso definito formato wire dei dati. Gli stub devono convertire i dati dal formato nativo nello spazio di memoria del programma in un rapporto di mancato recapito. Questa conversione viene definita marshalling dei dati. Quando un client o un programma server riceve dati, deve convertire i dati da NDR al formato nativo per il programma. Questa operazione è denominata unmarshaling the data.

Usare gli attributi di aliasing e di marshalling per controllare come i dati vengono inseriti in un pacchetto in formato NDR e trasmessi in rete.



| Attributo                             | Utilizzo                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**chiama \_ come**](call-as.md)           | Esegue il mapping di una funzione non a una chiamata di procedura remota.                                                                      |
| [**IID \_ è**](iid-is.md)             | Fornisce l'identificatore di interfaccia dell'interfaccia COM che rappresenta l'oggetto dell'indicatore di misura.                                     |
| [**Trasmetti \_ come**](transmit-as.md)   | Converte un tipo di dati in un tipo più semplice per la trasmissione in rete.                                                       |
| [**\_marshalling di rete**](wire-marshal.md) | Simile a [**trasmettere \_ come**](transmit-as.md) , ma si implementano le routine per ridimensionare, effettuare il marshalling, annullare il marshalling e liberare i dati. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione di tipi e attributi ACF di marshalling](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




