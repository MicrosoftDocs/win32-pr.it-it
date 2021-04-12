---
description: Nel tempo è possibile che vengano generate versioni diverse di TAPI, applicazioni e provider di servizi.
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: Controllo delle versioni di TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8565eb6282fd124c4f43e56d121ba7c053143683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346786"
---
# <a name="tapi-versioning"></a>Controllo delle versioni di TAPI

Nel tempo è possibile che vengano generate versioni diverse di TAPI, applicazioni e provider di servizi. Queste nuove versioni possono creare nuove definizioni, ad esempio per nuove funzionalità, nuovi membri nelle strutture di dati e nuovi campi di bit. I numeri di versione sono pertanto necessari per indicare come interpretare diverse strutture di dati.

Per consentire l'interoperabilità ottimale di versioni diverse di applicazioni, versioni di TAPI e versioni di provider di servizi da fornitori diversi, la telefonia Microsoft fornisce un meccanismo di negoziazione della versione semplice per le applicazioni. Esistono due versioni diverse che TAPI e il provider di servizi di telefonia devono accettare per ogni dispositivo di linea. Il primo è la versione negoziata con TAPI e la telefonia Basic e complementare del provider di servizi di telefonia (TSP), denominata versione dell'interfaccia TAPI. L'altro è per le estensioni specifiche del provider, se presente, e viene indicato come versione dell'estensione. Il formato delle strutture di dati e dei tipi di dati usati dalle funzionalità di base e supplementare di TAPI è definito dalla versione TAPI, mentre la versione dell'estensione determina il formato delle strutture di dati definite dalle estensioni specifiche del fornitore.

La funzione [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) negozia una versione TAPI e [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) negozia la versione dell'estensione TSP. Un singolo TSP può essere in grado di gestire più di una versione e un'applicazione deve eseguire il fallback all'utilizzo di una versione precedente se si utilizza un TSP precedente. In **lineNegotiateAPIVersion** il valore predefinito del parametro *dwApiVersion* è un valore in base alla versione, come indicato di seguito.



| Versione TAPI | Valore predefinito |
|--------------|---------------|
| 1.3          | 0x00010003    |
| 1.4          | 0x00010004    |
| 2.0          | 0x00020000    |
| 2.1          | 0x00020001    |
| 2.2          | 0x00020002    |



 

Tuttavia, TAPI rende questa operazione molto più semplice purché il TSP stesso stia usando una versione più recente dell'applicazione. Se il TSP è effettivamente più recente, TAPI è in grado di tradurre "Down" nella versione dell'applicazione. Ad esempio, TAPI 2,0 TSPs non deve essere specificamente in grado di gestire la versione di TAPI 1,4. Se viene eseguita un'applicazione TAPI 1,4, TAPI converte tutti i messaggi e le strutture TAPI 2,0 negli equivalenti di TAPI 1,4 o il più vicino possibile. Se non è presente alcuna approssimazione vicina in TAPI 1,4, tutte le informazioni specifiche di TAPI 2,0 andranno perse.

Il significato esatto di una versione dell'estensione è specifico del provider. Per usare un TSP che supporta le estensioni, consultare la documentazione del provider.

Sono disponibili diverse versioni di TAPI. Anche se la maggior parte di queste versioni implica modifiche ai set di documentazione TSPI (TAPI and phony Service Provider Interface), esistono altre implicazioni per ogni versione, vale a dire le differenze di architettura, le variazioni del sistema operativo, i ridistribuibili e i problemi di sviluppo di TSP.



| Versione TAPI        | Distribuzione                                                   |
|---------------------|----------------------------------------------------------------|
| 1,0 – 1,2           | Versioni beta che non devono essere più utilizzate.              |
| [1.4](tapi-1-4.md) | Incluso in Windows 95.                                        |
| [1,5](tapi-1-5.md) | Incluso in Windows CE 1,0.                                    |
| [2.0](tapi-2-0.md) | Incluso in Windows NT 4,0 con SP3.                           |
| [2.1](tapi-2-1.md) | Incluso in Windows NT 4,0 con SP4 e Windows 98.            |
| [2.2](tapi-2-2.md) | Incluso in Windows Server 2003, Windows XP e Windows 2000. |



 

 

 



