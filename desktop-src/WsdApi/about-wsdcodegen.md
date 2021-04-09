---
description: Descrive i file di input utilizzati da WsdCodeGen e i file di output generati da WsdCodeGen.
ms.assetid: 990511ca-a918-460b-91e0-c1454e242f17
title: Informazioni su WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073530560e7923f0e67ba888f168a669d6ba5561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049810"
---
# <a name="about-wsdcodegen"></a>Informazioni su WsdCodeGen

WsdCodeGen utilizza un file di configurazione XML per determinare il percorso dei metadati del servizio. Il file di configurazione viene usato anche per definire i nomi di interfaccia, i GUID di interfaccia, i nomi delle classi, i nomi dei metodi e altri identificatori. Per ulteriori informazioni su questo file, vedere [WsdCodeGen Configuration file](wsdcodegen-configuration-file.md).

WsdCodeGen richiede due tipi di file di input: un file di configurazione XML e uno o più file di descrizione del servizio (file WSDL e/o XSD). WsdCodeGen elabora questi file di input e genera due tipi di file di output: file di interfaccia e file di intestazione e di origine.

## <a name="input-files"></a>File di input



| Tipo                      | Descrizione                                                                                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| File di configurazione        | Un file XML che indica il percorso dei metadati del servizio e definisce i nomi delle interfacce, i GUID dell'interfaccia, i nomi delle classi, i nomi dei metodi e altri identificatori. |
| File di descrizione del servizio | Uno o più file WSDL o XSD che descrivono i servizi da implementare nel dispositivo.                                                                           |



 

## <a name="output-files"></a>File di output



| Tipo                        | Descrizione                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| File di interfaccia             | File IDL (Interface Definition Language) che può essere usato con il compilatore MIDL per produrre un file di intestazione di interfaccia. I client WSDAPI e i servizi WSDAPI possono usare questo file di interfaccia.                                                                                                                                                           |
| Intestazione C++ e file di origine | File C++ che descrivono le informazioni sul contratto di messaggio, lo spazio dei nomi e il tipo. Possono contenere codice proxy e/o codice stub. Il codice proxy implementa un'interfaccia del servizio e converte le chiamate al metodo del servizio in operazioni WSDAPI che effettuano richieste di servizio. Il codice stub converte le richieste di servizio WSDAPI in codice che chiama i metodi del servizio. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Generatore di codice dei servizi Web nei dispositivi](web-services-for-devices-code-generator.md)
</dt> <dt>

[Uso di WsdCodeGen](using-wsdcodegen.md)
</dt> </dl>

 

 



