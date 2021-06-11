---
description: Informazioni sul controllo delle versioni TAPI. Nel corso del tempo possono essere prodotte versioni diverse di TAPI, applicazioni e provider di servizi.
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: Controllo delle versioni TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853cf9d5f3744e11936f121986edc4e6e027d251
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989296"
---
# <a name="tapi-versioning"></a>Controllo delle versioni TAPI

Nel corso del tempo possono essere prodotte versioni diverse di TAPI, applicazioni e provider di servizi. Queste nuove versioni possono creare nuove definizioni, ad esempio per le nuove funzionalità, nuovi membri nelle strutture di dati e nuovi campi di bit. I numeri di versione sono quindi necessari per indicare come interpretare varie strutture di dati.

Per consentire l'interoperabilità ottimale di versioni diverse di applicazioni, versioni di TAPI e versioni di provider di servizi di fornitori diversi, Microsoft Telefonia fornisce un semplice meccanismo di negoziazione della versione per le applicazioni. Esistono due versioni diverse su cui TAPI e il provider di servizi di telefonia devono concordare per ogni dispositivo line. Il primo è la versione negoziata con TAPI e il provider di servizi di telefonia (TSP) Basic e telefonia supplementare, detta versione dell'interfaccia TAPI. L'altra è per le estensioni specifiche del provider, se presenti, e viene definita versione dell'estensione. Il formato delle strutture di dati e dei tipi di dati usati dalle funzionalità Di base e Supplementari di TAPI è definito dalla versione TAPI, mentre la versione dell'estensione determina il formato delle strutture di dati definite dalle estensioni specifiche del fornitore.

La [**funzione lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) negozia una versione TAPI e [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) negozia la versione dell'estensione TSP. Un singolo TSP potrebbe essere in grado di gestire più di una versione e un'applicazione deve "eseguire il fall back" all'uso di una versione precedente se si usa un TSP meno recente. In **lineNegotiateAPIVersion** il valore predefinito del parametro *dwApiVersion* è un valore in base alla versione, come indicato di seguito.



| Versione TAPI | Valore predefinito |
|--------------|---------------|
| 1.3          | 0x00010003    |
| 1.4          | 0x00010004    |
| 2,0          | 0x00020000    |
| 2.1          | 0x00020001    |
| 2.2          | 0x00020002    |



 

Tuttavia, TAPI rende questa operazione molto più semplice, purché il provider di servizi di configurazione stesso utilizzi una versione più recente rispetto all'applicazione. Se il TSP è effettivamente più recente, TAPI è in grado di convertire "verso il basso" la versione dell'applicazione. Ad esempio, i TSP TAPI 2.0 non devono essere specificamente in grado di gestire TAPI versione 1.4. Se viene eseguita un'applicazione TAPI 1.4, TAPI converte tutte le strutture e i messaggi TAPI 2.0 in equivalenti TAPI 1.4 o il più vicino possibile. Se non è presente alcuna approssimazione vicina in TAPI 1.4, tutte le informazioni specifiche di TAPI 2.0 andranno perse.

Il significato preciso di una versione dell'estensione è specifico del provider. Per usare un provider di servizi di configurazione che supporta le estensioni, consultare la documentazione del provider.

Esistono diverse versioni di TAPI. Anche se la maggior parte di queste versioni comporta modifiche ai set di documentazione TAPI e TSPI (Telefonia Service Provider Interface), esistono altre implicazioni per ogni versione, ovvero differenze a livello di architettura, variazioni del sistema operativo, ridistribuibili e problemi di sviluppo TSP.



| Versione TAPI        | Distribuzione                                                   |
|---------------------|----------------------------------------------------------------|
| 1.0 – 1.2           | Versioni beta che non devono più essere usate.              |
| [1.4](tapi-1-4.md) | Incluso in Windows 95.                                        |
| [1.5](tapi-1-5.md) | Incluso in Windows CE 1.0.                                    |
| [2.0](tapi-2-0.md) | Incluso in Windows NT 4.0 con SP3.                           |
| [2.1](tapi-2-1.md) | Incluso in Windows NT 4.0 con SP4 e Windows 98.            |
| [2.2](tapi-2-2.md) | Incluso in Windows Server 2003, Windows XP e Windows 2000. |



 

 

 



