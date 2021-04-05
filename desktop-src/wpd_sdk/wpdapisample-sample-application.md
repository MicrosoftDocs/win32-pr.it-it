---
description: Applicazione WpdApiSample
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Applicazione WpdApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751183"
---
# <a name="wpdapisample-application"></a>Applicazione WpdApiSample

L'applicazione di esempio WpdApiSample è un'applicazione desktop da riga di comando che consente di enumerare i dispositivi connessi, esplorare i dispositivi, eseguire query sugli oggetti per proprietà e attributi, inviare e recuperare oggetti e così via. All'avvio, l'applicazione apre una finestra di comando in cui sono elencate le attività che è possibile eseguire.

L'applicazione di esempio WpdApiSample include i file seguenti:



| **File**               | **Descrizione**                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ContentEnumeration. cpp | Contiene funzioni che enumerano tutti gli oggetti in un dispositivo.                                                                                                                                            |
| ContentProperties. cpp  | Contiene funzioni che leggono e scrivono le proprietà degli oggetti ed effettuano richieste Bulk set/get.                                                                                                         |
| ContentTransfer. cpp    | Contiene funzioni che trasferiscono il contenuto al o dal dispositivo, leggono i requisiti del tipo di oggetto e creano una cartella nel dispositivo.                                                                         |
| DeviceCapabilities. cpp | Contiene funzioni per elencare i tipi di oggetto funzionali nel dispositivo, elencare i tipi di contenuto supportati da ogni tipo di oggetto funzionale e visualizzare i profili degli oggetti di rendering.                             |
| DeviceEnumeration. cpp  | Elenca i nomi descrittivi, i produttori e le descrizioni di tutti i dispositivi connessi.                                                                                                                       |
| DeviceEvents. cpp       | Contiene funzioni che registrano gli eventi del dispositivo e i relativi parametri ogni volta che vengono generati eventi.                                                                                                                 |
| stdafx.cpp             | Include i file standard.                                                                                                                                                                              |
| WpdApiSample. cpp       | Ospita la funzione di avvio **\_ tmain** , che chiama la funzione **DoMenu** locale che visualizza un elenco di dispositivi e attività disponibili e chiama la funzione appropriata per la selezione di menu dell'utente. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio](sample.md)
</dt> </dl>

 

 



