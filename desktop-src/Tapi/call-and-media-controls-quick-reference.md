---
description: La tabella seguente elenca le interfacce COM della versione 3 di TAPI per categoria in ordine di importanza.
ms.assetid: fafb6d6e-934e-4942-8b90-dacb7ba09752
title: Riferimento rapido ai controlli Call e media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ed3105612205d6d516b8d0c5e4f0a7bf9719b3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320593"
---
# <a name="call-and-media-controls-quick-reference"></a>Riferimento rapido ai controlli Call e media

\[ Le [interfacce msp IPConf](ipconf-msp-interfaces.md) non sono disponibili per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

La tabella seguente elenca le interfacce COM della versione 3 di TAPI per categoria in ordine di importanza. Le interfacce sono raggruppate in base ai cinque oggetti di controllo delle chiamate di base di TAPI 3: TAPI, Address, Terminal, Call e CallHub. Le interfacce rimanenti vengono raggruppate in base alle interfacce ACD (Automatic Call Distribution), che forniscono funzionalità del Call-Center; interfacce di enumeratore e oggetti autonomi.



| Raggruppamenti di interfacce                                          | Descrizione                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfacce di oggetti TAPI](tapi-object-interfaces.md)         | L'oggetto TAPI è l'oggetto principale per TAPI 3.                                                                                                                                                                                                              |
| [Interfacce dell'oggetto Address](address-object-interfaces.md)   | L'oggetto Address rappresenta un'entità che può effettuare o ricevere chiamate. Le interfacce e i metodi associati consentono a un'applicazione di ottenere e impostare informazioni relative all'indirizzo, ad esempio se dispone del supporto per l'ID chiamante.                             |
| [Interfacce di oggetti Terminal](terminal-object-interfaces.md) | L'oggetto terminale rappresenta il sink o l'origine in corrispondenza del punto di terminazione o di origine di una chiamata. Le interfacce e i metodi associati consentono a un'applicazione di ottenere e impostare le informazioni relative al terminale, ad esempio se sono attualmente in uso. |
| [Chiama interfacce oggetto](call-object-interfaces.md)         | L'oggetto call rappresenta una chiamata e viene creato quando entra in vigore una chiamata. Le interfacce e i metodi associati ottengono e impostano informazioni relative alla chiamata, ad esempio lo stato corrente della chiamata.                                                           |
| [Interfacce per oggetti telefono](phone-object-interfaces.md)       | L'oggetto telefono è l'entità che rappresenta il dispositivo telefonico effettivo e tutti i relativi controlli.                                                                                                                                                             |
| [Interfacce MSP IPConf](ipconf-msp-interfaces.md)           | Il MSP di conferenza IP implementa diverse interfacce per il controllo partecipante esposte nell'oggetto chiamata.                                                                                                                                          |
| [Interfacce oggetto CallHub](callhub-object-interfaces.md)   | L'oggetto CallHub rappresenta una vista di terze parti di una chiamata a più parti. Le interfacce e i metodi associati ottengono e impostano le informazioni relative alla chiamata, ad esempio se l'hub chiamate è attivo o meno.                                                          |
| [Interfacce enumeratore](enumerator-interfaces.md)           | Interfacce dell'enumeratore standard COM.                                                                                                                                                                                                                         |
| [Interfacce evento](./event-interfaces.md)            | Le interfacce eventi vengono inoltre visualizzate con i relativi raggruppamenti di oggetti o funzioni.                                                                                                                                                                                |
| [Oggetti autonomi](stand-alone-objects.md)               | Gli oggetti autonomi di TAPI 3 vari forniscono interfacce e metodi per operazioni quali la telefonia assistita o la gestione degli eventi.                                                                                                                    |



 

 

 
