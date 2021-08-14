---
description: Applicazione WpdApiSample
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Applicazione WpdApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef1741f2cad07e28bee514cf6109cdbbf7347966e1a8184a88a11936cbccdcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963470"
---
# <a name="wpdapisample-application"></a>Applicazione WpdApiSample

L'applicazione di esempio WpdApiSample è un'applicazione desktop da riga di comando che consente di enumerare i dispositivi connessi, esplorare i dispositivi, eseguire query su oggetti per proprietà e attributi, inviare e recuperare oggetti e così via. All'avvio, l'applicazione apre una finestra di comando che elenca le attività che è possibile eseguire.

L'applicazione di esempio WpdApiSample include i file seguenti:



| **File**               | **Descrizione**                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration.cpp | Contiene funzioni che enumerano tutti gli oggetti in un dispositivo.                                                                                                                                            |
| ContentProperties.cpp  | Contiene funzioni che leggono e scrivono proprietà dell'oggetto e effettuano richieste bulk di set/get di proprietà.                                                                                                         |
| ContentTransfer.cpp    | Contiene funzioni che trasferiscono il contenuto da o verso il dispositivo, leggono i requisiti del tipo di oggetto e creano una cartella nel dispositivo.                                                                         |
| DeviceCapabilities.cpp | Contiene funzioni per elencare i tipi di oggetti funzionali nel dispositivo, elencare i tipi di contenuto supportati da ogni tipo di oggetto funzionale e visualizzare i profili degli oggetti di rendering.                             |
| DeviceEnumeration.cpp  | Elenca i nomi descrittivi, i produttori e le descrizioni di tutti i dispositivi connessi.                                                                                                                       |
| DeviceEvents.cpp       | Contiene funzioni che registrano gli eventi del dispositivo e i relativi parametri ogni volta che vengono generati eventi.                                                                                                                 |
| stdafx.cpp             | Include i file standard.                                                                                                                                                                              |
| WpdApiSample.cpp       | Ospita la funzione di avvio **\_ tmain,** che chiama la funzione **DoMenu** locale, che visualizza un elenco di dispositivi e attività disponibili e chiama la funzione appropriata per la selezione del menu dell'utente. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio](sample.md)
</dt> </dl>

 

 



